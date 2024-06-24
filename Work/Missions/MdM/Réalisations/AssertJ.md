**AssertJ**

- Comment ça fonctionne
    - Overloading
    - Fluent Interface Pattern
- Exemples d’utilisation
    - Syntaxe de base
        - expect/actual vs JUnit
    - Collections
        - Méthodes utilitaires
        - Matchers et Prédicates
    - Exceptions

```java
package demo.assertj;

import org.assertj.core.api.*;
import org.junit.jupiter.api.Nested;
import org.junit.jupiter.api.Test;

import java.util.List;
import java.util.Objects;

import static org.assertj.core.api.Assertions.assertThat;
import static org.assertj.core.api.Assertions.tuple;
import static org.assertj.core.api.InstanceOfAssertFactories.type;
import static org.junit.jupiter.api.Assertions.assertEquals;
import static org.junit.jupiter.api.Assertions.assertThrows;

class AssertJDemoTest {


    @Test
    void basic_usages() {
        // JUNIT
        assertEquals("TOTO", "TATA");

        // ASSERTJ
        Assertions.assertThat("TATA")
                .isEqualTo("TOTO");
    }

    @Test
    void examples_on_numbers() {
        Assertions.assertThat(12L)
                .isPositive()
                .isGreaterThan(10);
    }

    @Test
    void examples_on_strings() {
        Assertions.assertThat("TATA")
                .isNotNull()
                .hasLineCount(12)
                .isBlank()
                .isNotBlank()
                .isEqualToIgnoringCase("TOTO");
    }

    @Test
    void cast_properly_does_not_allow_to_use_build_in_asserts() {
        Object stingAsObject = "TATA";
        Assertions.assertThat(stingAsObject)
                .isNotNull()
                .asInstanceOf(type(String.class))
//                .hasLineCount(12)
//                .isBlank()
//                .isNotBlank()
//                .isEqualToIgnoringCase("TOTO");
                .satisfies(string -> assertThat(string)
                        .isNotBlank());
    }

    //
    // COLLECTIONS
    //

    static class Pojo {
        String name;
        String description;

        public Pojo(String name, String description) {
            this.name = name;
            this.description = description;
        }

        public String getName() {
            return name;
        }

        public String getDescription() {
            return description;
        }
    }

    @Nested
    class CollectionsExamples {
        @Test
        void basic_lists_examples() {
            // JUNIT
            assertEquals(List.of("TOTO", "TITI", "TATA"),
                    List.of("TOTO", "TUTU"));

            // ASSERTJ
            assertThat(List.of("TOTO", "TITI", "TATA"))
                    .hasSize(3)
                    .containsExactly("TOTO", "TUTU")
//                    .containsExactlyInAnyOrder("TOTO", "TUTU")
            ;
        }

        @Test
        void lists_matchers_examples() {
            List<Pojo> pojoLis = List.of(
                    new Pojo("OK", "desc"),
                    new Pojo("OK", "Description"),
                    new Pojo("KO", "Stacktrace"));

            assertThat(pojoLis)
                    .extracting(Pojo::getName)
                    .allMatch(name -> name.equals("OK"))
                    .noneMatch(Objects::isNull)
                    .anyMatch(Objects::isNull)
            ;
        }

        @Test
        void lists_satisfies_examples() {
            List<Pojo> pojoLis = List.of(
                    new Pojo("OK", "desc"),
                    new Pojo("OK", "Description"),
                    new Pojo("KO", "Stacktrace"));

            assertThat(pojoLis)
                    .anySatisfy(pojo -> {
                        assertThat(pojo)
                                .isNotNull()
                                .isEqualTo(new Pojo("Ok", "desc"));
                    })
            ;
        }

        @Test
        void lists_extraction_examples() {
            List<Pojo> pojoLis = List.of(
                    new Pojo("OK", "desc"),
                    new Pojo("OK", "Description"),
                    new Pojo("KO", "Stacktrace"));

            assertThat(pojoLis)
                    .extracting(Pojo::getName)
                    .containsExactly("OK", "OK", "KO")
            ;
        }

        @Test
        void lists_extraction_tuple_examples() {
            List<Pojo> pojoLis = List.of(
                    new Pojo("OK", "desc"),
                    new Pojo("OK", "Description"),
                    new Pojo("KO", "Stacktrace"));

            assertThat(pojoLis)
                    .extracting(Pojo::getName, Pojo::getDescription)
                    .containsExactly(
                            tuple("OK", "desc"),
                            tuple("OK", "Description"),
                            tuple("KO", "Stacktrace")
                    )
            ;
        }
    }

    //
    // EXCEPTIONS
    //

    static class CustomRuntimeException extends RuntimeException {

        public String getCode() {
            return "String";
        }

        public Pojo getSomeCustomData() {
            return new Pojo("", "");
        }
    }

    @Nested
    class ExceptionExamples {

        @Test
        void bascis_examples() {
            // JUNIT
            var metierException = assertThrows(CustomRuntimeException.class, () -> throwSomeException());
            assertEquals(metierException.getMessage(), "Message de l'erreur");
            assertEquals(metierException.getCode(), "UN_CODE");
            assertEquals(metierException.getSomeCustomData().getName(), "UN_CODE");

            // ASSERTJ
            Assertions.assertThatThrownBy(() -> throwSomeException())
                    .hasMessage("Message de l'erreur")
                    .hasCause(new RuntimeException())
                    .isInstanceOf(CustomRuntimeException.class)
                    .asInstanceOf(type(CustomRuntimeException.class)) // Nécessaire pour gérer la récupération des trucs customs
                    .satisfies(exception ->
                            assertThat(exception.getSomeCustomData())
                                    .isEqualTo(new Pojo("OK", "DESC"))
                    );
        }

    }

    static void throwSomeException() {
        throw new CustomRuntimeException();
    }

}
```

# Fluent Interface

```java
package com.mdm.demo.assertj;

import java.util.Collection;
import java.util.List;

public class FluentInterface {
    public static SomeSteps doSomethingWithSteps() {
        return new SomeSteps();
    }

    public static FluentInterFaceWithOverLoading exampleWithOverLoading() {
        return null;
    }

    public static class SomeSteps {
        public FirstStep firstStep() {
            return new FirstStep();
        }

        public FirstStepBis firstStepForOtherProcess() {
            return new FirstStepBis();
        }

        public class FirstStep {
            public SecondStep secondStep() {
                return null;
            }

            public class SecondStep {
                SomeSteps terminate() {
                    return SomeSteps.this;
                }
            }
        }
    }

    public static class FirstStepBis {
        public FirstStepBis optionalStepAvailableOnFirstStepBis() {
            return this;
        }

        public SecondStepBbis secondStep() {
            return new SecondStepBbis();
        }

    }

    public static class SecondStepBbis {
    }

    public static class FluentInterFaceWithOverLoading {
        public IntegerFirstStep firstStep(int intergerInput) {
            return firstStepWithInteger(intergerInput);
        }

        public <T extends Collection<?>> CollectionsFirstStep firstStep(T anyCollection) {
            return firstStepForCollections(anyCollection);
        }

        public IntegerFirstStep firstStepWithInteger(int integer) {
            return new IntegerFirstStep();
        }

        public <T extends Collection<?>> CollectionsFirstStep firstStepForCollections(T anyCollection) {
            return new CollectionsFirstStep();
        }

        public class IntegerFirstStep {
            public IntegerSecondStep secondStepOnlyForIntergerMethod() {
                return new IntegerSecondStep();
            }

            public class IntegerSecondStep {

                public FluentInterFaceWithOverLoading terminate() {
                    return FluentInterFaceWithOverLoading.this;
                }
            }
        }

        public class CollectionsFirstStep {
            public CollectionsFirstStep optionalStepForCollections() {
                return this;
            }

            public CollectionsSecondStep secondStepOnlyForCollections() {
                return new CollectionsSecondStep();
            }

            public class CollectionsSecondStep {


                public FluentInterFaceWithOverLoading terminate() {
                    return FluentInterFaceWithOverLoading.this;
                }
            }

        }
    }
}

package com.mdm.demo.assertj;

import org.junit.jupiter.api.Test;

import java.util.List;

class FluentInterfaceExamples {

    @Test
    void fluent_interface_decomposed_examples() {
        FluentInterface.SomeSteps steps = FluentInterface.doSomethingWithSteps();

        FluentInterface.SomeSteps.FirstStep firstStep = steps.firstStep();
        FluentInterface.SomeSteps.FirstStep.SecondStep secondStep = firstStep.secondStep();
        steps = secondStep.terminate();


        FluentInterface.FirstStepBis firstStepBis = steps.firstStepForOtherProcess();
        firstStepBis = firstStepBis.optionalStepAvailableOnFirstStepBis();
        FluentInterface.SecondStepBbis secondStepBis = firstStepBis.secondStep();
    }

    @Test
    void fluent_interface_examples() {

        FluentInterface.doSomethingWithSteps()
                .firstStep()
                .secondStep()
                .terminate()

                .firstStepForOtherProcess()
                .optionalStepAvailableOnFirstStepBis()
                .secondStep();
    }

    @Test
    void fluent_interface_with_overloading_examples() {

        FluentInterface.exampleWithOverLoading()
                .firstStepWithInteger(12)
                .secondStepOnlyForIntergerMethod()
                .terminate()

                .firstStepForCollections(List.of())
                .optionalStepForCollections()
                .secondStepOnlyForCollections()
                .terminate();

        FluentInterface.exampleWithOverLoading()
                .firstStep(12)
                .secondStepOnlyForIntergerMethod()
                .terminate()

                .firstStep(List.of())
                .optionalStepForCollections()
                .secondStepOnlyForCollections()
                .terminate();
    }
}
```

# Overloading

```java
package com.mdm.demo.assertj;

import java.math.BigDecimal;
import java.util.Collection;

public class Overloading {

    public void overloadedMethod(){
        // Some Stuff
    }

    public int overloadedMethod(String stringInput){
        return -1;
    }

    public Class<?> overloadedMethod(Collection<?> stringInput){
        return OverloadingExample.class;
    }

}

package com.mdm.demo.assertj;

import org.assertj.core.api.AbstractIntegerAssert;
import org.assertj.core.api.AbstractStringAssert;
import org.assertj.core.api.ListAssert;
import org.assertj.core.api.ObjectAssert;
import org.junit.jupiter.api.Nested;
import org.junit.jupiter.api.Test;

import java.util.List;

import static org.assertj.core.api.Assertions.assertThat;

@Nested
class OverloadingExamples {

    @Test
    void overloading_examples() {
        Overloading example = new Overloading();

        int result = example.overloadedMethod("Overload String");

        Class<?> aClass = example.overloadedMethod(List.of());

    }

    @Test
    void assertJ_overloading_examples() {
        ObjectAssert<Object> objectAssert = assertThat(new Object());

        AbstractIntegerAssert<?> integerAssert = assertThat(12);

        AbstractStringAssert<?> stringAssert = assertThat("actual String");

        ListAssert<?> objectListAssert = assertThat(List.of());
    }

}
```