**Either** est un concept très simple qui a été démocratisé par les langages de programmation fonctionnelle.

Il s'agit d'un type (une classe) qui représente un valeur pouvant prendre deux types possibles
- le type de gauche : Left
- le type de droite : Right

L'idée est de pouvoir avoir un unique type de retour (Either) pour une fonction **pure** ([https://fr.wikipedia.org/wiki/Fonction_pure](https://fr.wikipedia.org/wiki/Fonction_pure) ), et de pouvoir utiliser des fonctions de **map**/**reduce** dessus (comme ce qu'on peut faire en Java avec des Optional, des Stream ou des Mono).

Souvent, le type de gauche représente une erreur ou des exception (car "_right is right_"et "_right is not an error_").

### Autres ressources
- Either dans “Programming Kotlin” : [https://subscription.packtpub.com/book/programming/9781787126367/5/ch05lvl1sec77/either](https://subscription.packtpub.com/book/programming/9781787126367/5/ch05lvl1sec77/either)
- _The Either data type as an alternative to throwing exceptions_  
    [https://www.thoughtworks.com/insights/blog/either-data-type-alternative-throwing-exceptions](https://www.thoughtworks.com/insights/blog/either-data-type-alternative-throwing-exceptions)
- https://github.com/HadrienMP/result
- Histoire de relancer la machine : Either Vs. exceptions [https://dev.to/anthonyjoeseph/either-vs-exception-handling-3jmg](https://dev.to/anthonyjoeseph/either-vs-exception-handling-3jmg)

### **Exemple d'implémentation de Either en java**

```java
import java.util.function.BiFunction;
import java.util.function.Function;

public class Either<L, R>{
    public static final Either<?,?> EMPTY = new Either<>(null, null);
    final L left;
    final R right;
    Either(L left, R right) {
        this.left = left;
        this.right = right;
    }
    <V> Either<V, R> mapLeft(Function<L, V> mapper) {
        return new Either<>(
                mapper.apply(left),
                right
        );
    }
    <V> Either<L, V> mapRight(Function<R, V> mapper) {
        return new Either<>(
                left,
                mapper.apply(right)
        );
    }
    <V> Either<V, R> leftCombineWith(BiFunction<L, L, V> combiner, Either<L, ?> other) {
        return new Either<>(
                combiner.apply(left, other.left),
                right
        );
    }
    <V> Either<L, V> rightCombineWith(BiFunction<R, R, V> combiner, Either<?, R> other) {
        return new Either<>(
                left,
                combiner.apply(right, other.right)
        );
    }
    // /!\ Java 17 Feature PREVIEW
    <T> T fold(Function<L, T> leftFolder, Function<R, T> rightFolder) {
        return switch (this) {
            // Objectif : utiliser le pattern matching pour savoir quand est-ce qu'on renvoie un Left ou un Right
            case Either<L, R> l && l.left != null -> leftFolder.apply(l.left);
            case Either<L, R> r && r.right != null -> rightFolder.apply(r.right);
            default -> throw new IllegalStateException("Unexpected value: " + this);
        };
    }
}
```
### Autre exemple d'implémentation
```java
  
import java.util.List;  
import java.util.function.BiFunction;  
import java.util.function.Function;  
  
public class ResultOrErrors<R> {  
  
    private final Errors errors;  
    private final R result;  
  
    private ResultOrErrors(Errors errors, R result) {  
        this.result = result;  
        this.errors = errors;  
    }  
  
    public static <R> ResultOrErrors<R> errors(String errorMessage) {  
        return errors(Errors.single(errorMessage));  
    }  
  
    private static <R> ResultOrErrors<R> errors(Errors errors) {  
        return new ResultOrErrors<>(errors, null);  
    }  
  
    public static <R> ResultOrErrors<R> success(R result) {  
        return new ResultOrErrors<>(Errors.EMPTY, result);  
    }  
  
    public R result() {  
        return result;  
    }  
  
    public List<Error> errors() {  
        return errors.asList();  
    }  
  
    public boolean isSuccessful() {  
        return errors.isEmpty();  
    }  
  
    private boolean isEmpty() {  
        return result == null;  
    }  
  
    public <V> ResultOrErrors<V> map(Function<R, V> mapper) {  
        if (isEmpty() || !isSuccessful()) {  
            return errors(errors);  
        }  
        V mapped = mapper.apply(result);  
        return new ResultOrErrors<>(errors, mapped);  
    }  
  
    public <V> ResultOrErrors<V> flatMap(Function<R, ResultOrErrors<V>> mapper) {  
        if (isEmpty() || !isSuccessful()) {  
            return errors(errors);  
        }  
        ResultOrErrors<V> mapped = mapper.apply(result);  
        return mapped.withErrors(errors);  
    }  
  
    public ResultOrErrors<R> validate(Function<R, Errors> validator) {  
        return withErrors(validator.apply(result));  
    }  
  
    private ResultOrErrors<R> withErrors(Errors errors) {  
        return new ResultOrErrors<>(this.errors.addAll(errors), result);  
    }  
  
    public <T, V> ResultOrErrors<V> combineResults(BiFunction<R, T, V> combiner, ResultOrErrors<T> other) {  
        if (isEmpty() || other.isEmpty()) {  
            return ResultOrErrors.<V>errors(errors).withErrors(other.errors);  
        }  
        V newResult = combiner.apply(result, other.result);  
        return new ResultOrErrors<>(errors, newResult).withErrors(other.errors);  
    }  
  
    public <T> T fold(Function<Errors, T> errorFolder, Function<R, T> resultFolder) {  
        return isSuccessful()  
                ? resultFolder.apply(result)  
                : errorFolder.apply(errors);  
    }  
  
}

class Errors {  
    public static final Errors EMPTY = new Errors(List.of());  
    private final List<Error> errors;  
  
    static Errors single(String errorMessage) {  
        return of(Error.of(errorMessage));  
    }  
  
    public static Errors of(Error Error) {  
        return new Errors(List.of(Error));  
    }  
  
    public Errors(List<Error> errors) {  
        this.errors = List.copyOf(errors);  
    }  
  
    public boolean isEmpty() {  
        return errors.isEmpty();  
    }  
  
    public List<Error> asList() {  
        return List.copyOf(errors);  
    }  
  
    public Errors add(Error error) {  
        List<Error> mutableErrors = new ArrayList<>(errors);  
        mutableErrors.add(error);  
        return new Errors(mutableErrors);  
    }  
  
    public Errors addAll(Errors other) {  
        List<Error> mutableErrors = new ArrayList<>(errors);  
        mutableErrors.addAll(other.errors);  
        return new Errors(mutableErrors);  
    }  
}
```

### Exemple d'utilisation très basique :

```java
import com.mdm.error.FunctionalError;

import org.junit.jupiter.api.Test;
import org.springframework.http.ResponseEntity;
import reactor.core.publisher.Mono;
import java.io.IOException;
import java.io.UncheckedIOException;
import java.util.ArrayList;
import java.util.List;
import java.util.Optional;

import static org.assertj.core.api.Assertions.assertThat;

class EitherSandbox {
    Sample defaultSample = new Sample("Either Example", """
            Un example d'objet métier.
            Cet objet peut être plus ou moins complexe.
            """);
    @Test
    void either_permet_de_renvoyer_une_valeur_ou_une_autre() {
        Either<Error, Sample> either = new Either<>(null, defaultSample);
        // right is not an error
        // right is right
        boolean hasError = either.left != null;
        if (hasError) {
            Error error = either.left;
        } else {
            Sample result = either.right;
        }
    }
    @Test
    void either_permet_de_transformer_les_objets() {
        Optional<Sample> optional = Optional.of(defaultSample);
        Optional<String> optionalName = optional
                .map(Sample::name)
                .map(String::toUpperCase);
        Either<Error, Sample> either = new Either<>(null, defaultSample);
        Either<Error, String> eitherName = either
                .mapRight(Sample::name)
                .mapRight(String::toUpperCase);
        // Optional + feedback
    }

    @Test
    void pourquoi_either() {
        try {
            Sample sample = new Sample("Either Example", "Blabla"); // #1
            validate(sample); // #2
            writeInFile(sample);// #4
            sendToFTP(sample); // #6
        } catch (FunctionalError e) {
            // some stuff
            // #3
        } catch (IOException io) {
            // some stuff but different
            // #5
        }
        // #7 ?? Vraiment ?
        
        // Avec Either
        Either<Error, Sample> either = new Either<>(null, defaultSample);
        Either<FunctionalError, Sample> validatedEither = validateEither(either);
        Either<IOException, Sample> ioEither =  writeInFileEither(validatedEither);
    }
    
    @Test
    void either_avec_les_ResponseEntity() {
        Either<Error, Sample> either = new Either<>(null, defaultSample);
        ResponseEntity<Sample> folded;
        boolean hasError = either.left != null;
        if (hasError) {
            Error error = either.left;
            folded = ResponseEntity
                    .internalServerError()
                    .build();
        } else {
            Sample result = either.right;
            folded = ResponseEntity.ok(result);
        }
    }
    
    @Test
    void either_avec_les_mono() {
        Either<Error, Sample> either = new Either<>(null, defaultSample);
        Mono<Sample> folded;
        boolean hasError = either.left != null;
        if (hasError) {
            Error error = either.left;
            folded = Mono.error(new RuntimeException(error.message()));
        } else {
            Sample result = either.right;
            folded = Mono.just(result);
        }
    }
    
    @Test
    void either_permet_d_accumuler_les_objets() {
        Either<Error, Sample> either = new Either<>(new Error("Echec #1"), defaultSample);
        Either<Error, Sample> either2 = new Either<>(new Error("Echec #2"), defaultSample);
        Either<List<Error>, Sample> eitherErrorList = either
                .leftCombineWith(
                        (error, otherError) -> List.of(error, otherError),
                        either2);
        Either<List<Error>, Sample> moreErrors = new Either<>(List.of(new Error("Echec #3")), null);
        Either<List<Error>, Sample> allErrors = eitherErrorList.leftCombineWith(
                (errors, errors2) -> {
                    List<Error> objects = new ArrayList<>();
                    objects.addAll(errors);
                    objects.addAll(errors2);
                    return objects;
                }, moreErrors);
        assertThat(allErrors.left)
                .containsExactlyInAnyOrder(
                        new Error("Echec #1"),
                        new Error("Echec #2"),
                        new Error("Echec #3")
                );
    }
    @Test
    void either_dans_le_futur() {
        Either<Error, Sample> either = new Either<>(null, defaultSample);
        Sample folded = either.fold(
                error -> new Sample("", ""),
                sample -> sample
        );
    }
    // FIN
    
    /// PLACEHOLDERS POUR LA PREZ
    private void writeInFile(Sample sample) throws IOException {
        // some stuff
    }
    void validate(Sample sample) throws FunctionalError {
        // Some stuff
    }
    private void sendToFTP(Sample sample) {
        IOException e = new IOException("Vu!");
        throw new UncheckedIOException("Pas vu, pas pris !", e);
    }
    private Either<FunctionalError, Sample> validateEither(Either<Error, Sample> either) {
        return null;
    }
    private Either<IOException, Sample> writeInFileEither(Either<FunctionalError, Sample> validatedEither) {
        return null;
    }
    
    record Error(String message) {}
    
    record Sample(String name, String description) {}
}
```