# special theoretical method equation (#10045)
/root/Java & OO Fundamentals/Methods

It is possible for a method to call itself from its body.

- (x) True
- ( ) False

## Explanation

Yes, it is possible. This is called recursion (a method calling itself).

# Which of the following statements are true? (#10047)
/root/Java & OO Fundamentals/Garbage Collection

Which of the following statements are true?

- [x] finalize will always run before an object is garbage collected
- [ ] finalize may run before or after an object is garbage collected
- [ ] finalize will run when an object becomes unreachable
- [ ] finalize allows a programmer to free memory allocated to an object

## Explanation

1) finalize will always run before an object is garbage collected
2) finalize may run before or after an object is garbage collected
3) finalize will run when an object becomes unreachable
4) finalize allows a programmer to free memory allocated to an object
Finalize will always be run before an object is garbage collected. It cannot run after it is collected because by then the object will cease to exit. When an object becomes unreachable it will be eligible for garbage collection but there is no guarantee when finalize will run, only that it will run before garbage collection happens. The final option is a passable description of destructors in C++ but not of the finalize method in Java.

# Initializing Strings (#10055)
/root/Java & OO Fundamentals/Strings

Strings are initialized to an empty string.

- ( ) True
- (x) False

## Explanation

Strings are initialized to null, not an empty string.

# Putting class in the package (#10201)
/root/Java & OO Fundamentals/Packages

How does the following code behave?
File: java/lang/Test.java
```
package java.lang;public class Test {
      public static void main(String[] args) {
              System.out.println("Testing");
      }}
```


- ( ) It prints "Testing".
- ( ) It does not compile.
- ( ) It throws java.lang.PackageNotAllowed
- (x) It throws java.lang.RuntimeException

## Explanation

The above code compiles successfully, but it does not run. It throws:
java.lang.SecurityException: Prohibited package name: java.lang
which extends java.lang.RuntimeException. This happens because a program is not allowed to create classes in Java internal packages.

# Switch (#1106)
/root/Java & OO Fundamentals/Flow Control

Which variable may be used in a switch / case?

- [x] short
- [ ] float
- [ ] long
- [x] int
- [ ] boolean
- [x] byte
- [ ] double
- [x] char

## Explanation

Both the expression expressive and the constant expressions must be integers (byte, char, short, or int).

# bytecode and target platform (#11220)
/root/Java & OO Fundamentals/Platform

The bytecode generated from a java source file is dependent on the target platform (i.e. linux, windows, etc.)

- ( ) True
- (x) False

## Explanation

`False, java bytecode is platform independent.
This is the source of the well known slogan for java : &lt;i&gt;&quot;write once, run anywhere&quot;&lt;/i&gt;`

# || Operator (#11322)
/root/Java & OO Fundamentals/Operators

What is the right word for the "||" Operator?

- (x) Or
- ( ) And
- ( ) Abort
- ( ) Doesn't exist

## Explanation

http://download.oracle.com/javase/tutorial/java/nutsandbolts/operators.html

# String type (#11406)
/root/Java & OO Fundamentals/Strings

Java handles strings as...

- (x) instances of class String
- ( ) arrays of characters
- ( ) collections of Char instances
- ( ) arrays of integers

## Explanation

In the Java programming language, strings are objects. The String class is immutable, so that once it is created a String object cannot be changed.

# Choose the operations that can be performed? (#1196)
/root/Java & OO Fundamentals/Variables

Choose the operations that can be performed on String objects:

- [x] +
- [x] + =
- [ ] -
- [ ] %
- [ ] ^

## Explanation

The "+" and "+ =" operators are overlaoded in Java. They join the two operands into one String object.

# The difference between the JRE and the JDK (#11999)
/Java (core)/Java SE - basic/Misc/Vocabulary and Concepts

Please select all of the differences between the JDK (Java Development Kit) and the JRE (Java Runtime Environment).

- [x] The JDK includes a compiler, but the JRE does not.
- [x] The JDK includes development tools, but the JRE only contains the runtime environment.
- [ ] The JDK is pretty much the same as the JRE except that the JDK has been optimized for speed.

## Explanation

JDK = Java Development Kit
JRE = Java Runtime Environment
The JDK includes the JRE, along with lots of development tools like a compiler, javap, the Java Debugger (jdb), and so forth.

# Keywords (#12061)
/root/Java & OO Fundamentals/Variables

Which of the following are Java keywords?

- [ ] array
- [x] boolean
- [x] protected
- [x] super

## Explanation

boolean, super, protected
An array is a container object that holds a fixed number of values of a single type, but the word array isn't a keyword. 
Here is the list of keywords: 
http://java.sun.com/docs/books/tutorial/java/nutsandbolts/_keywords.html

# Object (#12220)
/root/Java & OO Fundamentals/Classes and Objects

java.lang.Object is the ultimate ancestor.

- (x) True
- ( ) False

## Explanation

Every object (arrays included) inherit from Object, either directly or indirectly.

# Naming convention for class and method names. (#12261)
/Java (core)/Java SE - basic/Misc/Naming

By convention, what is the difference between the name of a class and the name of a method?
Note: Consider regular class (i.e. static) and instance methods, but not constructors.

- ( ) The first letter of the method name should be uppercase while the first letter of the class name should be lowercase.
- ( ) The name of the class should contain only uppercase letters.
- (x) The first letter of the class name should be uppercase while the first letter of the method name should be lowercase.
- ( ) The name of the method should contain only uppercase letters.
- ( ) There is no difference.

## Explanation

This is a good conventional class:
```
public class ClassOne {
  private int instanceVariable;
  public String toString(){
      //...
  }}
```


# String property (#12309)
/root/Java & OO Fundamentals/Strings

String objects are immutable, i.e., it is not possible to modify a string object.
For example, if we write:
```
String s = "Test";
```
then the following line gives a compilation error
```
s = "Test Changed";
```


- ( ) True
- (x) False

## Explanation

String is immutable it means you cannot change the state of object but you can refer different object via same reference.

# Field modifiers (#12525)
/root/Java & OO Fundamentals/Variables

Which three are valid on line 2? (Choose three.)
```
1: public interface Status {2:  /* insert code here */ int MY_VALUE = 
10;3:  }
```


- [x] final
- [x] static
- [ ] native
- [x] public

## Explanation


```
FieldModifier: one of
 Annotation public protected private
 static final transient volatile
```

Cf. <a href="http://java.sun.com/docs/books/jls/third_edition/html/classes.html#78091">JLS 3rd edition, 8.3.1</a>

# Given: (#12722)
/root/Java & OO Fundamentals/Variables

Which is true?
```
public class CreditCard {
 private String cardlD;
 private Integer limit;
 public String ownerName;
 public void setCardlnformation(String cardlD, String ownerName, Integer limit) {
    this.cardlD = cardlD;
    this.ownerName = ownerName;
    this.limit = limit;
 }}
```


- ( ) The class is fully encapsulated. 
- ( ) The code demonstrates polymorphism. 
- (x) The ownerName variable breaks encapsulation.
- ( ) The cardlD and limit variables break polymorphism.
- ( ) The setCardlnformation method breaks encapsulation.

## Explanation



# variables initialise (#12867)
/root/Java & OO Fundamentals/Variables

Which of the following lines will compile without errors or warnings?

- [ ] byte b = 257;
- [x] int i = 12;
- [ ] char c = "b";
- [ ] float f = 1.3;
- [ ] boolean b = null;
- [x] boolean c = false;

## Explanation

float f = 1.3; - the loss of accuracy
char c = "b"; - Type mismatch
byte b = 257; and boolean b = null; - invalid value

# Abstract class (#13332)
/root/Java & OO Fundamentals/Classes and Objects

Can we declare a class both as abstract & final ?

- ( ) True
- (x) False

## Explanation

Abstract class needs subclasses. final keyword represents sub classes which cannot be created. So both are quite contradictory and cannot be used for same class

# % operator (#13496)
/root/Java & OO Fundamentals/Operators

What is the output of compiling and running the following class?
```
1: class Sixties {2:     public static void main(String[] args) {3:         int x = 
5;4:         int y = 
7;5:         System.out.print(((y * 
2) % x));6:         System.out.print(" " + (y % x));7:     }8: }
```


- ( ) 1 1
- ( ) 2 2 
- (x) 4 2
- ( ) 4 1

## Explanation

7 * 2 evaluates to 14, 14%5 evaluates to 4
and
7%5 evaluates to 2

# What is the result? (#13529)
/root/Java & OO Fundamentals/Flow Control

What would be the output of the following code snippet?
```
01: public class Test{ 02:      03:      public static void main(String[] args)04:      {05:          int num = 
1;06:          07:          while ( num++ < 
10 )08:          {09:              if (num % 
2 == 
0)10:                  continue;11:                          12:              System.out.print(num);13:          }14:      }15: }
```


- ( ) 3 5 7 9
- (x) 3579
- ( ) 3
5
7
9
- ( ) compile error.
- ( ) 246810

## Explanation



# Standard disassemble the code (#13636)
/root/Java & OO Fundamentals/Platform

Disassemble the code for Java, which provides standard JDK ?

- [x] javap

## Explanation

The javap command disassembles a class file. Its output depends on the options used. If no options are used, javap prints out the package, protected, and public fields and methods of the classes passed to it. javap prints its output to stdout.

# Java Memory Management (#13646)
/root/Java & OO Fundamentals/Garbage Collection

Every Java objects need to be destructed explicitly by programmer in order to prevent memory leak.

- ( ) True
- (x) False

## Explanation

Java platform utilizes the automatic memory management called Garbage Collection to take care of freeing dynamically allocated memory that is no longer referenced.

# True or False? (#13754)
/root/Java & OO Fundamentals/Classes and Objects

An abstract class can have static methods.

- (x) True
- ( ) False

## Explanation

Yes. Abstract class can have static methods.

# Static initialization (#13875)
/root/Java & OO Fundamentals/Classes and Objects

What will be the output?
```
01:  02: public class Actor {03:     Actor(String id) {04:         System.out.println("Actor " + id + " constructed");05:     }06: }07: 08: public class Stage {09:     Actor a1 = new Actor("a1");10:     static Actor a2 = new Actor("a2");11: 12:     Stage(String id) {13:         System.out.println("Stage " + id + " constructed");14:     }15: 16:     public static void main(String[] args) {17:         Stage s1 = new Stage("s1");18:         Stage s2 = new Stage("s2");19:     }20: }
```


- ( ) Actor a1 constructed
Actor a2 constructed
Stage s1 constructed
Actor a1 constructed
Stage s2 constructed
- ( ) Actor a2 constructed
Actor a1 constructed
Stage s1 constructed
Actor a2 constructed
Actor a1 constructed
Stage s2 constructed
- ( ) Actor a1 constructed
Actor a2 constructed
Stage s1 constructed
Actor a1 constructed
Actor a2 constructed
Stage s2 constructed
- (x) Actor a2 constructed
Actor a1 constructed
Stage s1 constructed
Actor a1 constructed
Stage s2 constructed

## Explanation

The order of initialization is:
1. static variables (only once)
2. non-static variables
3. constructor.

# Initialization (#13941)
/root/Java & OO Fundamentals/Variables


```
 public static double testInitialization(int i){
  double d;
       if (i >= 
0){
            d = Math.sqrt(i);
       }
  return d;}
```
In this code example the compiler will complain that variable d may not have been initialized. What is the problem?

- ( ) static methods explicitly assign an initialization value
- (x) initialization takes place but is dependent upon the condition of 
i >= 0
- ( ) local variables cannot be initialized at a lower level of curly braces

## Explanation

Since the argument i is being passed into the method as the initializing value, it cannot be conditional. If a negative value of i is passed, then d is not initialized (at the lower level of curly braces) and the return value is unknown.

# String mutability (#1404)
/root/Java & OO Fundamentals/Strings

Which of the following is true about String?

- [ ] String is object-oriented wrapper for array of characters, thus it provides all operations available on char array plus some additional ones for convenience. As an example the following code:
```
char s[] = new char[] {'A', ' ', 'S', 't', 'r', 'i', 'n', 'g'};s[
0] = 'c';
```
can be replaced with object-oriented version:
```
String s = "A String";s.setCharAt(
0, 'c');
```

- [x] String is immutable and if one wants to use a mutable "version" of String they should use a StringBuilder or StringBuffer class instead.
- [ ] To increase performance a String is implemented as a memory-efficient data structure. As a result; the following code does not result in any additional memory allocation.
```
String s = "A String";s.replace("Str", "Tu");
```

- [x] String is thread safe.

## Explanation

Java Strings are immutable (constant) so contrary to "regular" arrays of characters their value (state) cannot be changed. Java String have no such method like 
```
setCharAt
```
. If you wants to use a mutable "version" of String you should use a StringBuilder or StringBuffer class instead.Every potentially mutable operation, like for example 
```
replace
```
 is causing Java to create new array in memory, so in case of the following code 
```
t
```
 is different instance than 
```
s
```
 (i.e. 
```
t!=s
```
).
```
String s = "A String";String t = s.replace("Str", "Tu");
```
Since String is immutable (it's state cannot be changed) it is also thread safe. This is also true for all immutable objects.

# Cat's inheritance (#14151)
/root/Java & OO Fundamentals/Methods

What will be the result of the following piece of code:
```
01: class Cat {02:     private String color = "White";03:     public String getColor() {04:         return this.color;05:     }06: }07: 08: class Persian extends Cat {09:     private String color = "Persian";10:     protected String getColor(){11:         return this.color;12:     }13: }14: 15: public class CatTest {16:     public static void main(String [] args) {17:         Cat cat = new Persian();18:         System.out.println(cat.getColor());19:     }20: }
```


- ( ) White
- ( ) Persian
- ( ) The program will not write anything
- (x) The program will not be compiled

## Explanation

The access modifier of an overriding method must provide at least as much access as the method being overridden. 
Original Method Access Overriding method 
 public public
 protected public or protected
 package package, public or protected

# ++ Operator (#14813)
/root/Java & OO Fundamentals/Operators

Look at the following code:
```
01: public class A {02:     public static void main(String... args) {03:         int a = 
0;04:         if (a++ == a++) {05:             System.out.println("equals");06:         } else {07:             System.out.println("not equals");08:         }09: 10:         if (++a == 
2) {11:             System.out.println("equals 2");12:         } else {13:             System.out.println("not equals 2");14:         }15:     }16: }
```
What will happen if we run it?

- ( ) equals
equals 2
- ( ) equals
not equals 2
- ( ) not equals
equals 2
- (x) not equals
not equals 2
- ( ) Runtime error
- ( ) Compilation error

## Explanation

In the first if statement, 'a' stays 0 in the first operator, and in the second operator as '1' because of the a++ increment. (therefore, 0 == 1)
In the second if statement, 'a' gets incremented during the check, and becomes 3 (after being incremented to 2 after the first if statement).

# String type (#14979)
/root/Java & OO Fundamentals/Strings

A String is a primitive type as int, char, boolean

- ( ) True
- (x) False

## Explanation

A String is a class that implements the interface CharSequence and Comparable.

# Which of the following statements are true? (#15304)
/root/Java & OO Fundamentals/Garbage Collection

Which of the following statements is true?

- (x) You cannot be certain at what point Garbage collection will occur
- ( ) Once an object is unreachable it will be garbage collected
- ( ) Both references and primitives are subject to garbage collection.
- ( ) Garbage collection ensures programs will never run out of memory

## Explanation

You cannot be certain at what point Garbage collection will occur
Once an object is unreachable it will be subject to garbage collection but you cannot be certain it ever will actually be garbage collected. The garbage collection mechanism only applies to objects not primitives. You should be able to guess that garbage collection cannot ensure programs do not run ever run out of memory, but it does ensure that memory no longer required is reallocated to be available.

# String concatenation (#1531)
/root/Java & OO Fundamentals/Strings

String concatenation using "+" operator is forbidden

- ( ) True
- (x) False

## Explanation

You can concatenate strings using "+" operator, e.g.
String str = "str1"+ "str2";
For more details see :
http://docs.oracle.com/javase/6/docs/api/java/lang/String.html

# Variables (#15390)
/root/Java & OO Fundamentals/Variables

Which of the following is correct? Select the correct answer(s).

- [x] The native keyword indicates that the method is implemented in another language like C/C++.
- [ ] The only statements that can appear before an import statement in a Java file are comments.
- [x] The method definitions inside interfaces are public and abstract. They cannot be private or protected.
- [ ] A class constructor may have public or protected keyword before them, nothing else.

## Explanation

b is not correct. A package statement may appear before an import statement.
d is not correct. A class constructor may be declared private also.

# Prefix increment operator (#15475)
/root/Java & OO Fundamentals/Operators

What is the output of the following code?
```
1: public class test {2:     public static void main(String []args){3:         for(int b=
0;b<
12;){4:             System.out.print(++b);5:         }
 6:     }7: }
```


- [ ] 1234567891011
- [ ] 01234567891011
- [x] 123456789101112
- [ ] 0123456789101112
- [ ] 000000000000.....

## Explanation

See the specification for the prefix increment operator:
http://java.sun.com/docs/books/jls/third_edition/html/expressions.html#15.15.1

# Range of primitive type int (#15863)
/root/Java & OO Fundamentals/Variables

What will be the result of 
```
 System.out.println(Integer.MAX_VALUE +
1);
```
 Given that: 
Integer.MAX_VALUE = 2147483647 
Integer.MIN_VALUE = -2147483648?

- ( ) Compile time error: Primitive type 'int' range exceeds.
- ( ) Run time error: Primitive type 'int' range exceeds.
- ( ) 2147483647
- (x) -2147483648
- ( ) 0

## Explanation

If we assign a value to a primitive type grater than its maximum range(Integer.MAX_VALUE = 2147483647) then the value will move to the minimum range(Integer.MIN_VALUE)
For eg: A) Integer.MAX_VALUE (2147483647) + 1 = -2147483648 (Integer.MIN_VALUE). B) Integer.MAX_VALUE (2147483647) + 2 = -2147483647 (Integer.MIN_VALUE + 1) 

# finalize() question (#16076)
/root/Java & OO Fundamentals/Garbage Collection

Calling finalize() on an object will cause it to be garbage collected

- ( ) True
- (x) False

## Explanation

Method finalize() is called by the garbage collector on an object when garbage collection determines that there are no more references to the object.
If finalize() is called explicitly by Java code, if behaves just like any other method.

# Automatic Type Conversion (#16886)
/root/Java & OO Fundamentals/Variables

Given:
```
1: public class TypeConversion {2:     public static void main(String[] args) {3:          char a=
5;4:          short b=-++a;5:          System.out.println(b);6:     }7: }
```
What will be the output ?

- ( ) -4
- ( ) -5
- ( ) -6
- (x) Compiler Error

## Explanation

Line 4 gives a compiler error: 'type mismatch cannot convert from int to short'.
The unary operator (-) causes a conversion to an int type.

# Access Control in Classes (#16921)
/root/Java & OO Fundamentals/Naming

When used in a class declaration, the final keyword means

- ( ) The class will always be a superclass.
- (x) The class can't be subclassed.
- ( ) The class is completed

## Explanation

When used in a class declaration, the final keyword means the class can't be subclassed. In other words, no other class can ever extend (inherit from) a final class, and any attempts to do so will give you a compiler error.

# loop infinitely (#17364)
/root/Java & OO Fundamentals/Flow Control


```
1: public class Main {2:    public static void main(String[] args) {3:       int i = 
0;4:       while( true ){5:          System.out.println(++i);6:       }7:    }8: }
```
Will this statement execute an infinite loop?

- (x) True
- ( ) False

## Explanation

It's legal because there is no expression or condition that leads to jump out of the loop. There is also no "break" statement to jump out neither. So this loop will execute until the program is halted.

# Interface fields (#18834)
/root/Java & OO Fundamentals/Classes and Objects

We have an interface:
```
interface MyWithField {
      String MY_FIELD="Default";}
```
Check correct modifiers of MY_FIELD field:

- [x] public
- [ ] protected
- [ ] private
- [ ] const
- [x] static
- [x] final
- [ ] default

## Explanation

Fields in interfaces are public, static, and final even if those keywords are not explicitely used.

# type var (#18855)
/root/Java & OO Fundamentals/Variables

What is the range of values that can be specified for an int. Select the one correct answer.

- (x) -2^31 to 2^31 - 1
- ( ) The range of values is compiler dependent.
- ( ) -2^31-1 to 2^31
- ( ) -2^15 to 2^15 - 1
- ( ) -2^15-1 to 2^15

## Explanation

In Java, int types are signed numbers of 32 bits, that means the highest number that can be represented is 2^31=2147483647 because the most representative bit sets if the number is positive or negative. Hence, the range of values for an int number is from -2^31 to 2^31 - 1 because one of the numbers in the "positive" range represents the zero.

# Which are valid on line 12? (#18980)
/root/Java & OO Fundamentals/Methods

Which are valid on line 12?
```

11. public interface Status {
12. /* insert code here */ int MY_VALUE = 
10;
13. }
```


- [x] final
- [x] static
- [ ] native
- [x] public
- [ ] private
- [ ] abstract
- [ ] protected

## Explanation

Variables in an interface are implicitly public, static, and final. Those modifiers may be included or omitted. No other modifiers are allowed.

# java data type (#19378)
/root/Java & OO Fundamentals/Variables

Which of the following statements are legal?

- [x] 
```
float i = 
1/
3;
```

- [x] 
```
int i= 
1/
3;
```

- [ ] 
```
float f = 
1.01;
```

- [x] 
```
double d =
999d;
```


## Explanation

default for floating point data type in java is double. if you define data type as a double, you don't have to put d explicitly, but if you define float, you must put f behind the value.

# Constructors (#19521)
/root/Java & OO Fundamentals/Classes and Objects

Which of the following sentences are true about Java object's constructors ?

- [x] Constructors never have an explicit return type.
- [x] Constructors are always executed by the same thread.
- [x] Constructors cannot be directly invoked (the keyword “new�? must be used).
- [x] Constructors cannot be synchronized.
- [ ] Constructors can be final.
- [x] Constructors cannot be abstract.

## Explanation

Constructor takes only access modifier such as public protected private or NONE hence cannot be final.

# Note the Java code below: (#20101)
/root/Java & OO Fundamentals/Operators


```
01: public class Decrement {02:   public static void main (String[] args)03:   {04:      int m, n = 
44;05:      m = --n;06:      m = n--;07:      System.out.println (m);08:      System.out.println (n);09:   }10: }
```
Running this code gives the following output:

- ( ) 42
41
- ( ) 42
42
- ( ) 42
43
- (x) 43
42
- ( ) 43
43

## Explanation

Here, n is initialized with 44.
With "m = --n;", n is pre-decremented to 43 and m is set to 43.
With "m = n--;", m is set to 43 and n is post-decremented to 42.

# What If?? (#2047)
/root/Java & OO Fundamentals/Flow Control

What will be printed in this? Take your time with this.
```
01: 02:         int x=
0;03:         if(x>=
0)04:             x++;05:         if(x<x)06:             x--;07:         if(x>
0){08:             x++;09:             if(x==
3)10:                 System.out.println(x);11:             else12:                 System.out.println(x);13:         }else if(x==
0){14:             System.out.println(x);15:         }else{16:             System.out.println(x);17:         }18: 19:         System.out.println(x);
```


- ( ) 1
2
- ( ) 3
2
- ( ) 1
- (x) 2
2
- ( ) 3
- ( ) 2

## Explanation

Ok this can be a little tricky as there are a few if statements here, but I would reccommend to first create a tracetable, follow the code line by line filling it the value of X for each line. Also note down when the program outputs. 
Here is the result for each IF/ELSE IF statement
2: TRUE
4: FALSE
6: TRUE
8: FALSE
12: Never Reached

# Inheritance: What is the result? (#21218)
/root/Java & OO Fundamentals/Scope

What is the output of the following code?
```
01: class Bird {02:     protected void talk() {System.out.print("chirp ");}03: }04: 05: public class Swallow extends Bird {06:     public static void main (String[] args) {07:         Bird[] birds = { new Bird(), new Swallow()};08:         for (Bird b: birds) {09:             b.talk();10:         }11:     }12: 13:     void talk() {System.out.print("hello");}14: }
```


- ( ) chirp chirp
- ( ) chirp hello 
- ( ) hello hello
- ( ) hello chirp
- (x) Compilation fails
- ( ) An exception is thrown at runtime

## Explanation

Compilation will fail. The overriding 
```
talk()
```
 method has a weaker access modifier.

# Result of the if ..else weather true or false (#21347)
/root/Java & OO Fundamentals/Flow Control


```
 static int i;static int k = ++i;public static void main(String[] args) {
  if (k>
0) {
      System.out.print("True");
  } else {
      System.out.println("False");
  }}
```


- (x) 
```
output : True
```

- ( ) 
```
output : False
```

- ( ) An error will happen at runtime

## Explanation

The result is :
True because all static primitives are initialy assigned to their default.
And in that case, default for type int is 0, and i equals 0 at launch.
Then the pre-increment value ++i reinitialize k to 1.
so the K value is 1, and the condition is true.

# String (#21747)
/root/Java & OO Fundamentals/Strings

The contents of a String object can change at any time at runtime

- ( ) True
- (x) False

## Explanation

A String can not be modified after being created. To change this, you must make a new assignment as:
```
1: str = str.concat ("changed");
```


# Default values (#21893)
/root/Java & OO Fundamentals/Variables

What is the result when calling showValues() ?
```
1: class Vars {2:     String a;3:     int b;4:     float c;5:     6:     public void showValues() {7:         System.out.println(a+" "+b+" "+c);8:     }9: }
```


- ( )  0 0.0
- ( )  0 0
- ( ) Runtime error
- ( ) null 0 0
- (x) null 0 0.0
- ( ) null null null

## Explanation

http://www.janeg.ca/scjp/lang/defaults.html

# Operators Precedence. (#2197)
/root/Java & OO Fundamentals/Operators

 What is the value of h after you execute the sample code?
```
int f = 
2;int g = 
5;int h;h = 
3+f/g+
2;
```


- ( ) 2
- ( ) 3
- (x) 5
- ( ) 5.2
- ( ) 6

## Explanation

Division opearator has more precedence compared to addition. So f/g is executed first which gives 0.Then 3+0+2 is executed giving 5.

# JavaDoc tags (#22110)
/root/Java & OO Fundamentals/Javadoc

Choose all valid JavaDoc tags.

- [x] @author
- [x] @return
- [ ] @Author
- [x] @version
- [ ] @Deprecated
- [ ] @extends

## Explanation

http://en.wikipedia.org/wiki/Javadoc

# Can you extend String? (#22485)
/root/Java & OO Fundamentals/Strings

Can you extend String?

- ( ) Yes
- (x) No

## Explanation

Since String is a final class, it cannot be extended.

# Method Structure Validation (#22730)
/root/Java & OO Fundamentals/Classes and Objects

What is the result of compiling the following code?
```
1: 2:  public class MyClass {3:      4:      public void static main(String [] args){
}5:    }
```


- [ ] Will compile and run.
- [ ] Compilation error in line 1
- [x] Compilation error in line 3
- [ ] Compilation error in line 4

## Explanation

`The correct method declaration is : public static void main (String[] args) {}`

# Local variable (#22928)
/root/Java & OO Fundamentals/Classes and Objects

Local variables can not be declared static or transient.

- (x) True
- ( ) False

## Explanation

Only final modifier for local variable is permitted.

# final modifier (#23007)
/root/Java & OO Fundamentals/Variables

final is the only modifier available to local variables

- ( ) True
- (x) False

## Explanation

clear enough

# Compare two String (#23024)
/root/Java & OO Fundamentals/Strings


```
1: String a = "a";2: String b = new String("a");3: System.out.println(a==b);
```
The output of the above code is true

- ( ) True
- (x) False

## Explanation

There are two method for testing equality, "==" and "equals(object)", "equals(object)" will return true/equal if two object have same content but operator "==" will return true/equals if both of object have same references and same content.

# apparently overriding final method (#23406)
/root/Java & OO Fundamentals/Classes and Objects

Given the following code, what will be the output?
```
01:  02: class Fruit{03:     int size=
9;04: 05:     private final int getSize(){06:         return size;07:     }08: }09: 10: public class Pear extends Fruit{11:     int size=
8;12: 13:     public final int getSize(){14:         return size;15:     }16: 17:     public static void main(String [] smth){18:         System.out.println(new Pear().getSize());19:     }20: }
```


- ( ) 9
- (x) 8
- ( ) RuntimeException
- ( ) The code will not compile since final methods can't be overridden

## Explanation

The code will perfectly compile and output 8. First answer is incorrect since size is referring to the instance variable 'size'. To output the parent's instance variable 'size' the statement must be changed to 'return super.size;'. There is no RuntimeException that could occur in that code. Final methods indeed can't be overriden but since the parent's getSize method is private the Pear object isn't even aware of it and can create its own final getSize method.

# Java Platform Terms (#2351)
/root/Java & OO Fundamentals/Platform

It is composed by Java Virtual Machine and Java Class Libraries...

- ( ) Java Development Kit
- (x) Java Runtime Environment
- ( ) Java Virtual Machine
- ( ) Java Programming Language

## Explanation

Java Runtime Environment is composed only by JVM and the Java class Libraries that would be necessary for executing Java Programs. 

# Method Parameters (#23994)
/root/Java & OO Fundamentals/Methods

What is the output of the following code:
```

1. public class Test {
2.
int x = 
0;
3.
public static void main(String[] args) {
4.
    Test t = new Test();
5.
    String str = "string1";
6.
    t.method(str, t);
7.
    System.out.println(str+" "+t.x);
8.
}
9.
public void method(String str, Test t){
10.
   str = "string2";
11.
   t.x = 
6;
12. }
13. 
14. }
```


- ( ) Compilation fails
- ( ) string2 6
- (x) string1 6
- ( ) string1 0

## Explanation

Variables in Java are passed as a copy of the reference, for the string only the str copy passed is changes to reference another string "string2" while for the test object the object that is referenced by it is changed.

# Not Primitive (#24820)
/root/Java & OO Fundamentals/Strings

Which of the following types are not primitives in Java?

- [x] Object
- [ ] int
- [x] Integer
- [ ] byte
- [x] Boolean
- [x] String
- [ ] char
- [x] Float

## Explanation

The following type are primitives in java: byte, short, int, long, float, double, boolean and char.
Integer, Float and Boolean are object wrappers over primitive types.
String and Object and not primitive types.

# By value (#25320)
/root/Java & OO Fundamentals/References

What is the result?
```
01: class Person {02:     private String name;03:     04:     public void setName(String name) {05:         this.name = name;06:     }07:     public String getName() {08:         return this.name;09:     }10: }11: 12: public class Refs {13:     public void change(Person p) {14:         p = new Person();15:         p.setName("Mike");16:     }17:     18:     public static void main(String[] args) {19:         Refs r = new Refs();20:         Person p = new Person();21:         p.setName("John");22:         r.change(p);23:         System.out.println(p.getName());24:     }25: }
```


- ( ) Mike
- ( ) Compilation error
- ( ) Runtime error
- (x) John

## Explanation

We are passing an object reference by value, which is pointing to the same object instance, but inside change method we create a new reference so the p is pointing to another object.

# finalize method (#25328)
/root/Java & OO Fundamentals/Garbage Collection

Can finalize method be overloaded?

- (x) True
- ( ) False

## Explanation

Yes but only the following version is called by garbage collector:
protected void finalize() throws Throwable { };

# finalize method (#25331)
/root/Java & OO Fundamentals/Garbage Collection

If there is an exception in finalize method, will the object be garbage collected?

- (x) True
- ( ) False

## Explanation

Exception in finalize method doesn't prevent GC.

# String in a method (#25683)
/root/Java & OO Fundamentals/Strings

What is the output of the following code?
```
01: public class Test {02:     03:     String createNewString(String oldString)04:     {05:         String newString = "".toString();06:         newString.concat("Hello ");07:         newString+=oldString;08:         return newString;09:     }10:     11:       public static void main(String[] args) { 12:           13:           Test test = new Test();14:           String s;15:           s="world!";16:           s=test.createNewString(s);17:           System.out.println(s);18:  } 19:   }
```


- ( ) Hello world!
- ( ) Hello
- (x) world!
- ( ) world!world!
- ( ) ""
- ( ) Compile time error
- ( ) Runtime error

## Explanation

String is not mutable. The method concat does not change the value of String newString.
Reference:
http://download.oracle.com/javase/6/docs/api/java/lang/String.html

# Variable (#2629)
/root/Java & OO Fundamentals/Variables

What is the output of this code ?
```
1: //in a class A2: 
   private int number2 = 
5;3: 4:      public int getNumber2() {5:           return this.number2;6:      }
```

```
01: //in an other class02: 
   public static void main(String[] args) {03:           A a;04:           int myNumber = 
0;05:            if(myNumber != a.getNumber2())06:            {07:                  a = new A();08:                  myNumber = a.getNumber2();09:             }10:            System.out.println("My number : " + number);11:      }
```


- ( ) My number : 5
- ( ) My number : 0
- ( ) Runtime exception
- (x) Will not compile

## Explanation

The variable "a" is not initialized before use it in the if block.

# Entry point (#26488)
/root/Java & OO Fundamentals/Classes and Objects

Suppose that you declare the main method in your class as you would normally do, but you add the final modifier to the method header. The result of running this program (comprising of this sole class with only one method - main) is:

- ( ) Compile error
- ( ) Runtime exception
- (x) Runs fine

## Explanation

`In this case, adding the final modifier to main method definition is superfluous. If there was a class hierarchy and main was to be overriden in a subclass, it would matter in which class the main was defined as final`

# What is the result of the next code sample? (#26674)
/root/Java & OO Fundamentals/Methods


```
01: public class Test { 02:     private String name; 03:     04:     Test(String name) { 05:           this.name = name; 06:      } 07:     08:     public String toString(){09:         return this.name;10:     }11:     public static void main(String[] args) { 12:         Test t1 =
new Test("BLA");13:         14:         System.out.println(t1.toString());15:         this.name ="ttt";16:         System.out.println(t1.toString());17:     }
 18: 19: }
```


- ( ) BLA
ttt
- ( ) BLA
- (x) Compilation error

## Explanation

Referring to the this reference in a static method is a syntax error

# if then... what? (#27288)
/root/Java & OO Fundamentals/Flow Control

Given the following code, what will be the output?
```
01: public static void main(String[] args) {02: 03:     int number = 
5;04:         05:     if (number < 
5);06:         System.out.println("smaller than 5");07:     if (number > 
5);08:         System.out.println("bigger than 5");09:     if (number == 
5);10:         System.out.println("exactly 5");11: }
```


- ( ) This code will not compile!
- ( ) exactly 5
- ( ) The program will run but not give any output!
- ( ) smaller than 5
- (x) smaller than 5
bigger than 5
exactly 5
- ( ) bigger than 5
- ( ) The program will raise an exception!

## Explanation

Please notice the semicolon at the end of the if statement! Due to this tiny mistake the code is handled like a command and the execution continues.

# String and array (#27334)
/root/Java & OO Fundamentals/Strings

What happens when you compile and run the following code?
```
1: String [] str = new String[
5];2: str [
0]="1";3: str [
1]="2";4: str [
2]="3";5: for(int i=
0; str[i]!=""; i++)6:    System.out.print(str[i]);
```


- ( ) 123
- ( ) The code does not compile
- ( ) Compiled but does not run
- (x) Compiles and runs but throws an exception

## Explanation

In the for loop, instead of "" must be null, in order to run without any problem and not throw the exception.

# modifiers for constructor (#27375)
/root/Java & OO Fundamentals/Classes and Objects

Which of the following options are valid modifiers for a constructor?

- [x] public
- [ ] static
- [x] private
- [x] protected
- [ ] final
- [ ] abstract

## Explanation

A constructor can never be static, final or abstract. However its visibility can be modified by default, public, private or protected access modifiers.

# Platform dependency in java (#28076)
/root/Java & OO Fundamentals/Platform

Is the JVM platform dependent?

- (x) True
- ( ) False

## Explanation

The JVM is platform dependent. Java code is independent because of byte code generated.

# Using ++v and v++ operator (#28355)
/root/Java & OO Fundamentals/Operators

What is printed after running this code?
```
int a = 
3;int b = 
5;System.out.println( (a++) * (++b));
```


- [x] 18

## Explanation

This prints 18.
Operator a++ "returns" 3 (it "returns" value before incrementing), operator ++b "returns" 6 (it returns value after incrementing). So, (a++) * (++b) = 3 * 6 = 18.

# what will be the output? (#28920)
/root/Java & OO Fundamentals/Classes and Objects

What is the result of compiling and running the following code?
```
01: public class Java02: {03:       public Java j;04:       public Java()05:       {06:           j=new Java();07:       }08:       public static void main(String args[])09:      {10:            Java J=new Java();11:            System.out.println("Object Created");12:      }13: }
```


- ( ) Object Created
- ( ) Compilation Error
- ( ) Compiles and executes successfully
- (x) StackOverflowError

## Explanation

It will create Objects until stack becomes full and it will throw StackOverflowError

# Is it true? (#29535)
/root/Java & OO Fundamentals/Classes and Objects

A source file may contain an unlimited number of non-public class definitions. 

- (x) True
- ( ) False

## Explanation

True. A source file may contain an unlimited number of non-public class definitions. In fact, the source file may contain one public class definition and an unlimited number of non-public class definitions. However, the rules change if two or more of the classes are declared to be public. 

# String (#29556)
/root/Java & OO Fundamentals/Strings

This code is inside a valid main method, what is the result ?
```
1:  String<String> animal01 = new String<String>("Jaguar");2:  String animal02 = "Jaguar";3:  System.out.println(animal01 == animal02);
```


- (x) Compilation fails.
- ( ) Run time exception.
- ( ) Will print true.
- ( ) Will print false.

## Explanation

`There is nothing like String<String> in Java.`

# modifiers (#29741)
/root/Java & OO Fundamentals/Encapsulation

Select correct statements.
```
01: public class MyClass {02: 03:     public static void main(String args[]) {04:         05:         YourClass yourClass = new YourClass();06:         yourClass.a = 
1;07:         yourClass.b = 
2;08:         yourClass.c = 
3;09:         yourClass.d = 
4;10:         11:         System.out.println(yourClass.toString());12:     }13: }14: 15: class YourClass {16:     public int a;17:     protected int b;18:     private int c;19:     int d;20: 21:     @Override22:     public String toString() {23:         String ret = "";24:         ret += "a:" + a;25:         ret += ", b:" + b;26:         ret += ", c:" + c;27:         ret += ", d:" + d;28:         29:         return ret;30:     }
  31: }
```


- [ ] This code compile.
The output is "a:1, b:2, c:3, d:4"
- [ ] This code don't compile because the line 6 is in error.
You must use a getter.
- [ ] This code don't compile because the line 7 is in error.
Protected attributes are not visible here.
- [x] This code don't compile because the line 8 is in error.
Private attributes are not visible here.
- [ ] This code don't compile because the line 9 is in error.
You must use a getter.
- [ ] This code don't compile because the line 9 is in error.
Protected attributes are not visible here.
- [ ] This code don't compile because the line 9 is in error.
Private attributes are not visible here.
- [ ] This code don't compile because the line 11 is in error.

## Explanation



# What is the output of the code? (#31612)
/root/Java & OO Fundamentals/Strings

What is the output of this code?
```
1: String str1 = "Hello World";2: String str2 = new String("Welcome!");3: str1.toUpperCase();4: System.out.println(str1);5: System.out.println(str1.concat(str2));
```


- ( ) HELLO WORLD
Welcome!
- ( ) HELLO WORLD
WELCOME!
- (x) Hello World
Hello WorldWelcome!
- ( ) Hello World
Welcome!
- ( ) Hello World
WELCOME!

## Explanation

The method toUpperCase () has no effect on the str1, because it is not assigned to any variable. In the second printing texts are concatenated str1 and str2.

# How many naming mistakes are in this code? (#31713)
/root/Java & OO Fundamentals/Naming

How many naming mistakes are in this code?
```
package DoNotTryThisAtHome;public class nobodyKnows {
  private int Nevermind;
      public int GetNvm(){
      ... some code    }}
```


- ( ) 0
- ( ) 1
- ( ) 2
- ( ) 3
- (x) 4
- ( ) 5
- ( ) 6

## Explanation

 DoNotTryThisAtHome : 
 keywords and packages: lower case
 nobodyKnows : 
 classes: CaMeL case, begin with a capital
Nevermind, GetNvm: 
 methods and variables (including static): caMeL case, begin with a lower case. 

# JRE and JDK difference (#31951)
/root/Java & OO Fundamentals/Platform

If you want to be able to run java byte code you need (at least) ...

- (x) to have a JRE
- ( ) to have a JDK
- ( ) Both
- ( ) None of both

## Explanation



# What is the output for the below code ? (#31972)
/root/Java & OO Fundamentals/Scope

What is the output for the below code ?
```
01: class Outer {02:     private int a = 
7;03:        04:     class Inner {05:         public void displayValue() {06:             System.out.println("Value of a is " + a);07:         }08:     }09: }10: 11: public class Test {12:     public static void main(String... args) throws Exception {13:         Outer mo = new Outer();
   14:         Outer.Inner inner = mo.new Inner();15:         inner.displayValue();16:     }17: }
```


- ( ) Value of a is 7
- ( ) Compile Error - not able to access private member.
- ( ) Runtime Exception
- ( ) Value of a is null
- (x) java.lang.NoSuchMethodError: main
Exception in thread "main" Java Result: 1

## Explanation

An inner class instance can never stand alone without a direct relationship to an instance of the outer class. You can access the inner class is through a live instance of the outer class. Inner class can access private member of the outer class.

# Garbage collection (#32002)
/root/Java & OO Fundamentals/Garbage Collection

Calling System.gc() ensures that the Java Virtual Machine reclaims all memory that is occupied by unused objects.

- ( ) True
- (x) False

## Explanation

No, in the java doc for the system class you can read "Calling the gc method suggests that the Java Virtual Machine expend effort toward recycling unused objects in order to make the memory they currently occupy available for quick reuse. When control returns from the method call, the Java Virtual Machine has made a best effort to reclaim space from all discarded objects."
This means that it is not guaranteed to free up the memory occupied by unused objects.

# Read clone() JavaDoc (#32046)
/root/Java & OO Fundamentals/Methods

Which of the following statements about clone() method of java.lang.Object are correct? (hint: use JavaDoc)

- [x] All arrays are considered to implement the interface Cloneable.
- [ ] The class Object implements the interface Cloneable.
- [x] If a class does not implement the interface Cloneable, then a CloneNotSupportedException is thrown on clone() call.
- [ ] By convention, changes to the object returned by this method should impact the object, which is being cloned.
- [ ] If a class contains references to immutable objects, then it is usually the case that those fields in the object returned by super.clone need to be modified.
- [x] If a class contains only primitive fields then it is usually the case that no fields in the object returned by super.clone need to be modified.

## Explanation

1,3 and 6 are correct
Navigate through the Jave SE JavaDoc to find this information
http://java.sun.com/javase/6/docs/api/java/lang/Object.html#clone()

# Object creation in Strings (#32607)
/root/Java & OO Fundamentals/Strings

How many object does this code create?
```
String s = new String("Benfica");
```


- ( ) 0
- ( ) 1
- (x) 2
- ( ) 3

## Explanation

"Benfica" creates one object in String pool and "new String" creates another object in the heap.

# Garbage collection (#32933)
/root/Java & OO Fundamentals/Garbage Collection

How can you ensure that the memory allocated by an object is freed.

- ( ) By invoking the free method on the object
- ( ) By calling system.gc() method
- ( ) By setting all references to the object to new values (say null).
- (x) Garbage collection cannot be forced. The programmer cannot force the JVM to free the memory used by an object.

## Explanation



# Abstract your knowlege (#33088)
/root/Java & OO Fundamentals/Classes and Objects

Is it legal to write 
```
public abstract interface AbsrtractInterface {}
```


- (x) True
- ( ) False

## Explanation

it is redundant to declare an Interface with the keyword abstract but it is legal

# Prohibited package name (#3402354)
/root/Java & OO Fundamentals/Packages


```
01: package java.lang;02: 03: public class StringUtils {04:    public static void main(String[] args) {05:       System.out.println(concat("Hello", "World"));06:    }07:    public static String concat(String s1, String s2) {08:       return s1 + " " + s2;09:    }10: }
```
Does this code run properly and print out "Hello World"?

- ( ) Yes
- (x) No

## Explanation

This code compiles properly even if we put the class in the "java.lang" package.
However, it will not run properly: the JVM will throw the runtime exception: "java.lang.SecurityException: Prohibited package name: java.lang"
It is explained in <a href="http://docs.oracle.com/javase/7/docs/api/java/lang/ClassLoader.html#defineClass%28java.lang.String,%20byte%5B%5D,%20int,%20int%29">defineClass method of ClassLoader class</a>

# String declaration (#3402967)
/root/Java & OO Fundamentals/Strings


```
String str="string";
```
Always creates a new object in the heap.

- ( ) true
- (x) false

## Explanation

This code crates a new object in the heap only if the String pool doesn't have a reference to a String "string". 
http://www.javaranch.com/journal/200409/ScjpTipLine-StringsLiterally.html

# Correct Statements (#3402987)
/root/Java & OO Fundamentals/Classes and Objects

Which of the following statements are true?

- [ ] private keyword can never be applied to a class.
- [x] synchronized keyword can never be applied to a class.
- [ ] synchronized keyword may be applied to a non-primitive variable.
- [ ] final keyword can never be applied to a class.
- [x] A final variable can be shadowed in a subclass.

## Explanation

1. private keyword can be used for hide nested class.
2. synchronized keyword can be used for methods only.
3. final keyword when applied to a class means the class cannot be subclassed, when applied to a method means the method cannot be overridden (it can be overloaded though) and when applied to a variable means that the variable is a constant.

#  (#3402988)
/root/Java & OO Fundamentals/Variables

What will be the output of the following code ?
```
public class Sample {
  int[] ia = new int[
1];
  Object oA[] = new Object[
1];
  boolean bool;
  public static void main(String args[]) {
      Sample t = new Sample();
      System.out.println(t.ia[
0] + "  " + t.oA[
0] + "  " + t.bool);
  }}
```


- ( ) The program will fail to compile, because of uninitialized variable 'bool'.
- ( ) The program will throw a java.lang.NullPointerException when run.
- (x) The program will print "0 null false".
- ( ) The program will print "0 null true".

## Explanation

Instance variables are always initialized implicitly if no value is provided explicitly.
Following are the default values that instance variables are initialized with if not initialized explicitly:
Primitive types (byte, short, char, int, long, float, double) to 0 ( or 0.0 ).
All Object types to null.
boolean to false.
Local variables are slightly different; the compiler never assigns a default value to an uninitialized local variable. Is explained in <a href="http://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html">Primitive Data Types</a>

# Access Control (#3402990)
/root/Java & OO Fundamentals/Scope

How should I declare 'i' so that it is not visible outside the package 'test' even not to subclasses, but visible in this package.
```
package test;class Test {
  [modifier] int i;
  /* lot of code */}
```


- ( ) friend
- ( ) public
- ( ) protected
- (x) No access modifier

## Explanation

No Modifier and the protected modifier restrict the visiblility of the variable to the package (excluding subclassing). The protected modifier allows additionally to no modifier that the variable can be seen in all subclasses of Test even when these are outside the package test.

# Scope (#3402991)
/root/Java & OO Fundamentals/Scope

For object o1 of class A to access a member(field or method) of object o2 of class B, when the member has no access modifier, class B must be...

- ( ) a Subclass of A
- (x) in the same package as A is in.
- ( ) a Super class of A
- ( ) a subclass but may not be in the same package.

## Explanation

No access modifier means "default" access which means only classes of the same package can access it.
Note: that there is no 'default' access specifier. Putting no keyword is default access.

# Scope Test (#3402992)
/root/Java & OO Fundamentals/Methods

Consider the following classes...
```
class Teacher {
  void teach(String student) {
      /* lots of code */
  }}class Professor extends Teacher {
  // Line 1}
```
Which of the following methods can be inserted at line // Line 1 ?

- [x] public void teach() throws Exception
- [x] private void teach(int i) throws Exception
- [x] protected void teach(String s)
- [x] public final void teach(String s)
- [ ] public abstract void teach(String s)

## Explanation

Note  : that 'protected' is less restrictive than default 'no modifier'. So choice 3 is valid.
```
public abstract void teach(String s)
```
 would have been valid if class Professor had been declared abstract.

# int range (#3403063)
/root/Java & OO Fundamentals/Variables

Given the following variables:
```
int i = Integer.MAX_VALUE;
      int j = i + 
1;
```
Select true options after execution:

- [x] i > 0
- [ ] j > 0
- [ ] an ArithmeticException is thrown

## Explanation

Integer.MAX_VALUE + 1 produces overflow in int range, and gives a negative value.

# Interface naming convention (#3403152)
/root/Java & OO Fundamentals/Naming

According to the Java naming convention rules, the interface name must always be an adjective e.g. Serializable, Clonable, Comparable, Throwable and so on...

- ( ) true
- (x) false

## Explanation

The Java naming convention rules say that the interface names should be capitalized like class names (e.g. interface Sorting). The interface name might but does not have to be and adjective. Also, the Throwable is a class and not interface.
The naming convention rules:
http://www.oracle.com/technetwork/java/codeconventions-150003.pdf

# Parameterized constructor and default constructor (#3403156)
/root/Java & OO Fundamentals/Classes and Objects

With the following class :
```
01: public class Foo {02: 03:     private int x;04:     private int y;05: 06:     public Foo(int x, int y) {07:         this.x = x;08:         this.y = y;09:     }10: 11:     public int getX() {12:         return x;13:     }14: 15:     public void setX(int x) {16:         this.x = x;17:     }18: 19:     public int getY() {20:         return y;21:     }22: 23:     public void setY(int y) {24:         this.y = y;25:     }26: 27:     public String toString() {28:         return "Foo : " + x + ", " + y;29:     }30: 31:     public static void main(String[] args) {32:         Foo foo = new Foo();33:         foo.setX(
1);34:         foo.setY(
2);35:         36:         System.out.println(foo);37:     }38: }
```
What will be the output ?

- (x) This code doesn't compile
- ( ) An exception will occurs
- ( ) Foo : 1, 2
- ( ) Foo : 2, 1
- ( ) Foo : 0, 0

## Explanation

The default constructor is not accessible if there is a parameterized one.

# Visibility (#3403158)
/root/Java & OO Fundamentals/Scope

Which of the following are visibilities in Java?

- [x] private visibility
- [x] protected visibility
- [x] public visibility
- [x] default visibility
- [ ] volatile visibility
- [ ] global visibility

## Explanation

4 visibilities exists in Java.
The volatile keyword is related to synchronization.
The global visibility doesn't exists.

# Parameters are passed by value (#3403216)
/root/Java & OO Fundamentals/Methods

What is the output for this class :
```
public class Test {
  public static void main(String[] args) {
      int i = 
10;
      System.out.println("i=" + i);
      add(i, 
5);
      System.out.println("i=" + i);
      i = i + 
5;
      System.out.println("i=" + i);
  }
  private static void add(int i, int j) {
      i = i + j;
  }}
```


- ( ) i=10
i=15
i=20
- ( ) i=0
i=5
i=10
- (x) i=10
i=10
i=15
- ( ) i=10
i=15
i=15
- ( ) i=10
i=10
i=10
- ( ) An exception is caught during the executionThis code will not compile

## Explanation

The initial value (10) is set in the déclaration of the variable "i".
the parameter called "i" is passed by value (the value is copied into the stack) to the "add" method.
Therefore, the variable "i" has the same value (10) after calling the method "add".
But the variable "i" is set to 15 after the addition assignment.

# String compare (#3403307)
/root/Java & OO Fundamentals/Strings

For comparing strings, we have to use equals() method instead of "=="?

- (x) True
- ( ) False

## Explanation

String is class in Java inherited from Object, and equals() method is method from Object class which is overridden in String class. If you try to compare String objects with "==" you will compare just references, not a real objects. Method equals(...) compare content of String object instead of link to the object (what "==" do).

# Developer Environment (#3403334)
/root/Java & OO Fundamentals/Platform

What do you need to be installed for compile java source code to java byte code?

- (x) JDK
- ( ) JRE
- ( ) JVM

## Explanation

JDK (Java Development Kit) contains compiler javac, which can be used for compile source code.
JRE (Java Runtime Environment) contains libraries and JVM and do not contains compiler javac.
JVM (Java Virtual Machine) executes your java byte code.

# Array questions (#3403524)
/root/Java & OO Fundamentals/Classes and Objects

Check correct answers about arrays

- [ ] Brackets can be only to the right of the variable name when you declare an array
- [x] Arrays can hold primitives or objects
- [ ] Size of an array can be include in the declaration
- [x] Any object that passes the IS-A or instanceof test for the declared type of the array you can add to an array

## Explanation

Brackets can be to the left or right of the variable name when you declare an array.
Yes. Arrays can hold primitives or objects.
If you declare an array you CAN'T include array size. You should set it in definition.
It's true that object that passes the IS-A test can be add to the array declared of that objects.

# Class modifiers (#3403526)
/root/Java & OO Fundamentals/Classes and Objects

Check correct answers

- [ ] Final class can be subclasses
- [x] Abstract class can't be instantiated
- [x] If class include one abstract method then whole class must be abstract
- [ ] Class can't be modified with final

## Explanation

If you set final for the class all is over. Then you can't extend this class. 
It's true that class can be modified as final. 
What you can obtain if you want instantie abstract class? Total absurd, of course illegal. 
Class must be abstract if only one method is abstract.

# Switch statement (#3403533)
/root/Java & OO Fundamentals/Flow Control

Check correct answers:
Switch statements can evaluate to:

- [x] enums
- [ ] long
- [ ] double
- [x] int

## Explanation

Switch statements can evaluate only to:
 - enums
 - byte
 - short
 - int
 - char

# Default keyword in switch statement (#3403534)
/root/Java & OO Fundamentals/Flow Control

Default keyword can be placed anywhere in switch block.
True or false?

- ( ) False
- (x) True

## Explanation

Default case does not necessarily have to be the last case in a Switch block. This example would work:
switch (x) {
 case 0: 
 doSomething0();
 break;
 case 1: 
 doSomething1();
 break;
 default: 
 doSomethingElse();
 break;
 case 2: 
 doSomething2();
 break;
 case 3: 
 doSomething3();
}

# Garbage Collection (#3403535)
/root/Java & OO Fundamentals/Garbage Collection

Check the correct answers

- [ ] Garbage Collection can be manualy run
- [ ] The purpose of Garbage Collection is the acceleration of the environment
- [x] Only Java Virtual Machine decides when to run Garbage Collection

## Explanation

GC is automated memory management and the purpose is delete unused objects.

# Fine expression (#3403538)
/root/Java & OO Fundamentals/Operators

What is the result
```
public class Test {
  static int varA=
2;
  public static void main(String [] argv) {
      int varA=
5;
      float varB=
7.5f;
      System.out.println("Result: " + (Test.varA + varB));
  }}
```


- ( ) 12
- (x) 9.5
- ( ) Compilation error
- ( ) 12.5
- ( ) RuntimeException

## Explanation

There's no problem to use static variable and add it to float varB:
2 + 7.5 = 9.5

# Hard expression (#3403539)
/root/Java & OO Fundamentals/Operators

What is the result:
```
public class Test {
  static int varA=
5;
  public static void main(String [] argv) {
      int varA=
3;
      float varB=
2.5;
      System.out.println("Result: " + (varA + varB));
  }}
```


- ( ) 5
- ( ) RuntimeException
- ( ) 7.5
- ( ) 5.5
- (x) Compilation error

## Explanation

Compilation error is the correct answer.
Compilator can't cope with statement float varB=2.5;
Possible loss of precision.

# Exception expression (#3403543)
/root/Java & OO Fundamentals/Flow Control

What is the result
```
public class Test {
  public static void main(String [] argv) {
      String errorComment = null;
      try {
          Integer.parseInt("5,");
      } catch (Exception ex) {
          errorComment = "Exception";
      } catch (NumberFormatException nfEx) {
          errorComment = "NumberFormatException ";
      } finally {
          System.out.println("Result: " + errorComment);
      }
  }}
```


- ( ) Result: Exception
- ( ) Result: NumberFormatException
- (x) Compilation error
- ( ) RuntimeException

## Explanation

Order of catch block must be from most specific to most general.

# Legal Identifiers (#3403547)
/root/Java & OO Fundamentals/Variables

Select the correct statement(s) about defining identifiers:

- [x] After the first character, identifiers can also include digits.
- [x] Identifiers can be of any length.
- [ ] Identifiers must start with a letter, a currency character ($) or a number.
- [x] You can't use a Java keyword as an identifier.

## Explanation

Valid identifiers:
- can start with a letter, underscore or a dollar sign ($). 
- can be of any length,
- can't be a Java keyword.

# Source File Declaration Rules (#3403548)
/root/Java & OO Fundamentals/Packages

Select the correct answers on the package statement.

- [ ] If there isn't a package statement, then the class declaration must be the first line(s) in the source code file
- [x] If the class is part of a package, the package statement must be the first line in the source code file, before any import statements that may be present.
- [x] import and package statements apply to all classes within a source code file
- [x] If there are import statements, they must go between the package statement (if there is one) and the class declaration

## Explanation

Proper and irreplaceable order of statements is:
- package statement (if any),
- import statement(s) (if any),
- class declaration

# Access Modifiers (#3403549)
/root/Java & OO Fundamentals/Classes and Objects

Which from the following are access modifiers:

- [x] public
- [ ] abstract
- [x] private
- [ ] final
- [ ] package

## Explanation

Abstract and final aren´t access modifiers.
- Final: When used in a class declaration, the final keyword means the class can't be subclassed. In other words, no other class can ever extend (inherit from) a final class, and any attempts to do so will give you a compiler error.
- Abstract: An abstract class can never be instantiated.

# Is it true? (#34829)
/root/Java & OO Fundamentals/Platform

Each source file that you compile will always produce exactly one file with an extension .class

- ( ) True
- (x) False

## Explanation

Compilation may produce single class file, but it also may produce multiple class files (in case of internal classes).

# True or false? (#349)
/root/Java & OO Fundamentals/Classes and Objects

A class can extend just one class and implement only one interface.

- ( ) True
- (x) False

## Explanation

extends one class, implements multiple interfaces

# Compiled or interpreted (#35321)
/root/Java & OO Fundamentals/Platform

The java language is:

- [x] Compiled
- [x] Interpreted

## Explanation

The java language is both compiled and interpreted. It is compiled to bytecode (.class) by the javac or IDE compiler and then interpreted by the JVM. In fact, your code can be even compile again to native code by the Just In Time (JIT) compiler.

# Which Java platform should be used ? (#35879)
/root/Java & OO Fundamentals/Platform

Which Java platform contains the specifications for servlets, JavaServer Pages, and JavaServer Faces?

- ( ) Java ME
- ( ) Java SE
- (x) Java EE
- ( ) Java EA

## Explanation

C. The Java EE platform contains the specifications related to dynamic web content
solutions, including servlets, JavaServer Pages, and JavaServer Faces.
A, B, and D are incorrect. A is incorrect because Java ME is the Java Micro Edition used
for embedded solutions. B is incorrect because Java SE is the Java 2 Standard Edition used
for basic application development. D is incorrect because Java EA is fictitious.

# Synchronized (#37133)
/root/Java & OO Fundamentals/Classes and Objects

A class can be declared synchronized.

- ( ) True
- (x) False

## Explanation

Only public and default modifier allowed unless inner classes

# Access modiers (#37136)
/root/Java & OO Fundamentals/Classes and Objects

Which access modifier is more strict ?

- (x) default (no keyword)
- ( ) protected (protected keyword)

## Explanation

See http://java.sun.com/docs/books/tutorial/java/javaOO/accesscontrol.html

# JDK and JRE (#37393)
/root/Java & OO Fundamentals/Platform

Which of the following statements are true?

- [x] The 
```
java
```
 tool is part of JRE
- [ ] The 
```
javac
```
 tool is part of JRE
- [x] The 
```
java
```
 tool is part of JDK
- [x] The 
```
java
```
 tool is used to run Java programs
- [x] The 
```
javac
```
 tool is used to compile Java programs

## Explanation

1 is true: 
```
java
```
 tool is part of Java Runtime Environment2 is false: 
```
javac
```
 tool is not part of Java Runtime Environment, it is part of the Java Development Kit3 is true: The Java Runtime Environment is included in the Java Development Kit
4 is true
5 is true

# Access (#37697)
/root/Java & OO Fundamentals/Methods

Given
```
1: package test;2: 3: class Target {4: public String name = "hello";5: }
```
What can directly access and change the value of the name field?

- ( ) any class
- ( ) only Target class
- (x) any class in the test package
- ( ) any class that extends Target

## Explanation

Although the name field is declared public, the Target class is declared with package access. So the class itself is visible only in the test package.

# what is the result of that? (#37978)
/root/Java & OO Fundamentals/References


```
myclass a = new myclass();myclass b = new myclass();b = a;System.out.println(a == b);
```
What is the output if the above code is run?

- (x) True
- ( ) False
- ( ) Compilation fails

## Explanation

The output is "true". Two instances of the class "myclass" are created, referenced by two different variables. The assignment "b=a" changes the reference of b to point to the same object as a. Thus, the boolean test a==b which tests the references for identity returns true.
Also, the compilation will succeed. The lowercase class names are discouraged by convention but legal to the compiler.

# Table (#38255)
/root/Java & OO Fundamentals/References


```
String[] names = { "kasia", "ania", "ola" };System.out.println(names[id]);
```
 What number should 
```
id
```
 be replaced by in order to generate 
```
ania
```
 as the output?

- ( ) 
```

2 
```

- ( ) 
```

0 
```

- (x) 
```

1 
```


## Explanation



# Varargs (#38308)
/root/Java & OO Fundamentals/Variables

If a method makes use of a variable number of parameters with the varargs notation (Object... name), then the method will require at least one argument when called.
Ex:
```
public void printData (String... dataToBePrinted) {
  // function body ...}
```


- ( ) True
- (x) False

## Explanation

The varargs notation works for any number of objects including 0. Keep in mind that the code inside the method needs to be designed to handle this case.

# Is this a valid java operator? (#38475)
/root/Java & OO Fundamentals/Operators

Is =! a valid java operator?

- ( ) True
- (x) False

## Explanation

There is operator != (called not equal to).
No, there is no operator in Java called =!. The correct operator is !=, which means "not equal to".

# Is it a valid java operator ? (#38515)
/root/Java & OO Fundamentals/Operators

Is => a valid java operator ?

- ( ) True
- (x) False

## Explanation

`There is operator &gt;= (called greater than or equal to).`And there is operator &lt;= (called less than or equal to).`

# Variables (#39692)
/root/Java & OO Fundamentals/Variables

A local variable within a method and the method parameter must have different names.

- (x) True
- ( ) False

## Explanation

They share the scope, so can't have the same name

# Garbage Collection (#39753)
/root/Java & OO Fundamentals/Garbage Collection

How can you force garbage collection?

- ( ) by calling System.gc()
- ( ) System.exit(0);
- (x) You can't force GC, JVM does not gurantee that GC will be started immediately.

## Explanation

You can't force GC, but could request it by calling System.gc(). JVM does not guarantee that GC will be started immediately.

# Access Control (#40690)
/root/Java & OO Fundamentals/Naming

When we say code from one class (class A) has
access to another class (class B), it means class A can do:

- [x] Create an instance of class B.
- [x] Extend class B.
- [x] Access certain methods and variables within class B, depending on the access control of those methods and variables.

## Explanation

When we say code from one class (class A) has access to another class (class B), it means class A can do one of three things:
■ Create an instance of class B.
■ Extend class B (in other words, become a subclass of class B).
■ Access certain methods and variables within class B, depending on the access control of those methods and variables.
In effect, access means visibility. If class A can't see class B, the access level of the methods and variables within class B won't matter; class A won't have any way to access those methods and variables.

# System Class Loader (#40729)
/root/Java & OO Fundamentals/Platform

System class loader loads JDK internal classes from java.* packages.

- ( ) True
- (x) False

## Explanation

System class loader loads classes from system classpath (as defined by the java.class.path property, which
is set by the CLASSPATH environment variable or –classpath or –cp command line
options)

# At what point will the object created.. (#41082)
/root/Java & OO Fundamentals/Garbage Collection

At what point will the object created on line 8 be eligible for garbage collection?
```
01: public class RJMould{02:     StringBuffer sb;03:     public static void main(String argv[]){04:         RJMould rjm = new RJMould();05:         rjm.kansas();06:     }07:     public void kansas(){08:         sb = new StringBuffer("Manchester");09:         StringBuffer sb2 = sb;10:         StringBuffer sb3 = new StringBuffer("Chester");11:         sb=sb3;12:         sb3=null;13:         sb2=null;14:     }15: }
```


- ( ) Line 11
- ( ) Line 9
- ( ) Line 12
- (x) Line 13

## Explanation

Line 13.
On line 9 the object created on line 8 has the reference sb2 pointed to it. Until something happens to make that reference unable to reach the object it will not be eligible for garbage collection.

# Variables (#41148)
/root/Java & OO Fundamentals/Variables

Which of the following lines will compile correctly?

- ( ) 1) 
```
short myshort = 99S; 
```

- ( ) 2) 
```
String name = 'Excellent tutorial Mr Rogerio'; 
```

- ( ) 3) 
```
char c = 
17c; 
```

- (x) 4) 
```
int z = 
015; 
```


## Explanation

"S" and "c" postfixes are not valid:
http://java.sun.com/docs/books/jls/third_edition/html/lexical.html#3.10.2
String value should be enclosed whith double, not single qoutes:
http://java.sun.com/docs/books/jls/third_edition/html/lexical.html#3.10.5

# Flow Control, loops (#41780)
/root/Java & OO Fundamentals/Flow Control

The loop do-while will run at least once.

- (x) True
- ( ) False

## Explanation

`do-while` loop is executed at least once because it makes an action and then verifies.

# Variable not initialized (#43251)
/root/Java & OO Fundamentals/Variables

What is the result ?
```
1: 
  public static void main(String[] args) {2:         int j = 
0;3:         for(int i=
0;i<
50;++i) {4:             System.out.print(i);5:             if(i>
9) break;6:             j = i;7:         }8:         System.out.print(j);9:     }
```


- ( ) Compilation fails
- ( ) Runtime error
- ( ) 012345678910
- ( ) 0123456789
- ( ) 01234567891010
- (x) 0123456789109
- ( ) 01234567899

## Explanation

The loop stop when i equals 10 and j is assigned with i when i equals 9.

# Java language (#43288)
/root/Java & OO Fundamentals/Platform

Java is a...

- ( ) Compiled language
- (x) Just-in-time compiled language
- ( ) Interpreted language
- ( ) None of the above

## Explanation

Compiled Java code can run on most computers because Java interpreters and runtime environments, known as Java Virtual Machines (VMs), exist for most operating systems, including UNIX, the Macintosh OS, and Windows. Bytecode can also be converted directly into machine language instructions by a just-in-time compiler (JIT).

# if and else if (#44084)
/root/Java & OO Fundamentals/Flow Control

You have variable i in code. You are given this two snippets:
snippet 1:
```
if ((i % 
5) == 
0 && (i % 
3) == 
0)
System.out.print("FizzDizz");else if ((i % 
5) == 
0)
System.out.print("Fizz");else if ((i % 
3) == 
0)
System.out.print("Dizz");
         
```
snippet 2:
```
if ((i % 
5) == 
0)
System.out.print("Fizz");if ((i % 
3) == 
0)
System.out.print("Dizz");
```
When we try this two snippets against the same variable i value, will the output be equal?

- (x) True
- ( ) False

## Explanation

Despite second snippet is written better with no excess code, the output will be the same. 

# - Operators (#44333)
/root/Java & OO Fundamentals/Operators

What's the output if you run the code below?
```
1: int a = 
3;2: int b = 
2;3: System.out.println(a/b);
```


- (x) 1
- ( ) 1.5

## Explanation

The code will print an integer result because a and b are both integers.

# Integer class and int type (#45507)
/root/Java & OO Fundamentals/Platform

What will be the output?
```
1:  2: package Course1;3: class OperatorExercise {4:     public static void main(String args[]) {5:         int n = 
0;6:         Integer i = 
0;
         7:         System.out.println(n.compareTo(i));8:     }9: }
```


- ( ) 1
- ( ) 0
- ( ) -1
- (x) does not compile.
- ( ) nullpointerException at Runtime

## Explanation

Remember that the primitive "int" type is not an object, and thus do not have methods.
You can do this:
System.out.println(i.compareTo(n));

# Operator ||. What is the output? (#45792)
/root/Java & OO Fundamentals/Operators

What is the output if you run the following code?
```
1: int i=
0;2: System.out.println((
0== i++ || 
1==i++) + ". Value i="+i );
```


- ( ) Runtime error.
- ( ) Compile error.
- (x) true. Value i=1
- ( ) false. Value i=1
- ( ) true. Value i=2
- ( ) false. Value i=2

## Explanation

Only evaluates 0== i++, but not the expression 1==i++.
As i++ is a post-increment, the comparison is 0 == 0 and then the increment and assignment are executed, so "true. Value i=1" is printed.

# Java Se meaning. (#46120)
/root/Java & OO Fundamentals/Platform

The meaning of Java SE is: 

- ( ) Java Second Edition
- (x) Java Standard Edition
- ( ) Java Student Edition
- ( ) Java Security Edition
- ( ) none of the above.

## Explanation

http://www.oracle.com/technetwork/java/javase/downloads/index.html

# Valid Java variable identifiers (#46213)
/root/Java & OO Fundamentals/Naming

Please choose all valid identifiers in Java (as of Java 5):

- [x] double _x_axis
- [x] int $money
- [ ] Enumeration enum
- [ ] Date 1stSaturdayInMonth
- [x] long number_of_seconds_in_a_year

## Explanation

Identifiers in Java must start with letter, $ sign (or another currency symbol) or underscore (_) (or another "connecting punctuation character"). To check if a character is a valid start for an identifier the method Character.isJavaIdentifierStart() can be used. As of Java 5, enum is a keyword, so only A, B and E are correct.

# Variable Naming (#46309)
/root/Java & OO Fundamentals/Variables

Choose all answers that apply to the following code:
```
1: String #name = "Jane Doe";2: int $age=
24;3: double _height = 
123.5;4: double ~temp = 
37.5;
```


- [x] Line 1 will not compile. 
- [ ] Line 2 will not compile.
- [ ] Line 3 will not compile.
- [x] Line 4 will not compile.

## Explanation

Variable names are case-sensitive. A variable's name can be any legal identifier — an unlimited-length sequence of Unicode letters and digits, beginning with a letter, the dollar sign "$", or the underscore character "_".
http://docs.oracle.com/javase/tutorial/java/nutsandbolts/variables.html

# Constructor (#46657)
/root/Java & OO Fundamentals/Classes and Objects

A constructor cannot have parameters inside.

- ( ) True
- (x) False

## Explanation

One constructor accepts parameters as in the following case:
```
class Constructor {
      Constructor (int i) {
      System.out.println(
      "The " + i + "can have parameters within") ;
      }
  }
```


# gc on demand (#46936)
/root/Java & OO Fundamentals/Garbage Collection

The garbage collector can be 'executed' on demand.

- ( ) True
- (x) False

## Explanation

No. System.gc() is only the suggestion for garbage collector to trash unused objects.

# Is the code correct? (#47109)
/root/Java & OO Fundamentals/Variables

Are both pieces of code correct?
```
1: int x = 
1;2: long y = x;
```

```
1: long x = 
1;2: int y = x;
```


- ( ) True
- (x) False

## Explanation

The long data type can not be assigned to an int variable,
int data type has less capacity than a long

# Keywords vs literals (#47179)
/root/Java & OO Fundamentals/Naming

Which of the following are Java keywords

- [x] 
```
public
```

- [ ] 
```
null
```

- [x] 
```
for
```

- [ ] 
```
false
```

- [x] 
```
class
```


## Explanation


```
true
```
, 
```
false
```
 and 
```
null
```
 are literals not keywords. See: http://java.sun.com/docs/books/tutorial/java/nutsandbolts/_keywords.html

# Packages and directory structure (#47204)
/Java (core)/Java SE - basic/Misc/Files and Packages

We have the following code located in project/src:
```
1: package com.jbb.tests;2: 3: public class Test {4:   int x;5: }
```
After compiling the file using javac -d project/bin /src/Test.java where would we find the compiled code?

- ( ) project/bin/Test.java
- ( ) project/bin/Test.class
- ( ) project/bin/com/jbb/tests/Test.java
- (x) project/bin/com/jbb/tests/Test.class
- ( ) project/bin/com.jbb.tests.Test.java
- ( ) project/bin/com.jbb.tests.Test.class
- ( ) project/src/com/jbb/tests/Test.class
- ( ) project/src/com.jbb.tests.Test.java
- ( ) project/src/com.jbb.tests.Test.class
- ( ) project/src/com/jbb/tests/Test.java

## Explanation

Directory structure is determined by the package name. Directories are created according to packages and sub-packages, and the .class file itself resides in the last package name.

# Given: (#47428)
/root/Java & OO Fundamentals/Variables

Given:
```

1: String #name = "Jane Doe";
2: int $age=
24;
3: double _height = 
123.5;
4: double ~temp = 
37.5;
```
Which two are true? (Choose two.)

- [x] Line 1 will not compile.
- [ ] Line 2 will not compile.
- [ ] Line 3 will not compile.
- [x] Line 4 will not compile.

## Explanation

A variable can start with $ , _ or a letter. A variable can't start with anything else (a variable starting with #, ~ , a number, ... is not valid).

# Wrapper Class (#47488)
/root/Java & OO Fundamentals/Classes and Objects

Which of the following are the wrapper classes?
(A) Random
(B) Byte
(C) Vector
(D) Integer
(E) Short
(F) Double
(G) String

- ( ) D,E & F
- (x) B,D,E & F
- ( ) B,E & F
- ( ) A,B,D,E & F
- ( ) B,D & E

## Explanation



# java identifiers (#47547)
/root/Java & OO Fundamentals/Naming

Which of these are valid java declarations:
```
/* 1 */ int $expensive_variable;/* 2 */ String variable-two;/* 3 */ float 
4give_me;/* 4 */ double _______zzz;
```


- [x] 1
- [ ] 2
- [ ] 3
- [x] 4

## Explanation

Identifier can begin with a letter, an underscore or a currency character and first character it can also include digits.
More details about Java identifier can be found under:
http://java.sun.com/docs/books/jls/third_edition/html/lexical.html#40625

# When does an object become eligible for garbage.. (#48855)
/root/Java & OO Fundamentals/Garbage Collection

When does an object become eligible for garbage collection?

- ( ) It is static object.
- (x) An object becomes eligible for Garbage Collection when no live thread can access it.
- ( ) It already was utilized once
- ( ) The programmer choice which elements will be destroyed

## Explanation

An object becomes eligible for Garbage Collection when no live thread can access it.

# final keyword (#48893)
/root/Java & OO Fundamentals/Classes and Objects

If you add the final keyword to a reference, then the referenced Object becomes immutable.

- ( ) True
- (x) False

## Explanation

It's not the referenced Object that becomes immutable but the reference itself.
final StringBuffer sb = new StringBuffer(); 
sb.append('a'); 
is ok while 
final StringBuffer sb = new StringBuffer(); 
sb = new StringBuffer(); 
does not work.

# Runtime environment for Java programs. (#49205)
/Java (core)/Java SE - basic/Misc/Vocabulary and Concepts

A Java program runs in a platform which is a layer between the program and the operating system.
What is the abbreviated name of this platform?
Hint to avoid ambiguity: ''J?M'' (find the middle letter).
Type the 3 letters abbreviation uppercase with no dots.

- [x] JVM
- [x] V

## Explanation

JVM stands for Java Virtual Machine, which is an important concept to understand when developping in Java. You do not compile your source code to .exe files for your machine, you compile for this virtual machine to a binary format called bytecode.

# Loops (#49345)
/root/Java & OO Fundamentals/Flow Control

What is the value of k after the following code fragment?
```
1: int k = 
0;2: int n = 
12;3: while (k < n)4: {5:    k = k + 
1;6: }
```


- ( ) 0
- ( ) 11
- (x) 12
- ( ) unknown

## Explanation

in Loop while k became 1 after that 2,3, ..... and 12

# How can you compare the following variables? (#50098)
/root/Java & OO Fundamentals/Variables

How can you compare the following variables?
```
Integer oldvar = 
5;int newvar = 
5;
```


- [x] newvar == oldvar
- [x] oldvar == newvar
- [ ] newvar.equals(oldvar)
- [x] oldvar.equals(newvar)

## Explanation

newvar - Primitive Type and do not have any metods.

# Default values for primitive members (#50180)
/root/Java & OO Fundamentals/Variables

In Java when a primitive data type is a member of a class (class variable) is guaranteed to have a default value if not initialized.

- (x) True
- ( ) False

## Explanation

The default values are what Java guarantees when the variable is used
 as a member of a class. This ensures that member variables of primitive types will always be initialized (something that does not occur in C + +), reducing a source of errors. However, this initial value may not be correct or even legal in the particular program in which you are working. It is always better to initialize all variables explicitly
Thinking in Java (Piensa en Java)
Bruce Eckel

# Valid package name (#50482)
/root/Java & OO Fundamentals/Packages

What will be an output of the following code snippet after the class instantiated:
```
1: 2: package java;3: 4: public class Alpha {5: 6:     public Alpha() {7:         System.out.println("It works");8:     }9: }
```


- ( ) Compilation fails
- ( ) It will print:
```
It works
```

- (x) Runtime exception

## Explanation

Exception "java.lang.SecurityException: Prohibited package name: java" is thrown at runtime.

# package (#50499)
/root/Java & OO Fundamentals/Packages

You want subclasses in any package to have access to members of a superclass. Which is the most restrictive access that accomplishes this objective?

- ( ) public
- ( ) private
- (x) protected
- ( ) transient
- ( ) default access

## Explanation



# Shadowing Variable Feature (#50574)
/root/Java & OO Fundamentals/Variables

What is the output after you run the following code snippet? Please select all possible answers.
```
01: public class C {02:     private int int_i = 
10;03:     public int getInt_i() {04:         return int_i;05:     }06:     public C() {07:     }08:     public void f1(int int_i) {09:         int_i = int_i;10:         System.out.println("int_i : "+ int_i);11:     }12:     public static void main(String[] args) {13:         C c = new C();14:         c.f1(
3);15:         System.out.println("int_i : " + c.getInt_i());16:     }17:  }
```


- [ ] int_i : 10
int_i : 10
- [x] int_i : 3
int_i : 10
- [ ] int_i : 3
int_i : 3
- [ ] int_i : 10
int_i : 3

## Explanation

The assignment int_i = int_i; inside method f1() has no effect due to shadowing variable feature. The correct assignment is this.int_i = int_i to avoid such situation.

# The static keyword (#50706)
/root/Java & OO Fundamentals/Variables

You can access a static attribute of a class without creating any object of that class

- (x) True
- ( ) False

## Explanation

Saying that something is static, it indicates that the data or method is not tied to any object instance of that class in particular. So even if you never created an object of that class can invoke a static method or access a piece of static data.
 Thinking in Java (Piensa en Java)
 Bruce Eckel

# garbage collection (#50825)
/root/Java & OO Fundamentals/Garbage Collection

Given:
```
class Snoochy {
 Boochy booch;
 public Snoochy() { booch = new Boochy(this); }}class Boochy {
 Snoochy snooch;
 public Boochy(Snoochy s) { snooch = s; }}
```
And the statements:
```
1: public static void main(String[] args) {2: Snoochy snoog = new Snoochy();3: snoog = null;4: // This is the line for the context of the question5: // More code here6: }
```
Which statement is true about the objects referenced by snoog, snooch, and booch immediately after line 3 executes?

- ( ) None of these objects are eligible for garbage collection.
- ( ) Only the object referenced by booch is eligible for garbage collection.
- ( ) Only the object referenced by snoog is eligible for garbage collection.
- ( ) Only the object referenced by snooch is eligible for garbage collection.
- (x) The objects referenced by snooch and booch are eligible for garbage collection.

## Explanation

snooch and booch are unreferenced objects which are eligible for GC.
Because snooch are set to null and booch was referenced only by snooch.

# Out of scope (#50876)
/root/Java & OO Fundamentals/Scope

What is the result ?
```
1: 
  public static void main(String[] args) {2:         for(int i=
0;i<
12;++i) {3:             System.out.print(i);4:             if(i>
9) break;5:         }6:         System.out.print(i);7:     }
```


- ( ) 0123456789101112
- ( ) 01234567891011
- ( ) 01234567891010
- ( ) 0123456789
- ( ) Runtime Error
- (x) Compilation fails

## Explanation

Compilation fails at line 7 : the variable i is not visible.

# operator ++ (#51160)
/root/Java & OO Fundamentals/Operators

which is the output of the following code
```
01:  02: public class Test {03:     04:     public static void main(String[] args) {05:         int count=
0;06:         System.out.print(count++);07:         System.out.print(++count);08:         System.out.print(count++);09:     }10: }
```


- ( ) 123
- ( ) 012
- (x) 022
- ( ) 113
- ( ) compilation fails

## Explanation

I tried with java 1.6, the answer is 022

# Garbage collector is a daemon thread (#51262)
/root/Java & OO Fundamentals/Garbage Collection

Garbage collector is a daemon thread.

- (x) True
- ( ) False

## Explanation

Yes, GC is a daemon thread. A daemon thread runs behind the application. It is started by JVM. The thread stops when all non-daemon threads stop. 

# Logical Operators (#51317)
/root/Java & OO Fundamentals/Operators

 Which of the following are so called "short circuit" logical operators? 

- [ ] &
- [x] ||
- [ ] |
- [x] &&
- [ ] !

## Explanation

Actually we use logically and (&&) and logically or (||) operators for short circuit operators.Not single ' & ' and single ' | ' operators.

# Final classes (#51318)
/root/Java & OO Fundamentals/Classes and Objects

What the following code fragment will print?
```
public class Test extends String{//implementation with overriding methodspublic static void main(String s[]){
      System.out.println(new Test("test class").length);}}
```


- ( ) 10
- ( ) Runtime Error
- ( ) 9
- (x) Compile Error

## Explanation

This code fragment will not compile since you can't subclass a final class. String is declared as final and so it can't be subclassed. It will give compile time error.

# Local variable (#51608)
/root/Java & OO Fundamentals/Scope

What is the output for the following code :
```
01: public class Main {02:     public static void main(String[] args) {03: 04:         int a = 
10;05: 06:         {07:             int a = 
20;08:             System.out.println("a:" + a);09:         }10:         System.out.println("a:" + a);11:     }12: }
```


- ( ) a:10
a:20
- ( ) a:10
a:10
- ( ) a:20
a:20
- ( ) None of above
- (x) This code will not compile

## Explanation

This code can not compile because the local variable 'a' is duplicated.

# Overloading (#52258)
/root/Java & OO Fundamentals/Methods

Methods can be overloaded with a difference only in the type of the return variable. 

- ( ) True
- (x) False

## Explanation

Method overloading (having two methods with the same name within a class) requires that parameters to the methods must be different.

# Modulus operator (#52280)
/root/Java & OO Fundamentals/Operators

What will be the result of the expression
a % b
when a and b are of type int and their values are a = -17 and b = -6? 

- (x) -5
- ( ) -23
- ( ) 5
- ( ) None of these

## Explanation

a % b calculates the remainder when a is divided by b.

# keywords case (#52468)
/root/Java & OO Fundamentals/Naming

Java keywords are written in lowercase as well as uppercase. 

- ( ) True
- (x) False

## Explanation

Java is case sensitive, so keywords must match exactly (lowercase).

# Source code file contents (#52638)
/root/Java & OO Fundamentals/Classes and Objects

One source file must contain only one class or interface.

- ( ) True
- (x) False

## Explanation

A source code file can have only one PUBLIC class, but more than one nonpublic class.

# Initialization of variables (#52672)
/root/Java & OO Fundamentals/Variables

What is the result of the following program?
```java
public class Vehicle {
	public boolean used;
	public String make;
	
	public static void main(String [] args) {
		Vehicle v = new Vehicle();
		if(v.used) {
			System.out.println(v.make);
		} else {
			System.out.println(v.make.length());
		}
	}
}
```


- ( ) A. null
- ( ) B. 0
- ( ) C. Line 7 generates a compiler error.
- ( ) D. Line 8 generates an exception at runtime.
- (x) E. Line 10 generates an exception at runtime.

## Explanation

E. The code compiles fine, so C is incorrect. 
The used field initializes to false and the make field initializes to null for the new Vehicle v. 
Therefore, line 7 is false and line 10 executes. 
Because v.make is a null reference, attempting to invoke its length method results in a NullPointerException at runtime.

# Default values (#52825)
/root/Java & OO Fundamentals/Variables

The following method will compile:
```java
int doIncrement() {
  int i;
  while (i < 10) {
      ++i;
  }
  return i;}
```


- ( ) True
- (x) False

## Explanation

In java local variables don't get default values and must be assigned before first usage. So this code must be rewritten as:
```java
int doIncrement() {
  int i = 0;
  while (i < 10) {
      ++i;
  }
  return i;
}
```


# a .java file contain more than one java classes (#53142)
/root/Java & OO Fundamentals/Variables

a .java file can contain more than one java classes

- (x) True
- ( ) False

## Explanation

Yes, a .java file contain more than one java classes, provided at the most one of them is a public class.

# How many objects are created in the following pie (#53197)
/root/Java & OO Fundamentals/Variables

How many objects are created in the following piece of code? 
```
1: MyClass c1, c2, c3;2: c1 = new MyClass ();3: c3 = new MyClass ();
```


- ( ) 1
- ( ) 4
- ( ) 3
- (x) 2

## Explanation

Only 2 objects are created, c1 and c3. The reference c2 is only declared and not initialized. 

# what is correct result (#53440)
/root/Java & OO Fundamentals/Strings


```java
String str = "pedro,programmer,,555-5555";
String[] values = str.split(",") ;
for(int i = 0; i < values.length; i++)
	System.out.println("Array" + (i + 1) + ": " + values[i]);

```


- ( ) compile error
- ( ) Array1: pedro
Array2: programmer
Array3: 555-5555
- (x) Array1: pedro
Array2: programmer
Array3: 
Array4: 555-5555
- ( ) Array1: pedro
Array2: programmer
- ( ) runtime error 

## Explanation

The split method recognizes that between 2 "," there's empty element.
Reference: http://download.oracle.com/javase/1.4.2/docs/api/java/lang/String.html#split%28java.lang.String%29

# valid declaration (#53502)
/root/Java & OO Fundamentals/Variables

Which of the following is a valid declaration?

- [x] int $x;
- [ ] int 123;
- [x] int _123;
- [ ] int \#dim;
- [ ] int %percent;
- [ ] int *divide;
- [x] int central_sales_region_Summer_2005_gross_sales;

## Explanation

Identifiers must start with $, \_, or a letter. Identifier can't start with a digit.

# "!=!" is legal? (#53664)
/root/Java & OO Fundamentals/Operators

Is this code correct?
```java
boolean x=true;
System.out.println(x!=!x);
```


- (x) True
- ( ) False

## Explanation

Answer is true. In "!=!" we have 2 operators. The first is "!=" and second is "!". So "!=!" is correct statement.

# Free keyword (#53673)
/root/Java & OO Fundamentals/Garbage Collection

You must use the free keyword to notify to the garbage collector that it should clear the instance.

- ( ) True
- (x) False

## Explanation

You must unreference the instance (assign null) and the garbage collector will clear the instance.

# Multiple inheritance in Java (#53716)
/root/Java & OO Fundamentals/Classes and Objects

In Java a class can inherit from multiple classes

- ( ) True
- (x) False

## Explanation

In java there is no native multiple inheritance

# Consider the following program: (#53751)
/root/Java & OO Fundamentals/Classes and Objects


```
1: import myLibrary.*;2: public class ShowSomeClass3: {4: // code for the class...5: }
```
What is the name of the java file containing this program?

- ( ) myLibrary.java
- (x) ShowSomeClass.java
- ( ) ShowSomeClass
- ( ) ShowSomeClass.class
- ( ) Any file name with the java suffix will do

## Explanation

The file name should be the name of the public class with the .java suffix.

# Variables (#53957)
/root/Java & OO Fundamentals/Variables

A local variable and a method parameter can have the same name.

- ( ) True
- (x) False

## Explanation

I guess the question refers to a local variable within a method; not class variable and hence 'false' is the right answer.

# Java Program (#54317)
/root/Java & OO Fundamentals/Platform

Is it possible to compile and run a java program without main() method

- (x) True
- ( ) False

## Explanation

Yes it is possible by having a static block & System.exit(0)
The static initialization blocks get executed as soon as the class is loaded. During run time JVM will search for the main method after exiting them.

# Java is fully object oriented language? (#54423)
/root/Java & OO Fundamentals/Variables

Is this statement true or false : Java is fully object oriented language.

- ( ) True
- (x) False

## Explanation

Yes truth is java is not fully object oriented one of the reason being that it uses primitives like int, float etc which are not classes .

# JavaBeans methods (#54633)
/root/Java & OO Fundamentals/Naming

Which of these method names follow the JavaBeans standard?(Choose all that apply)

- [ ] changeLength
- [ ] putVariable
- [x] setDimension
- [x] getWidth

## Explanation

JavaBeans methods must be named using camelCase and depending on the method's purpose, must start with set, get, is, add, or remove.

# Out of scope (#54901)
/root/Java & OO Fundamentals/Scope

What is the result?
```
1: int num = 
0;2: for (int i=
0; i<
5; i++) {3:     num = num+i;4: }5: System.out.println(i+": "+num);
```


- ( ) 5: 0
- (x) Compilation error
- ( ) 5: 10
- ( ) 5: 5

## Explanation

i is defined inside for block, hence is local. System.out.println can't see it.

# Heap and Stack difference (#54903)
/root/Java & OO Fundamentals/Platform

The Stack holds:

- [ ] class level variables
- [ ] object created inside method body
- [x] local variables
- [ ] object instance variables

## Explanation

The Stack holds local variables and partial results, and plays a part in method invocation and return.

# Static and local variable (#55104)
/root/Java & OO Fundamentals/Platform

Can I declare local variable as static ?

- ( ) True
- (x) False

## Explanation

see : http://download.oracle.com/javase/tutorial/java/nutsandbolts/variables.html
Local variables in Java are declared inside method or a block. They are visible only from method/block in which they are declared. Only variables declared in class scope can be declared static - they have same value in every instance of this class. 

# Primitives in Java (#55123)
/root/Java & OO Fundamentals/Variables

What are the eight primitive data types supported by the Java programming language?

- [x] byte, short, int, long, float, double, boolean, char
- [ ] byte, short, integer, long, float, double, string, char
- [ ] byte, array, integer, vector, float, double, string, char
- [ ] List, array, integer, vector, float, double, string, char

## Explanation

the Java programming language supports eight primitive data types. A primitive type is predefined by the language and is named by a reserved keyword. Primitive values do not share state with other primitive values. The eight primitive data types supported by the Java programming language are:
 * byte: The byte data type is an 8-bit signed two's complement integer. It has a minimum value of -128 and a maximum value of 127 (inclusive). The byte data type can be useful for saving memory in large arrays, where the memory savings actually matters. They can also be used in place of int where their limits help to clarify your code; the fact that a variable's range is limited can serve as a form of documentation.
 * short: The short data type is a 16-bit signed two's complement integer. It has a minimum value of -32,768 and a maximum value of 32,767 (inclusive). As with byte, the same guidelines apply: you can use a short to save memory in large arrays, in situations where the memory savings actually matters.
 * int: The int data type is a 32-bit signed two's complement integer. It has a minimum value of -2,147,483,648 and a maximum value of 2,147,483,647 (inclusive). For integral values, this data type is generally the default choice unless there is a reason (like the above) to choose something else. This data type will most likely be large enough for the numbers your program will use, but if you need a wider range of values, use long instead.
 * long: The long data type is a 64-bit signed two's complement integer. It has a minimum value of -9,223,372,036,854,775,808 and a maximum value of 9,223,372,036,854,775,807 (inclusive). Use this data type when you need a range of values wider than those provided by int.
 * float: The float data type is a single-precision 32-bit IEEE 754 floating point. Its range of values is beyond the scope of this discussion, but is specified in section 4.2.3 of the Java Language Specification. As with the recommendations for byte and short, use a float (instead of double) if you need to save memory in large arrays of floating point numbers. This data type should never be used for precise values, such as currency. For that, you will need to use the java.math.BigDecimal class instead. Numbers and Strings covers BigDecimal and other useful classes provided by the Java platform.
 * double: The double data type is a double-precision 64-bit IEEE 754 floating point. Its range of values is beyond the scope of this discussion, but is specified in section 4.2.3 of the Java Language Specification. For decimal values, this data type is generally the default choice. As mentioned above, this data type should never be used for precise values, such as currency.
 * boolean: The boolean data type has only two possible values: true and false. Use this data type for simple flags that track true/false conditions. This data type represents one bit of information, but its "size" isn't something that's precisely defined.
 * char: The char data type is a single 16-bit Unicode character. It has a minimum value of '\u0000' (or 0) and a maximum value of '\uffff' (or 65,535 inclusive).

# || and && (#55211)
/root/Java & OO Fundamentals/Operators

The || and && operators work only with boolean operands.

- (x) True
- ( ) False

## Explanation

It is truth. You can't use, for example, integers with these operators.

# JRE and JDK purpose (#55508)
/root/Java & OO Fundamentals/Platform

If you want to be able to compile java code you need...

- ( ) To have a JRE
- (x) To have a JDK
- ( ) Both
- ( ) None of both
- ( ) either one or the other

## Explanation

The JDK also includes a JRE in its installation, thus you just need a JDK and not specifically both.

# Memory Management (#55519)
/root/Java & OO Fundamentals/Garbage Collection


```

1. MyClass obj = new MyClass()
2.
// more code here
3. obj = null;
4. /* insert code here */
```
Which statement should be placed at line 4 to suggest that the virtual
machine expend effort toward recycling the memory used by the
object obj?

- (x) System.gc();
- ( ) Runtime.gc();
- ( ) System.freeMemory();
- ( ) Runtime.getRuntime().growHeap();
- ( ) Runtime.getRuntime().freeMemory();

## Explanation

reference:
http://docs.oracle.com/javase/6/docs/api/java/lang/System.html#gc()


The call `System.gc()` is effectively equivalent to the call: `Runtime.getRuntime().gc()`

# Operands promotion (#55524)
/root/Java & OO Fundamentals/Operators

Which of the following operators can perform promotion on their operands?

- [x] +
- [x] -
- [ ] ++
- [ ] --
- [x] ~
- [ ] !

## Explanation

A, B, E are correct. All numeric operators promote (except ++ and --). !, which is strictly boolean, does not promote.

# Static Variable (#55545)
/root/Java & OO Fundamentals/Variables

What features define a Static Variable?

- ( ) A Static Variable is declared in a method, constructor, or block. They are visible only in the method, constructor, or block in which they are declared. 
- ( ) A Static Variable is declared in a class, but outside a method. They are visible by all methods in the class. They are created when instance of class is created with (new).
- (x) A Static Variable are declared with the static keyword in a class, but outside a method. There is only one copy per class, regardless of how many objects are created from it.

## Explanation

The first answer define the features of a local variable.
The second answer define the features of an instance variable.
The third answer define the features of a static variable.
See more information: 
http://download.oracle.com/javase/tutorial/java/nutsandbolts/variables.html

# Bytecode extension (#55549)
/root/Java & OO Fundamentals/Platform

What is the extension name of compiled bytecode file?
You do not need to specify the period ( . ) 

- [x] class

## Explanation

Compiled bytecode extension is 'class'.

# The keyword this (#55553)
/Java (core)/Java SE - basic/Java Objects/Object

In case of successfully compiled code: the keyword 
```
this
```
 always refers to the object that executes the line of code that includes the 
```
this
```
 keyword.

- (x) True
- ( ) False

## Explanation

From Java Tutorials:"Within an instance method or a constructor, 
```
this
```
 is a reference to the current object — the object whose method or constructor is being called."

# Variable initialization 2 (#55556)
/root/Java & OO Fundamentals/Variables

Given the following class:
```
01: public class Test {02: 03:     int i;04: 05:     public static void main(String[] argv) {06:         new Test().doSomething();07:     }08: 09:     void doSomething() {10:         i++;11:         System.out.println(i);12:     }13: }
```
What will be the result when running the main method?

- [x] 1
- [ ] 2
- [ ] Compilation error because variable i is not initialized.
- [ ] Runtime exception because variable i is not initialized

## Explanation

Member variables are initialized with a default value. In the case of int the default value is 0

# JavaBeans Naming conventions (#55579)
/root/Java & OO Fundamentals/Naming

Which of the method names below follow the JavaBeans naming convention for property accessor methods?

- [ ] addSize
- [x] getFirstName
- [ ] deleteRep
- [ ] putDimensions
- [x] isJakarta

## Explanation

'get' and 'is' are valid prefixes. 'add' can only be used with Listener methods. 'delete' and 'put' are not standard JavaBeans name prefixes

# Use void keyword (#55611)
/root/Java & OO Fundamentals/Methods

Which of the following method definitions are correct if you are defining a method that doesn't return anything.

- [x] public void myMethod(int i)
- [ ] private Void myNewMethod(int i)
- [x] protected static void myMethod (int i)
- [ ] public null myMethod (int i)
- [ ] public void(int i)

## Explanation

remember to use the void keyword, also that while Java is case sensitive Case is different from case. The "public void(int i)" is trying to make a method called void so that isn't nice to the java language (compiler).

# What is the output? (#55680)
/root/Java & OO Fundamentals/Variables

What is the output? 
```
1: float a=Float.NaN;2: float b=a;3: System.out.println(a==b);
```


- ( ) true
- (x) false
- ( ) compile error
- ( ) Float.NaN doesn't exist in Java
- ( ) Float.NaN

## Explanation

The == operator compares primitive type values, not references. Since Float.NaN is a constant denoting a not-a-number state of a float variable it is implicit that no two variables that are not a number are equal. 
For example:
```
float f = 
0.0f / 
0.0f;System.out.println(Float.isNaN(f));
```
will print true. Nothing can be said about possible value of f (it is not known whether it is infinitely large or small, whether this infinity would be positive or negative). Because of that it cannot be said, that two such values are equal (because nothing is known about the value itself).
See http://java.sun.com/j2se/1.4.2/docs/api/java/lang/Float.html

# Comment types (#55688)
/root/Java & OO Fundamentals/Comments


```
// What type of comment is this?
```


- (x) Single-line comment
- ( ) Multi-line comment
- ( ) Javadoc comment

## Explanation

This type of comment starts with the // characters and ends at the end of the line.

# Operator Assignment (#55701)
/root/Java & OO Fundamentals/Variables

What will be the output of following program
```
1: int i=
0;2: i=i++;3: System.out.println(i);
```


- [x] 0

## Explanation


```
i=i++;
```
 is equivalent to
```
int j=i++;i=j;
```
which will result to 0

# Generic Instantiation (#55716)
/root/Java & OO Fundamentals/Variables

Which of the following compiles without error (assume to Java SE 5):

- [x] 
```
List a = new ArrayList();
```

- [x] 
```
List<String> b = new ArrayList();
```

- [x] 
```
List c = new ArrayList<String>();
```

- [x] 
```
List<String> d = new ArrayList<String>();
```

- [ ] 
```
List<String> e = new ArrayList<?>();
```

- [x] 
```
List<?> f = new ArrayList<String>();
```


## Explanation

`Answer e is wrong, because the compiler can not convert <?> to <String>. And if we compile with -Xlint:unchecked Answer b just generates a compiler warning about an unchecked conversion, but it compiles as all the other options.`

# changing values for a final attribute (#55742)
/root/Java & OO Fundamentals/Encapsulation


```
01: public class HelloWorld{02:   final private int number = 
10;03: 04:   public void setNumber(int number) {05:     this.number = number;06:   }07: 08:   public int getNumber() {09:     return number;10:  }11: }
```
 What will this return:
```

HelloWorld hello = new HelloWorld();
hello.setNumber(
20);
System.out.println(hello.getNumber());
```


- ( ) 20
- ( ) 10
- (x) will not compile
- ( ) none of the above

## Explanation

final attributes cannot be changed

# superclass constructors (#55812)
/root/Java & OO Fundamentals/Classes and Objects

Given the following code, what is the output?
```
01:  02: public class MyClass {03: 04:     public static void main(String[] args) {05:         B b = new B();06:     }07: }08: 09: class A {10: 11:     public A(int x) {12:         System.out.println("A- constructor");13:     }14: }15: 16: class B extends A {17: 18:     public B() {19:         super();20:     }21: }
```


- ( ) A- constructor
- ( ) nothing happens
- (x) compile-time error
- ( ) runtime error

## Explanation

The code will not compile. The B class requires a default constructor from the A class but there is no default constructor because there is a constructor which gets an int parameter. 

# Flow Control (#55903)
/root/Java & OO Fundamentals/Flow Control

What will be the output after the following code runs?
```
1: for (int i = 
0;i <= 
10;i++){2:     switch(++i){3:         case 
3: continue;4:         case 
5: break;5:         case 
9: return;6:     }7:     System.out.print(i);8: }
```


- ( ) 1579
- ( ) 157911
- (x) 157
- ( ) 13579

## Explanation

`The exact execution of statements goes like this:`int i = 
0; // i == 0
++i; // i == 1
System.out.print(i); // prints 1, output == &quot;1&quot;
i++; // i == 2
i &lt; 
10 == true // loop continues
++i; // i == 3
case 
3: continue; // skips System.out.print, output = &quot;1&quot; still
i++; // i == 4
i &lt; 
10 == true // loop continues
++i; // i == 5
case 
5: break; // breaks only the switch statement and goes directly after its closing bracket
System.out.print(i); // prints 5, output = &quot;15&quot;
i++; i == 
6
i &lt; 
10 == true // loop continues
++i; // i == 7
System.out.print(i); // prints 7, output = &quot;157&quot;
i++; // i == 8
i &lt; 
10 == true; // loop continues
++i; // i == 9
case 
9: return; // ends the method execution and returns to the calling point, output remains &quot;157&quot;`

# Scope in try catch blocks (#55940)
/root/Java & OO Fundamentals/Scope

What prints flobber() if called?
```
01: class Klakatt {02:   private int shadow = 
1;03: 04:   public void flobber() {05:     int shadow = 
2;06:     try {07:       int shadow = 
3;08:       throw new RuntimeException();09:     } catch (Exception e) {10:       System.out.println(shadow);11:     }12:     System.out.println(shadow);13:   }14: }
```


- [ ] Prints: 2 3
- [ ] Prints: 3 3
- [ ] Prints: 2 2
- [ ] An Exception is thrown at Runtime
- [x] Compile Error

## Explanation

A local variable can't have the same name an instance variable has.

# String assignment (#55993)
/Java (core)/Java SE - basic/Language Elements/Variables

The output of the following code will be: "Apples are tasty"
```
1: public class Printer {2:     public static void main(String[] args) {3:         String a = "Apples";4:         String b = a;5:         b = b + " are tasty";6:         System.out.print(a);7:     }8: }
```


- ( ) True
- (x) False

## Explanation

Strings cannot have their value changed. Every time it should happen, new instance of String is created (or taken from the String constant pool). 
String a = "Apples"; // object String is created
String b = a; // variable b is pointing to the same object as variable a 
b = b + " are tasty";// new String object is created from b+"are tasty" and assigned to variable b
System.out.print(a); // variable a still pointing to String that contains "Apples"

# finalize() question (#56025)
/root/Java & OO Fundamentals/Garbage Collection

Calling finalize() on an object will cause it to be garbage collected.

- ( ) True
- (x) False

## Explanation

Calling finalize will not invoke the garbage collector. finalize() is called by the garbage collector when no references to the object exist.

# Final type (#56032)
/root/Java & OO Fundamentals/Variables

What happens if trying to assign values to final arguments inside the method.

- ( ) Nothing
- (x) Compile error
- ( ) RunTime exception

## Explanation

 Method arguments marked final are read-only. Compiler error, if trying to assign values to final arguments inside the method.

# Determine the result of this code: (#56084)
/root/Java & OO Fundamentals/Operators

What is printed if you run this code?
```
1: boolean x = true;2: int j = 
4;3: if ((x=false) && (j > 
5)) {4:    System.out.println("OK!");5: } else {6:    System.out.println("NO!");7: }
```


- ( ) OK!
- (x) NO!
- ( ) This code not compile.

## Explanation

It's legal to assign a boolean value in the condition expression, after this assignment x will have the value of false.

# Visibility (#56085)
/root/Java & OO Fundamentals/Classes and Objects

Look at the following source file:
```
package cert;class Beverage { }
```
Now look at the second source file:
```
package exam.stuff;import cert.Beverage;class Tea extends Beverage { }
```


- [x] Beverage file compiles fine
- [ ] Beverage file does not compile
- [x] Tea file does not compile
- [ ] Tea file compiles fine

## Explanation

As you can see, the superclass (Beverage) is in a different package from the
subclass (Tea). The import statement at the top of the Tea file is trying (fingers
crossed) to import the Beverage class. The Beverage file compiles fine, but when we
try to compile the Tea file we get something like:
Can't access class cert.Beverage. Class or interface must be
public, in same package, or an accessible member class.
import cert.Beverage;

# Operators (#56104)
/root/Java & OO Fundamentals/Operators

for the code segment
```
1: int n = 
0;2: 3: if (++n == n++) {4:      System.out.println("Equals");5: } else {6:      System.out.println("Not equals");7: }
```
What is the output of the following code?

- [x] Equals

## Explanation

in order of priority, ++n is incremented by one, therefore n has the value 1.
n++ not increased and continues with the value 1.
Therefore the sentence ( ++n == n++ ) is true

# Increment operator (#56122)
/root/Java & OO Fundamentals/Operators

Expressions y++ and ++y give the same result.

- ( ) True
- (x) False

## Explanation

y++ returns the value of y for further expression evaluation and then increments y
++y increments y first and then returns the (already incremented) value.

# Variables (#56124)
/root/Java & OO Fundamentals/Variables

A local variable and a method parameter can't have the same name as shown in the Clazz class.
```
public class Clazz {
  public int calc(int x) {
     return int x;
  }}
```


- (x) True
- ( ) False

## Explanation

It is true because a method parameter declares a variable also, hence if a local variable has the same name of a parameter it would be a repeated declaration of the same variable which is not allowed in Java.

# Keywords in method declaration (#56210)
/root/Java & OO Fundamentals/Methods

Which of the following code compiles ?

- [x] 
```
 public static final void method() {
 //code}
```

- [ ] 
```
 public static final void int(){
 //code}
```

- [x] 
```
 final static public void method(){
 //code}
```

- [ ] 
```
 void static method(){
 //code}
```


## Explanation

<a href="http://download.oracle.com/javase/tutorial/java/nutsandbolts/_keywords.html">http://download.oracle.com/javase/tutorial/java/nutsandbolts/_keywords.html</a>

# What is the result ? (#56252)
/root/Java & OO Fundamentals/Classes and Objects


```
01:  02:   class Slug {03:       static void crawl() {System.out.print("crawling ");}04:   }05:   public class OrangeSlug extends Slug {06:       public static void main (String[] args){07:           Slug[] sa = {new Slug(), new OrangeSlug()};08:           for (Slug s: sa)09:              crawl();10:       }11:     static void crawl(){12:        System.out.print("shuffling ");13:     }14: }
```


- ( ) crawling crawling
- ( ) crawling shuffling
- (x) shuffling shuffling
- ( ) compilation fails 
- ( ) An exception is thrown at runtime

## Explanation

Method crawl() is invoked directly, note the reference is not used (s.crawl()), therefore the correct answer is "shuffling shuffling". If the reference was used then the answer would have been "crawling crawling".

# Instance Variable (#56268)
/root/Java & OO Fundamentals/Methods

A static method can refer to any instance variable of the class. 

- (x) True
- ( ) False

## Explanation

It is illegal in Java to refer to instance variables from a static method.

# Private Constructor (#56312)
/root/Java & OO Fundamentals/Classes and Objects

A constructor cannot be private.

- ( ) True
- (x) False

## Explanation

A private constructor can be used any time no outside class should be able to create an instance. This is utilized for utility classes as well as situations where instance creation must be carefully controlled (e.g. a singleton).

# Parameters (#56336)
/root/Java & OO Fundamentals/Methods

What is the output for this class :
```
01: public class Test {02: 03:     public static void main(String[] args) {04:         int a = 
1;05:         int b = 
2;06:         int c = add(a, b);07:         System.out.println("a:" + a + ", b:" + b + ", c:" + c);08: 09:     }10: 11:     static int add(int a, int b) {12:         a = a + b;13:         return a;14:     }15: }
```


- (x) a:1, b:2, c:3
- ( ) a:3, b:2, c:3
- ( ) It doesn't compile
- ( ) None of this answers are correct

## Explanation

The add method can be used here because it's a static method.
Method add() actually works with copies of a and b and doesn't change a.

# Garbage Collection (#56353)
/root/Java & OO Fundamentals/Garbage Collection

Which of the following statements are true?

- [x] You cannot be certain at what point Garbage collection will occur
- [ ] Once an object is unreachable it's trash and is at the mercy of the garbage collector.
- [ ] Garbage collection ensures programs will never run out of memory
- [ ] All the above

## Explanation

Once an object is unreachable it will be subject to garbage collection but you cannot be certain it ever will actually be garbage collected. The garbage collection mechanism only applies to objects not primitives. You should be able to guess that garbage collection cannot ensure programs do not run ever run out of memory, but it does ensure that memory no longer required is reallocated to be available.

# java file naming (#56388)
/root/Java & OO Fundamentals/Naming

Under which circumstances does a java source file have no naming restrictions?

- ( ) There are multiple classes in the file
- (x) The file contains only non public classes
- ( ) The file contains an interface with the access modifier protected
- ( ) The file contains only classes and interfaces with the access modifier abstract
- ( ) There are multiple interfaces in the file

## Explanation

Java source files without a public class are not bound to naming restrictions, otherwise the file name must match the class name. A java source file can have multiple classes but only one can be public.

# Variable indirectly initialized (#56389)
/root/Java & OO Fundamentals/Variables

What is the result ?
```
01: 02:     public static void main(String[] args) {03:         int j;04:         if(true) j = 
0;05:         for(int i=
0;i<
50;++i) {06:             System.out.print(i);07:             if(i>
9) break;08:             j = i;09:         }10:         System.out.print(j);11:     }
```


- ( ) Compilation fails
- ( ) Runtime error
- ( ) 012345678910
- ( ) 0123456789
- ( ) 01234567891010
- (x) 0123456789109
- ( ) 01234567899

## Explanation

The loop stop when i equals 10 and j is assigned with i when i equals 9.
The compiler identify that j is initialized at line 3.

# ?: (#56404)
/root/Java & OO Fundamentals/Operators

consider the statement 
```
x = (a > b) ? a : b;
```
then the value of x is 27, if a = 18 and b = 27.

- (x) True
- ( ) False

## Explanation

The statement is equivalent to: 
`if (a > b)`   x = a;
else
   x = b;`

# variable (#56450)
/root/Java & OO Fundamentals/Variables

Declarations must appear at the start of the body of a Java method.

- ( ) True
- (x) False

## Explanation

They can appear anywhere within the body of the method.

# The main method (#56548)
/root/Java & OO Fundamentals/Classes and Objects

Can main() method be overloaded?

- (x) true
- ( ) false

## Explanation

The main() method is a special method for a program entry. You can overload main() method in any ways. But if you change the signature of the main method, the entry point for the program will be gone.

# 1 (#56572)
/root/Java & OO Fundamentals/Classes and Objects

The main method can be declared as follows (assume that SomeException is a well-known exception):
```
public static void main(String args[])
  throws SomeException {
   // ........... } 
```


- (x) True
- ( ) False

## Explanation

As long as SomeException is known to the class (ie. it has been previously imported or it's of such type that importing is not necessary for a successful compilation), this is a valid construct.

# superclass (#56885)
/root/Java & OO Fundamentals/Classes and Objects

The class that inherits from another class is called superclass

- ( ) True
- (x) False

## Explanation

The class that inherits from another class is called a subclass. The class that is subclassed by a subclass is called the superclass.

# naming (#56891)
/root/Java & OO Fundamentals/Naming

Which of these are not legal identifiers. Select the four correct answers.

- [x] 1alpha
- [ ] _abcd
- [x] xy+abc
- [x] transient
- [x] account-num
- [ ] very_long_name

## Explanation

REFERENCE: http://download.oracle.com/javase/tutorial/java/nutsandbolts/variables.html

# GC (#56924)
/Java (core)/Java SE - basic/Misc/Garbage Collection

The Garbage Collector relieves programmers from all burden of freeing allocated memory.

- ( ) True
- (x) False

## Explanation

In Java, GC frees memory by removing objects that no longer referenced by a reference variable. If the program keeps unneeded references to unused objects GC can't free the associated memory.

# Naming (#56933)
/root/Java & OO Fundamentals/Naming

Which of these are legal identifiers. Select the three correct answers.

- [x] number_1
- [x] number_a
- [x] $1234
- [ ] -volatile

## Explanation

Reference:
http://download.oracle.com/javase/tutorial/java/nutsandbolts/variables.html

# Modulus operator (#56959)
/root/Java & OO Fundamentals/Operators

What will be the result of the expression
a / b
when a and b are of type int and their values are a = 10 and b = 6? 

- ( ) 4
- (x) 1
- ( ) 1.66
- ( ) None of these.

## Explanation

The division operator (/) may be used with floating-point as well as integer types. 
It returns the quotient of a division operation.
Therefore, 10 / 6 will return 1.

# What will be the output of the following program? (#57089)
/root/Java & OO Fundamentals/Classes and Objects

What will be the output of the following program?
```
01: public class Ques01 {02: 03:     public static void main(String[] args) {04:         test1(
1, 
1.00f, '1');05:         test1(new Integer(
1), new Float(
1.00), new Character('1'));06:     }07: 08:     static void test1(int a, float b, char c){09:         System.out.println("Primitive types");10:     }11: 12:     static void test1(Integer a, Float b, Character c){13:         System.out.println("Reference types");14:     }15: }
```


- ( ) The program will result in compilation errors telling that the definition of method test1 is duplicated. 
- (x) The program will output 'Primitive types Reference types'. 
- ( ) The program will output 'Reference types Primitive types'. 
- ( ) The program will output 'Reference types Reference types'. 

## Explanation

The method test1() will be considered as an overloaded function by the compiler, so the first call (with primitive values) to the method test1() will match the first definition of the test1() method and the second call (with reference values) to the method test1() will match the second overloaded form. 

# Final keyword (#57162)
/root/Java & OO Fundamentals/Classes and Objects

If you add the final keyword to a reference, then the referenced Object becomes immutable.

- ( ) True
- (x) False

## Explanation

It's not the referenced Object that becomes immutable but the reference itself.
final StringBuffer sb = new StringBuffer(); 
sb.append('a'); 
is ok while 
final StringBuffer sb = new StringBuffer(); 
sb = new StringBuffer(); 
does not work.

# non-static(instance) methods (#57181)
/root/Java & OO Fundamentals/Methods

What will be the output?
```
1: public class Test3{2:    public void method(){ 3:        System.out.println("Called");4:    }5:    public static void main(String[] args){6:        method();7:    }8: }
```


- ( ) "Called"
- (x) Compiler Error
- ( ) Runtime Error
- ( ) Nothing

## Explanation

non-static(instance) methods or variables cannot be referenced from static context. Compiler will give the following error while compiling the above code: Test3.java:6: non-static method method() cannot be referenced from a static context method();

# Final keyword (#57185)
/root/Java & OO Fundamentals/Classes and Objects

If you add the final keyword to a reference, then the referenced Object becomes immutable.

- ( ) True
- (x) False

## Explanation

It's not the referenced Object that becomes immutable but the reference itself.
final StringBuffer sb = new StringBuffer(); 
sb.append('a'); 
is ok while 
final StringBuffer sb = new StringBuffer(); 
sb = new StringBuffer(); 
does not work.

# String comparision (#57237)
/root/Java & OO Fundamentals/Strings

Referring to the code below, what is the correct way to compare the strings str1and str2 in an "if" statement, checking only to see if the strings have the same characters?
```
String str1 = "My name is Billy.";String str2 = "My name is Billy.";
```


- ( ) `if (str1.compareTo(str2)){}`
- (x) `if (str1.equals(str2)){}`
- ( ) `if (str1 <> str2){}`
- ( ) `if ((str1 - str2) == 
0){}`
- ( ) `if (str1 == str2){}`

## Explanation

choice c and d causes compilation error. The compareTo method returns an int and hence cannot be used in if statement. The == operator compares the references of string objects and hence it is not correct. Choice b is correct as the equals method compares the characters of the 2 strings and returns true if they are the same. Hence it can be used in if statement.

# constructor (#57406)
/root/Java & OO Fundamentals/Classes and Objects

A constructor

- ( ) must have the same name as the class it is declared within.
- ( ) is used to create objects.
- ( ) may be declared private
- (x) all true

## Explanation

Constructor can be private, must have the same name as the name of the class and it is used to create an object.

# System.gc(); (#57422)
/root/Java & OO Fundamentals/Garbage Collection

You can force garbage collection using System.gc().

- ( ) True
- (x) False

## Explanation

Garbage collection is automated in java. System.gc() in your code the java vm may or may not decide at runtime to do a garbage collection at that point. Garbage collection can never be forced.

# Select valid constructor signature (#57425)
/Java (core)/Java SE - basic/Java Objects/Class

Which of the following can be a valid constructor signature?

- [x] 
```
DogHouse(String dogName)
```

- [ ] 
```
int DogHouse(String dogName)
```

- [ ] 
```
void DogHouse(String dogName)
```

- [ ] 
```
DogHouse(dogName)
```

- [x] 
```
DogHouse()
```


## Explanation

A constructor has no return type (even no void) , if we add a return type , it is not a compile error , it simply defines a function that has the same name of the constructor.

# Final variable (#57549)
/root/Java & OO Fundamentals/Variables

What is the output if the following code is executed ?
```

01: public class Car {
02: private final String constructorName ="Peugeot";
03: public String getConstructorName() {
04:
   return constructorName;
05: }
  
06: public void setConstructorName(String c) {
07:
   this.constructorName = c;
08: }
      
09: public static void main(String[] args) {
10:
   final Car superCar = new Car();
11: superCar.setConstructorName("Ferrari");
12: System.out.println(superCar.getConstructorName());
12: }
      
14: }
```


- ( ) Ferrari
- ( ) Peugeot
- ( ) Runtime Exception
- (x) Compilation error at line 07
- ( ) Compilation error at line 11

## Explanation

Compilation error at line 07 : The constructorName field is final and cannot be assigned here.

# Constructor throws Exception (#57716)
/root/Java & OO Fundamentals/Classes and Objects

A class constructor can throw an exception.

- (x) True
- ( ) False

## Explanation

Constructors can throw exceptions. It is a valid construct in java.

# constructors (#57721)
/root/Java & OO Fundamentals/Classes and Objects

Constructors can be inherited, thus they can be overridden.

- ( ) True
- (x) False

## Explanation

Constructors are not overridden in Java. They are also not inherited. The constructor always calls one of the constructors of it's superclass by calling super() (default constructor), and if you don't type it yourself, the compiler will do it for you.

# Names of Packages (#57886)
/root/Java & OO Fundamentals/Naming

Reverse domain names, appended with division and/or project names it's for example:

- [x] com.geeksanonymous.steps.client.Utilities
- [ ] Utilities.client.steps.geeksanonymous.com
- [x] com/geeksanonymous/steps/client/Utilities

## Explanation

Sun recommends that developers use reverse domain names,
appended with division and/or project names. For example, if your domain
name is geeksanonymous.com, and you're working on the client code for
the TwelvePointOSteps program, you would name your package something
like com.geeksanonymous.steps.client. That would essentially change the
name of your class to com.geeksanonymous.steps.client.Utilities.

# Overriding Concept (#58085)
/root/Java & OO Fundamentals/Classes and Objects


```
01: class abc {02:    private void test(){
 03:        System.out.println("abc");04:    }05: }06: 07: class def extends abc {08:     void test(){09:         System.out.println("def");10:     }11: }
```
In the above case, method test() in class def is said to be ....................

- ( ) Overloaded
- ( ) Overridden
- (x) None

## Explanation

It is not overloaded as it does not follow the concept of method overloading i.e. method with same name but different arguments.
Neither it can be said overridden as being the private method it is not visible to class def.

# While (#58114)
/root/Java & OO Fundamentals/Flow Control

Will the following code run?
```
int i=
0;while (i) System.out.print("x") ;
         
```


- ( ) True
- (x) False

## Explanation

while (THIS MUST BE A BOOLEAN VALUE) 
So using i ( an int) causes a compilation error.

# Basic Operations (#58379)
/root/Java & OO Fundamentals/Operators

After execution of the code fragment below, what are the values of the variable x, y and z?
```
1: int x = 
10, y = 
15;2: int z = x++ + --y;
```


- ( ) z = 25, x = 11, y = 14
- ( ) z = 24, x = 10, y = 14
- (x) z = 24, x = 11, y = 14
- ( ) z = 25, x = 10, y = 15

## Explanation

The code is equivalent to:
```
1: int x = 
10, y = 
15;2: y = y - 
1; // y is now 143: int z = x + y; // z is now 10 + 14 = 244: x = x + 
1; // x is now 11
```


# Constructor of the subclass (#58979)
/root/Java & OO Fundamentals/Classes and Objects

A subclass may call the constructor of a parent class as follows... *

- ( )  this.super(...)
- (x) super(...)
- ( ) parent(...)
- ( ) this is NOT possible!

## Explanation

super(...). Use super to call a constructor in a parent class. Calling the constructor for the superclass must be the first statement in the body of a constructor. If you are satisfied with the default constructor in the superclass, there is no need to make a call to it because it will be supplied automatically.

# invalid unicode in comment (#59031)
/root/Java & OO Fundamentals/Comments

What is the output of the following code:
```

  public static void main(String[] args) {
         // tha'\u
  }
```


- (x) cause a compiler error
- ( ) cause runtime error
- ( ) this piece of code will compile and run without problems

## Explanation

Raises an 'illegal unicode escape' error.
The \u sequence indicates the beginning of a unicode escape, but it must be followed by four hexadecimal digits.

# Class (#59040)
/root/Java & OO Fundamentals/Classes and Objects

We can have multiple, not nested, top level classes with private access modifier in a single source file ?

- ( ) True
- (x) False

## Explanation

No, private access modifier is not applicable to top level classes in java

# Splitting classes and packages (#59251)
/root/Java & OO Fundamentals/Classes and Objects

Task:
create Class A in package apack
create Class B,which extends Class A, in package bpack

- ( ) 
```
1:  2: /*A.java*/3: package apack;4: public class A{ }
```

```
1:  2: /*B.java*/3: package apack;4: public class B extends A{ }
```

- ( ) 
```
1:  2: /*A.java*/3: package apack;4: public class A{ }
```

```
1:  2: /*B.java*/3: package bpack;4: public class B { }
```

- ( ) 
```
1:  2: /*A.java*/3: package apack;4: package bpack;5: public class A{ }6: public class B extends A{ }
```

- ( ) 
```
1:  2: /*A.java*/3: package apack;4: public class A{ }
```

```
1:  2: /*B.java*/3: package bpack;4: public class B extends A { }
```

- ( ) 
```
1:  2: /*A.java*/3: package apack;4: class A{ }
```

```
1:  2: /*B.java*/3: package bpack;4: public class B extends A { }
```

- (x) 
```
1:  2: /*A.java*/3: package apack;4: public class A{ }
```

```
1:  2: /*B.java*/3: package bpack;4: import apack.A;5: public class B extends A { }
```


## Explanation

The first possibility ist not correct because the two classes would be in the same package.
In each .java-File there only can be ONE public class in ONE package!
Due to the line above there must be two files.
And the last possibility is wrong because a class has to be marked public to have access outside the package.

# Terminology (#59277)
/OO /OO with Java - basic/Object and Class

Fill in the blank with the correct answer given below.
A named collection of fields that hold data values and methods that operate on them is called a _______.

- ( ) method
- (x) class
- ( ) package
- ( ) packet
- ( ) unit

## Explanation

a method is a named operation that may be part of a class.
a package is a named group of compilation modules that may include classes
a packet is a block of data transmitted on a network communications channel.
a unit is an atomic element in a generic sense.

# memory leak. (#59362)
/root/Java & OO Fundamentals/Garbage Collection

Overriding finally method guarantees that object will be garbage collected.

- ( ) True
- (x) False

## Explanation

Its false. 
If finalize method throws exception then it may happen the object is never garage collected.

# What will be the output of the following code? (#59372)
/root/Java & OO Fundamentals/Classes and Objects


```
 public class Student {
  private String name;
      Student(String name){
      this.name = name;
  }
  public static void main(String arg[]){
      System.out.println(new Student("Renjith"));
  }
    public String toString(){
      return this.name;
  }}
```


- ( ) Compilation fails
- ( ) Runtime Exception
- (x) It will print the string "Renjith"

## Explanation

The java toString() method can override when we need a string representation of an object.

# Static (#59373)
/root/Java & OO Fundamentals/Methods

Which of the following choices can be marked as static

- [x] Variables
- [x] Interfaces
- [x] Methods
- [ ] Constructors
- [x] Initialization blocks

## Explanation

Contructors are used to create new intances : it's nonsense to declare it static.

# equal (#59479)
/root/Java & OO Fundamentals/Strings

What's the result from the following code when run:
```
1: 
public static void main(String[] args) {2: 3:         String a = "test";4:         String b =
new String("test");5:         String c = "test";6:         System.out.println(a==b);7:         System.out.println(c==a);8:     }
```


- ( ) true
true
- ( ) true
false
- (x) false
true
- ( ) false
false

## Explanation

String literals are stored internally as instances of String and are managed in a pool of such strings created at compile time and linked to their containing class (or compilation object). The compiler is "smart enough" to keep only unique strings in the pool, so if a literal is used more than once in the code the compiler points the reference to the existing String instance in the pool.
Thus when line 3 is compiled “test�? is added to the literals pool and the variable 'a' is a reference to it. When lines 4 and 5 are compiled, the existing “test�? instance in the pool is reused, first as an argument to the String constructor, and then as the target for a second reference by 'c'.At runtime 'a' and 'c' are initialized to point to the instance of "test" in the pool .. but the 
```
new String()
```
 statement creates a new instance of String on the heap, which includes a place for its content, and 'b' is made to refer to it. Note that while the content of 'b' is filled with a copy of the "test" literal from the pool, it is a separate place in storage.Thus variables 'a' and 'c' point to the same string literal in the pool, but 'b' points into the heap.
The comparisons thus evaluate as shown.

# & and | (#59693)
/root/Java & OO Fundamentals/Operators

The operators & and | always evaluate both operands.

- (x) True
- ( ) False

## Explanation



# && operator (#59694)
/root/Java & OO Fundamentals/Operators

The && operator will not evaluate the right operand if the left is false.

- (x) True
- ( ) False

## Explanation



# output after for loop (#59787)
/root/Java & OO Fundamentals/Flow Control

What all gets printed when the following code is compiled and run? Select the three correct answers.
```
01: public class Xyz {02:   public static void main(String args[]) {03:     for(int i = 
0; i < 
2; i++) {04:       for(int j = 
2; j >= 
0; j--) {05:         if(i == j) break;06:         System.out.println("i=" + i + " j=" + j);07:       }08:     }09:   }10: }
```


- [x] i=0 j=1 
- [ ] i=2 j=2
- [ ] i=2 j=1
- [ ] i=2 j=0
- [x] i=1 j=2
- [ ] i=1 j=1
- [ ] i=1 j=0 
- [x] i=0 j=2

## Explanation

Its basic loop iteration: 
first iteration of the outer loop: 0 , inner loop takes values 2, 1, 0.
Printed:
i=0 j=2
i=0 j=1
Next, inner loop (j) reaches value 0 , inner loop breaks before printing.
Next printed:
i=1 j=2, then inner loop breaks.
Next iteration on outer loop brings values to 2,2 which breaks inner loop on first iteration. 

# Operators (#59792)
/root/Java & OO Fundamentals/Operators

What is the output of the following code snippet?
```
1: int i = 
5; 2: 3: if (i++ < 
8 || i++ < 
10) {4:     if (i++ < 
8 || i++ < 
10) {5:        System.out.println(i);6:     } 7: }
```


- [x] 7

## Explanation

The || behave "short-circuiting" (the second operand is evaluated only if needed). 

# Increment Operator (#59905)
/root/Java & OO Fundamentals/Operators

Consider the following code:
```
1: 2: int x, y, z;3: 4: y = 
1;5: z = 
5;6: x = 
0 - (++y) + z++;
```
After execution of this, what will be the values of x, y and z?

- ( ) x = 4, y = 2, z = 6
- ( ) x = -7, y = 1, z = 5
- (x) x = 3, y = 2, z = 6
- ( ) x = 4, y = 1, z = 5

## Explanation

Both y and z get incremented as a result of the last statement, but y gets incremented before and z after the assignment of the calculated value to x.

# class (#60125)
/root/Java & OO Fundamentals/Classes and Objects

top level class can be private or protected

- ( ) True
- (x) False

## Explanation

A top level class can not be private or protected. It can have either "public" or no modifier. If it does not have a modifier it is supposed to have a default access.If a top level class is declared as private the compiler will complain that the "modifier private is not allowed here". This means that a top level class can not be private. Same is the case with protected

# Out of memory in Java applications (#60175)
/root/Java & OO Fundamentals/Garbage Collection

Java applications cannot run out of memory causing stack overflow because of garbage collection mechanism. Is that true?

- ( ) True
- (x) False

## Explanation

Garbage collector does not guarantee that the application will not run out of memory. The amount of memory on a computer and the amount of memory the application needs determine whether it will run out of memory.

# fundamentals (#60190)
/root/Java & OO Fundamentals/Methods


```
1: public class Yippee2 {2: 3:    static public void main(String [] yahoo) {4:       for(int x = 
1; x < yahoo.length; x++) {5:          System.out.print(yahoo[x] + " ");6:       }7:    }}
```
and the command line invocation:
java Yippee2 a b c
What is the result?

- ( ) a b
- ( ) b c
- (x) a b c
- ( ) Compilation fails.
- ( ) An exception is thrown at runtime.

## Explanation

http://download-llnw.oracle.com/javase/tutorial/essential/environment/cmdLineArgs.html
"The runtime system passes the command-line arguments to the application's main method via an array of Strings."
In Java arrays are 0-origin, so cause for cycle start from 1 first argument will not be printed.

# StringBuilder(String) constructor question2 (#60264)
/root/Java & OO Fundamentals/Variables

Samson works for StringBulldozer Tech. He writes the following class.
```
01: package com.BullDozerTech.Strings;02: public class QuesXXX {03:     private String companyName; 04:     public static void main(String... args){05:         QuesXXX qx = new QuesXXX ();06:         qx.bulldoze("Stringers");07:     }08:     public void bulldoze(String job)
  {09:         StringBuilder sb = new StringBuilder(companyName)10:         .append(" can bulldoze ").append(job); 11:         System.out.print(sb.toString());12:     }13: }
```
The code compiles. But when he executes the code a 
```
NullPointerException
```
 is thrown.Which of the following can Samson do to avoid 
```
NullPointerException
```
? (Answer all that applies)

- [x] a) Replace line 03 with the following...
```

  private String companyName = "BullDozerTech";
```

- [x] b) Replace line 09 with the following... 
```

  StringBuilder sb = new StringBuilder().append(companyName)
```

- [ ] c) Replace line 09 and 10 with the following...
```

  StringBuilder sb = new StringBuilder(companyName);
  sb.append(" can bulldoze ");
  sb.append(job);
```

- [ ] d) Replace line 06 with the following... 
```

  qx.bulldoze("Stringers");
  companyName = "BullDozerTech";
```


## Explanation

answers are a) and b)
The NullPointerException is thrown by the StringBuilder(String) constructor when it encounters a null argument.
a) initializes the instance variable companyName so that it is not null. This satisfies the constructor.
b) uses a different constructor that first creates an empty StringBuilder. Thus avoids the problem.
c) is incorrect because the problem is not in the chaining of the append() methods. Hence the problem is not resolved.
d) is incorrect because it initializes the companyName instance variable too late. The problem has already occurred by then.

# What is printed after running this code? (#6035)
/root/Java & OO Fundamentals/Operators


```
1: public class Test { 2:     public static void main(String[] args) { 3:      int a = 
2; 4:      int b = 
4; 5:      System.out.println( (a++) * (++b));6:     } 7: }
```


- (x) 10
- ( ) 15
- ( ) Runtime Error
- ( ) Compilation fails

## Explanation

`(a++)
=&gt; returns a and then increments,
`(++b)
=&gt; increments b and then returns,
so 
2 * 
5 = 
10.`

# What's the right output? (#60353)
/root/Java & OO Fundamentals/Methods


```
01: class Main {02:     public static void main(String args[]) {03:         A a = null;04:         a = new A();05:         a.in("cat");06:         a.fooout();07:     }08: }09: 10: class A {11: 12:     private String x = "dog";13:     private String y = "mouse";14: 15:     public A() {16:         x = "cat";17:     }18: 19:     public void in(String y) {20:         this.y = y;21:     }22: 23:     public void fooout() {24:         System.out.println(x + y); 25:     }26: }
```
What is the output if you run this code?

- ( ) catdog
- (x) catcat
- ( ) dogcat
- ( ) mousecat
- ( ) catmouse
- ( ) compile fails
- ( ) runtime exception

## Explanation


```
a = new A(); // x = "cat" , y = "mouse" a.in("cat"); // y = "cat"
```
So it prints out "catcat"

# comments form (#60529)
/Java (core)/Java SE - basic/Misc/Comments and JavaDoc

Which of the following are valid Java comments?

- [ ] 
```
\\ This is a comment.
```

- [x] 
```
/* This is a comment. */
```

- [x] 
```
/** This is a documentary comment. */
```

- [ ] 
```
\* This is a comment *\
```

- [x] 
```
// This is a comment.
```


## Explanation

Comments use slashes and not backslashes.

# Keywords (#60536)
/root/Java & OO Fundamentals/Naming

Which of the following are keywords or reserved words in Java? 

- [x] 
```
if
```

- [ ] 
```
then
```

- [x] 
```
goto
```

- [x] 
```
while
```

- [x] 
```
case
```


## Explanation

See: http://java.sun.com/docs/books/tutorial/java/nutsandbolts/_keywords.html

# Operators (#60556)
/root/Java & OO Fundamentals/Operators

Which of the following operators are called arithmetic operators?
```
1: =2: /3: %4: &&5: ()6: \\7: ||
```


- (x) /, %
- ( ) =, /, %
- ( ) %, &&, ()
- ( ) \\, ||
- ( ) ||
- ( ) =, ||
- ( ) /, %, &&

## Explanation

`Unary operators are: ++ -- + - ! ~ ()`Arithmetic operators are: * / % + -
Shift operators are: << >> >>>
Comparison operators are: < <= > >= instanceof == !=
Bitwise operators are: & ^ |
Short-circuit operators are: && ||
Conditional operators are: ?:
Assignment operators are: = "op="`

# if danel (#60608)
/Sun Certifications/SCJP (Java)

Which of the following is a valid expression that returns true?

- [x] 
```
"john".equals("john") 
```

- [ ] 
```
"john" = "john" 
```

- [ ] 
```
new String("john") == new String("john")
```


## Explanation

Only the first option will return true.
Second option is an invalid expression, although "john" == "john" would return true.
Third option creates two new Strings and will not compare with any String from the "String constant pool". Hence, return false.

# Garbage Collection (#607)
/root/Java & OO Fundamentals/Garbage Collection

By calling the gc() method of the System (i.e. System.gc()) class you will invoke the garbage collector. By using the gc() method you have ensured that inaccessible objects will get collected immediately.

- ( ) True
- (x) False

## Explanation

The answer is False. Garbage Collection can only be suggested to the JVM. You can never compel the JVM to immediately remove old objects.

# String array (#60874)
/root/Java & OO Fundamentals/Strings

Which of the following declare an array of string objects?

- [x] `String[ ] s;`
- [x] `String [ ]s;`
- [ ] `String[s]`
- [ ] `String [s]`
- [x] `String s[ ];`

## Explanation



# Naming (#60884)
/root/Java & OO Fundamentals/Naming

A legal identifier for a variable is also a legal identifier for a method or a class

- (x) True
- ( ) False

## Explanation

The rules for Java naming apply to ALL Java components.

# Boolean comparisons (#60947)
/root/Java & OO Fundamentals/Operators


```
 Boolean b1 = new Boolean(true);Boolean b2 = new Boolean(true);
```
 Which of the following expressions (as of Java 5) will evaluate to 
```
true
```
?

- [ ] b1 == b2 
- [x] b1.equals(b2) 
- [x] b1 && b2 
- [x] b1 || b2 

## Explanation

The 1st option will return false because we compare two instances of the Boolean object.
The other options are good because we compare Boolean values (3 and 4 use autoboxing - a feature of Java 5).

# Check for Output (#610)
/root/Java & OO Fundamentals/Variables

What will be the output of the following code?
```
1: int m = 
10;2: double j = 
20;3: boolean ij = true;4: System.out.println(m + j + ij);
```


- ( ) true
- ( ) false
- (x) compilation error
- ( ) 30.0 true
- ( ) 20 10.0 true

## Explanation

Boolean and int values cannot be added.

# Basic switch (#61020)
/root/Java & OO Fundamentals/Flow Control

What is the result of this block of code?
```
01:  02: int forSwitch = 
1;03: switch (forSwitch) {04:   case 
1:05:     System.out.println("one");06:   case 
2:07:     System.out.println("second");08:   default:09:     System.out.println("default");10: }
```


- ( ) one
second
- (x) one
second
default
- ( ) one
- ( ) one
default
- ( ) second

## Explanation

If there is no break; after the code in case body, the execution continues to the next case body

# Memory leak (#61027)
/root/Java & OO Fundamentals/Garbage Collection

Since Java has an automatic Garbage Collector it is not possible to have memory leaks.

- ( ) True
- (x) False

## Explanation

Even thought garbage collection is automatic, note that only objects which are not referenced by a live thread are candidates for garbage collection. If care isn't taken to ensure there are no references to unused objects lying around they will pile up and eventually use up all the memory causing a memory leak.

# Default value (#61041)
/root/Java & OO Fundamentals/Variables

Choose the default value of 
```
boolean
```
 data type:

- ( ) True
- (x) False

## Explanation

For type 
```
boolean
```
, the default value is 
```
false
```
.See JLS: http://java.sun.com/docs/books/jls/third_edition/html/typesValues.html#4.12.5

# Java Properties (#61090)
/root/Java & OO Fundamentals/Properties

What is the result of running the following piece of code?
```

1: import java.io.FileNotFoundException;
2: import java.io.IOException;
3: import java.util.Properties;
4: 
5: public class TestProp {
6:
public static void main(String[] args) 
7:
throws FileNotFoundException, IOException {
8:
    Properties props = new Properties();
9:
    props.put("firstName", "John");
10:
       props.put("lastname", "Smith");
11:
       props.put("age", "30");
12:
       props.put("career", "Programmer");
13:
       System.out.println(props.getProperty("firstName"));
14:
       System.out.println(props.getProperty("CAREER"));
15:
       System.out.println(props.getProperty("age"));
16:
       System.out.println(props.getProperty("LASTNAME"));
17:
   }
18: }
```


- ( ) John
Programmer
30
Smith
- ( ) RuntimeException is thrown
- (x) John
null
30
null
- ( ) Code does not compile
- ( ) Smith
Programmer
30
John
- ( ) null
Programmer
30
John
- ( ) Smith
null
30
null

## Explanation

The correct answer is that the code compiles and runs and displays the following on the console:
John
null
30
null
Reason: getProperty(String key) returns null if the key is an invalid property

# Local Variables (#61198)
/root/Java & OO Fundamentals/Variables

Which of the following modifiers can be used for local variables?

- (x) final
- ( ) static
- ( ) protected
- ( ) public
- ( ) native
- ( ) None of the above

## Explanation

Local variables may only have the 
```
final
```
 modifier.

# Encapsulation (#61217)
/root/Java & OO Fundamentals/Encapsulation

what is the result of the following code?
```
 public class A{
public int num;
private int num1;}public class B extends A{
public static void main(String[] args){
          B b = new B();
   System.out.println(b.num);
   System.out.println(b.num1);}
```


- ( ) Runtime exception
- ( ) 0
0
- ( ) 0
Runtime exception
- (x) compilation error

## Explanation

class B cannot access to private instance variable of class A.
the statement: 
```
 System.out.println(b.num1);
```
will cause a compile error.

# What is the correct syntax of a javadoc comment ? (#61252)
/root/Java & OO Fundamentals/Javadoc

What is the correct syntax of a javadoc comment ?

- (x) /** This is a javadoc comment. */
- ( ) // This is a javadoc comment
- ( ) /*@ This is a javadoc comment. */
- ( ) /*@ This is a javadoc comment. @*/
- ( ) /* This is a javadoc comment. */

## Explanation

Javadoc comments start with /** and end with */.

# Local variable scope (#61345)
/root/Java & OO Fundamentals/Scope


```
01: public class Foo{02:    public static void main(String[] args) {03:       /* First */04:       int[] numbers = { 
1, 
3, 
5, 
7, 
9 };05:       for (long item : numbers) 06:          System.out.println("Number is: " + item);07:       /* First  */08: 09:       /* Second */10:       long item;11:       int[] numbers2 = { 
2, 
4, 
6, 
8, 
10 };12:       for (long item : numbers2)13:          System.out.println("Count is: " + item);14:       /* Second */15:    }16: }
```
Choose one correct statement:

- ( ) Code will compile
- ( ) There is an error in 'First' part
- (x) There is an error in 'Second' part
- ( ) Other

## Explanation

Item variable is duplicated in the same scope.

# Class field and method name clash (#61378)
/root/Java & OO Fundamentals/Naming

It is possible for a class to declare a field named $ (dollar sign) and a method named $ (dollar sign) at the same time.

- (x) True
- ( ) False

## Explanation

$ (dollar sign) is a valid Java identifier. Also it is absolutely valid for a field to have the same name as method.

# find Java bytecode file extension (#61467)
/root/Java & OO Fundamentals/Platform

Which of the following is/are correct Java bytecode file extension(s)?

- [ ] .java
- [ ] .javac
- [ ] .bcode
- [x] .class
- [ ] .jclass
- [ ] .jre

## Explanation

The correct answer is ".class"
For further information please see (http://en.wikipedia.org/wiki/Class_(file_format))

# Variable initialization (#61468)
/root/Java & OO Fundamentals/Variables

Which line/s fail to compile?
```
01: class Vars {02:     String a;03:     int b;04:     int c;05:     06:     public void showValues(int c) {07:         String d;08:         09:         System.out.println(a);10:         System.out.println(b);11:         System.out.println(c);12:         System.out.println(d);13:     }14: }
```


- [ ] line 6
- [ ] line 7
- [ ] line 9
- [ ] line 11
- [x] line 12
- [ ] It does compile

## Explanation

Local variables must be initialized before using them

# Legal & Ilegal Identifiers (#61490)
/root/Java & OO Fundamentals/Variables

Identify the illegal identifiers from the below options. Select all that apply. Consider Java 5 for answering.

- [ ] int _____2_w;
- [ ] int _$;
- [x] int enum;
- [ ] String boolean6;
- [x] double .d;

## Explanation

Identifiers must start with a letter, a currency character($), or a connecting character such as the underscore( _ ). Java Keyword can't be used as an identifier. enum is a keyword in Java 5.

# String Pool (#61519)
/root/Java & OO Fundamentals/Strings


```
01: public class StringPool {02: 03:     public static void main(String[] args) {04:         String s1 = "1234";05:         String s2 = s1;06:         String s3 = new String("1234");07:         String s4 = s2.toString();08: 09:     }10: }
```
Which of the following statements are true?

- [x] s1==s2;
- [ ] s2==s3;
- [x] s4==s1;
- [x] s2.equals(s3);

## Explanation



# Modifiers (#61606)
/root/Java & OO Fundamentals/Platform

Select from these all the modifiers that apply to top-level classes (not nested).

- [ ] private
- [x] final
- [ ] static
- [x] abstract
- [ ] transient
- [x] public
- [ ] protected
- [ ] volatile

## Explanation

see: http://www.javacamp.org/javaI/Modifier.html

# Differentiate the purpose of the JDK and the JRE (#61947)
/root/Java & OO Fundamentals/Platform

JRE is development kit that enables users to write their own Java programs while JDK is a runtime environment for Applets and running Java code.

- ( ) True
- (x) False

## Explanation

JDK, Java Development Kit, allows for development of Java programs.
JRE, Java Runtime Environment, runs java programs and/or browses Applets on the web.

# Consider the following code: (#61984)
/root/Java & OO Fundamentals/Scope


```
01: public class TestClass {02:    public static void main(String[] args) {03:       int i = 
9;04:       add(i);05:       System.out.println(--i);06:    }07: 08:    public static int add(int i) {09:       ++i;10:       return i += 
1;11:    }12: }
```
After execution of this, what will be the value of i?

- ( ) 10
- ( ) 11
- (x) 8
- ( ) 9
- ( ) 7
- ( ) 12

## Explanation

The value of i will be 8. While returning from the add method no assignment was done to i and because i is a primitive it passes to the add function by value and not by reference.

# Short circuit feature for Logical Operators (#62031)
/root/Java & OO Fundamentals/Operators

What will be printed if Java code below is executed?
```
1:  public static void main(String args[]) {2:         int i = 
10;3:         int j = 
11;4:         int k = 
12;5:         boolean trueorfalse = ((i < j) && (i++ < j) && (++i < k) && (--i > j));6:         System.out.println(trueorfalse);7:         System.out.println(i);8: }
```


- ( ) false
11
- ( ) true
11
- (x) false
12
- ( ) true
12
- ( ) false
13

## Explanation


```
i<j
```
 is evaluated as 
```

10<
11
```
. This returns true.
```
i++<j
```
 is evaluated as 
```

10<
11
```
 (since it is post-increment for i). This also returns true.i value now is 11.
```
++i<k
```
 is evaluated as 
```

12<
12
```
 (since it is pre-increment for i). This will return false, since 12 is equal to 12.Expression would result "false", regardless of final condition evaluation. The && operator does not evaluate the second expression if the first one evaluate to "false". This is called Short-circuiting and is opposed to the operator & that evaluate both expression regardeless of their value.
Output will be:
False
12

# What is the output of a program? (#62131)
/root/Java & OO Fundamentals/Strings

What will be the output of the following code?
```
01: public class StrBld {02: 03:     public static void main(String[] args) {04:         String str = new String("abc");05:         StringBuilder stb = new StringBuilder(str);06: 07:         if (str.equals(stb.toString())) {08:             System.out.println("true");09:         } else {10:             System.out.println("false");11:         }12: 13:         if (str.equals(stb)) {14:             System.out.println("true");15:         } else {16:             System.out.println("false");17:         }18:     }19: }
```


- ( ) true
true
- ( ) false
false
- (x) true
false
- ( ) It will not compile
- ( ) Runtime exception

## Explanation

http://download.oracle.com/javase/1.5.0/docs/api/java/lang/StringBuilder.html

# Scope basics (#62137)
/root/Java & OO Fundamentals/Scope

What will be the output of the following method:
```
public static void main( String[] args ) {
  int x = 
15;
  for(int x=
1;x<
5;x++){
      System.out.println(x);
  }
  System.out.println(x);}
```


- ( ) 123415
- ( ) 12344
- ( ) 12345
- ( ) Exception will be thrown while runtime
- (x) Code will not compile

## Explanation

You cannot declare two variables with the same name in one scope.

# Access specifiers (#62142)
/root/Java & OO Fundamentals/Packages

Class "Foo" resides in package "com.foo" and contains methods with the following declarations:
 a. final String getName()
 b. protected final String getDescription()
 c. private String getCode()
 d. synchronized String getFilename()
 e. String getID()
Class "Bar" extends "Foo" and resides in package "com.foo.bar".
Referring to the scenario above, which one of the following methods of Foo is accessible to class Bar?

- ( ) Method a
- (x) Method b
- ( ) Method c
- ( ) Method d
- ( ) Method e

## Explanation

Because method b has protected access, it is accessible to subclasses outside the package.

# Is Java bytecode a machine code? (#62153)
/root/Java & OO Fundamentals/Platform

Java bytecode is executed directly by the CPU.

- ( ) True
- (x) False

## Explanation

Java bytecode is executed on Java Virtual Machine (JVM), and is not machine code.

# Trim (#62154)
/root/Java & OO Fundamentals/Strings

What method in the java.lang.String class allows you to remove all blank spaces at the beginning and the end of a String?

- [x] \s*(((java\s*\.)?lang\s*\.)?String\s*\.)?trim(\(\s*\)(\s*;)?)?\s*

## Explanation

`&lt;b&gt;java.lang.String.trim()&lt;/b&gt; can be used to remove leading and trailing whitespace.`Reference:
http://java.sun.com/j2se/1.5.0/docs/api/java/lang/String.html#trim%28%29`

# Meaning of the size() method of ArrayList (#62156)
/Java (core)/Java SE - basic/Misc/Collections

The 
```
size()
```
 method of 
```
ArrayList
```
 returns:

- (x) The number of elements currently in an ArrayList object.
- ( ) The current length of the array minus 1.
- ( ) The number of lists in the array.
- ( ) The number of lists used in the javadoc.
- ( ) The maximum capacity of an ArrayList object.
- ( ) 
```
ArrayList
```
 does not provide the 
```
size()
```
 method.

## Explanation

Returns the number of elements in the list.
Taken directly from the method description at:
http://java.sun.com/javase/6/docs/api/java/util/ArrayList.html#size()

# What will be the output of the following code? (#62162)
/root/Java & OO Fundamentals/Operators

What will be the output of the following code?
```
String a = "String";int b = 
3;int c = 
7;System.out.println(a + b + c);System.out.println(a + (b + c));
```


- ( ) String10
String10
- ( ) String37
String37
- (x) String37
String10
- ( ) String10
String37

## Explanation



# use a class that has no package from a class that (#62163)
/root/Java & OO Fundamentals/Classes and Objects

Is it possible to use a class defined in the default nameless package from a class defined in a different named package ? (without reflection)

- ( ) True
- (x) False

## Explanation

It is simply not allowed (the default, also known as package-private).

# Uninitialized variables (#62164)
/root/Java & OO Fundamentals/Variables

What is the result of compiling and running the following program?
```
1:  2: public class Test {3:     public static void main(String... args){4:         int x,y = 
2;5:         System.out.println(x + y);6: 7:     }8: }
```


- ( ) 02
- ( ) 2
- ( ) 22
- ( ) 4
- (x) Code does not compile

## Explanation

Code does not compile because variable x is not initialized!

# Continue Statement (#62165)
/root/Java & OO Fundamentals/Flow Control

The 'continue' statement causes execution to jump:

- ( ) out of a loop.
- (x) to the end of the current iteration of a loop.
- ( ) to the beginning of the program.
- ( ) out of an if statement.

## Explanation

A continue statement may occur only in a while, do, or for statement; statements of these three kinds are called iteration statements. Control passes to the loop-continuation point of an iteration statement.

# The if-then Statements with Bitwise exclusive OR (#62172)
/root/Java & OO Fundamentals/Operators

What is the output when you compile and run the following block of code?
```
01: 02: public static void main(String[] args) {03:         boolean a = true;04:         boolean b = !a;05:         boolean c = false;06:         c |= a;07:         int sum = 
0;08:         if(a ^ b)09:             sum++;10:         if(c = (!c ^ b ^ a))11:             sum += 
10;12:         if(!a)13:             sum++;14:         System.out.println(sum);15:         16:     }
```


- ( ) 0
- ( ) 1
- (x) 11
- ( ) 10
- ( ) 12

## Explanation

& Bitwise AND
^ Bitwise exclusive OR
| Bitwise inclusive OR
++ Increment operator; increments a value by 1
! Logical compliment operator; inverts the value of a boolean

# Garbage Collection (#62173)
/root/Java & OO Fundamentals/Garbage Collection

The Garbage Collector Thread is a low priority daemon Thread.

- (x) True
- ( ) False

## Explanation

Yes,gc Thread is low priority Thread.

# Importing classes (#62175)
/Java (core)/Java SE - basic/Misc/Files and Packages

What is the correct ordering for the import, class and package declarations when found in a single file? Select the correct answer.

- (x) package, import, class
- ( ) class, import, package
- ( ) import, package, class
- ( ) package, class, import

## Explanation

The correct ordering is package, import and class.

# Where are the compiler errors? (#62179)
/root/Java & OO Fundamentals/Naming

What happens if you run the code below?
```
01: public class blackbelt{02:     public static void main(String[] args) {03:     String new = "My new text";04:     String string = "I will be a string";05:     String will_I_Really_Work = "What do you think?";06:     String will_I_Really_Work_2 = "What about me?";07:     String 3_will_I_Really_Work = "And me?";08:     Boolean public = true;09:     Object instanceOf = new Object();10:     System.out.println("Done");11:     }12: }
```


- [x] Compile Error in line 3
- [ ] Compile Error in line 4
- [ ] Compile Error in line 5
- [ ] Compile Error in line 6
- [x] Compile Error in line 7
- [x] Compile Error in line 8
- [ ] Compile Error in line 9
- [ ] None of them, it will run and print "Done".

## Explanation

`Line 
3 and 
8 will bring compiler errors because &lt;b&gt;new&lt;/b&gt; and &lt;b&gt;public&lt;/b&gt; are Java keywords. &lt;b&gt;instanceOf&lt;/b&gt; is allowed because keywords are always lowercase, so this wont be counting as keyword.`Line 
7 brings the compiler error because you cant start with numbers in the naming.`

# Package declaration in Class (#62365)
/root/Java & OO Fundamentals/Naming

If the class is part of a package, the package statement must be in?.

- ( ) anywhere in the source code file.
- ( ) before class declaration after imports.
- (x) the first line in the source code file, before any import statements that may be present.

## Explanation

If the class is part of a package, the package statement must be the first line
in the source code file, before any import statements that may be present.

# method (#62372)
/root/Java & OO Fundamentals/Methods

What is the result of the following code snippet?
```
1: class Test1 {2:     int a=
0;3:     public static void main(String[] args) {4:         System.out.println(++a);5:     }
 6: }
```


- (x) compile error will occur
- ( ) runtime error will occur
- ( ) 1

## Explanation

non-static variable a cannot be referenced from a static context.

# == operator application to objects (#62382)
/OO /OO with Java - basic/Object and Class

References 
```
a
```
 and 
```
b
```
 point to the same instance of class 
```
XYZ
```
. What will 
```
a == b
```
 evaluate to?

- (x) True
- ( ) False

## Explanation

a==b compares two object references to see whether they refer to same instance.
This statement will be true if references a and b reference to the same instance. For example: 
```

  A a = new A();
  A b = new A();
  // now a==b is false , but..
  a=b;
  //now a==b is true!!! 
```


# private methods (#62392)
/root/Java & OO Fundamentals/Classes and Objects

It's possible to override private methods?

- ( ) True
- (x) False

## Explanation

No, private methods cannot be seen by subclasses so they cannot be overridden. Subclasses can, however, define a method which has the same name and return type (the same "signature") as the private method in the superclass. Although you might think you're overriding the private method, in actuality you are creating an entirely new method which has nothing to do with the method of the same signature in the superclass.

# What is the name of the java file ? (#62397)
/root/Java & OO Fundamentals/Classes and Objects

What is the name of the java file ?
```
import myLibrary.*;public class ShowSomeClass{// code for the class...}
```


- [ ] myLibrary.java
- [x] ShowSomeClass.java
- [ ] ShowSomeClass
- [ ] ShowSomeClass.class

## Explanation



# JVM (#62399)
/root/Java & OO Fundamentals/Platform

A JVM can not be used to implement programming languages other than Java. 

- ( ) True
- (x) False

## Explanation

A JVM can also be used to implement programming languages other than Java. For example, Ada source code can be compiled to Java bytecode, which may then be executed by a JVM. 

# Float and Double (#62424)
/root/Java & OO Fundamentals/Variables

Select the invalid assignment statements from the following:
```
(A) float x = 
238.88;(B) double y = 
0x443;
```


- (x) A only
- ( ) B only
- ( ) A & B
- ( ) Both are Valid.

## Explanation


```

238.88
```
 is a double in Java. To assign this value to a float, 
```

238.88f
```
 must be used. A variable of type boolean cannot be converted to an int in Java.

# Default Value of Char (#62491)
/root/Java & OO Fundamentals/Variables

If not assigned a value, a variable of type char has the following default value: 

- ( ) 
```
'\uffff'
```

- (x) 
```
'\u0000'
```

- ( ) 
```
" "
```
 (space)
- ( ) 
```
'\u0001'
```


## Explanation

The value of a variable of type char is 16 bits of data formatted as a Unicode character.

# return intValue (#62501)
/root/Java & OO Fundamentals/Variables

Select the correct answer. Which method defined in Integer class can be used to convert an Integer object to primitive int type.

- ( ) valueOf
- (x) intValue
- ( ) getInteger
- ( ) getInt
- ( ) initInt

## Explanation

See http://java.sun.com/j2se/1.4.2/docs/api/java/lang/Integer.html

# Override static methods (#62503)
/root/Java & OO Fundamentals/Platform

Can you override a static method?

- ( ) True
- (x) False

## Explanation

Static method means one method per class, not one for each object. 
This means that you can use them without creating an instance of a class. Static methods are implicitly final, because overriding is done based on the type of the object, and static methods are attached to a class, not an object.
A static method in a superclass can be shadowed by another static method in a subclass, as long as the original method was not declared final. However, you cannot override a static method with a non-static method. In other words, you cannot change a static method into an instance method in a subclass.

# Understanding Primitives (#62549)
/root/Java & OO Fundamentals/Variables

You need to create an application that is used to calculate the attendance at a baseball game.
What data type would be most appropriate for storing the attendance?

- ( ) boolean
- ( ) char
- ( ) float
- (x) int

## Explanation

The attendance of a baseball game is going to be a whole number within the range of an
int.

# Java program execution. (#62577)
/root/Java & OO Fundamentals/Platform

Command to execute a compiled java programs is.

- ( ) run
- ( ) execute
- (x) java
- ( ) javac

## Explanation

The java tool launches a Java application. It does this by starting a Java runtime environment, loading a specified class, and invoking that class's main method.

# Understanding Primitives (#62642)
/root/Java & OO Fundamentals/Variables

You are writing a class that will store the status of an on/off switch. Which data type is most
appropriate to store this value?

- (x) boolean
- ( ) char
- ( ) float
- ( ) int

## Explanation

A boolean primitive is used to store true or false which can be applied to a switch.

# Compile and Run (#62686)
/root/Java & OO Fundamentals/Classes and Objects

Given:
```
01: public class Boxer1{02:     Integer i;03:     int x;04:     public Boxer1(int y) {05:         x = i+y;06:         System.out.println(x);07:     }08:     public static void main(String[] args) {09:         new Boxer1(new Integer(
4));10:     }11: }
```
 What is the result?

- ( ) A. The value "4" is printed at the command line.
- ( ) B. Compilation fails because of an error in line 5.
- ( ) C. Compilation fails because of an error in line 9.
- (x) D. A NullPointerException occurs at runtime.
- ( ) E. A NumberFormatException occurs at runtime.
- ( ) F. An IllegalStateException occurs at runtime.

## Explanation

i is declared as an instance of the class Integer, no value is assigned, so by default it is null. So a NullPointerException will be thrown at line 5

# Verify whether Java code is portable between OS (#62701)
/root/Java & OO Fundamentals/Platform

Suppose that you have a typical Java "Hello World!" program and compile it using JDK 1.5 on a Linux x86 machine. You take the compiled program and try to run it on a Windows x86 machine with JRE 1.5 installed. Will the program run?

- (x) True
- ( ) False

## Explanation

Yes, because the compiled bytecode is executed on a JVM (Java Virtual Machine), not the physical machine. The host's operating system does not affect the code portability, as long as there is a suitable Java runtime available for the target OS.

# A .java file (#62718)
/root/Java & OO Fundamentals/Platform

A .java file can contain more than one Java class.

- (x) True
- ( ) False

## Explanation

Yes, you can have more than one class per each file. However only one of these classes can be marked as "public". This also means that the .java file has to have the same name as the name of the only public class.

# Java comment (#62720)
/root/Java & OO Fundamentals/Comments

Is it possible to comment a line like this?
/// some code;

- (x) True
- ( ) False

## Explanation

Only the first 2 chars count!

# Null value (#62730)
/root/Java & OO Fundamentals/Variables

Null value can be assigned to all variable type.

- ( ) True
- (x) False

## Explanation

null can't be assigned to primitive types

# substring (#62742)
/root/Java & OO Fundamentals/Strings

If you run the code below, what gets printed out ? 
```
1: String s = new String("Bicycle");2: int iBegin = 
1;3: char iEnd = 
3;4: System.out.println(s.substring(iBegin, iEnd));
```


- ( ) Bic
- (x) ic
- ( ) icy
- ( ) error: no method matching substring (int,char)

## Explanation

Returns a new string that is a substring of this string. The substring begins at the specified beginIndex and extends to the character at index endIndex - 1. Thus the length of the substring is endIndex-beginIndex. 
API Reference:
http://download.oracle.com/docs/cd/E17476_01/javase/1.5.0/docs/api/java/lang/String.html#substring%28int,%20int%29

# Java platform compatibility (#62752)
/root/Java & OO Fundamentals/Platform

Java only runs on Solaris and Linux.

- ( ) True
- (x) False

## Explanation

It runs on several more operating systems

# Which of the following is the correct syntax for s (#62756)
/root/Java & OO Fundamentals/Garbage Collection

Which of the following is the correct syntax for suggesting that the JVM performs garbage collection?

- ( ) System.free();
- ( ) System.setGarbageCollection();
- ( ) System.out.gc();
- (x) System.gc();

## Explanation

System.gc();
Calling the gc method suggests that the Java Virtual Machine expend effort toward recycling unused objects.

# For loop with no content - equivalent (#62822)
/root/Java & OO Fundamentals/Flow Control

The following loop will compile and run fine.
What is a suitable 'while' equivalent for this?
```
 for( ; ; ){
 System.out.println("test");}
```


- ( ) while(1)
{
 System.out.println("test");
}
- ( ) while()
{
 System.out.println("test");
}
- (x) while(true)
{
 System.out.println("test");
}
- ( ) while(false)
{
 System.out.println("test");
}
- ( ) while( ; ; )
{
 System.out.println("test");
}

## Explanation

The for loop will execute continuously until the possibility of running out of memory.
Therefore the while loop should also run continuously.
The first answer is incorrect as in java 1 cannot be read as a boolean type.
The second answer is incorrect as while statements require conditions.
The third answer is CORRECT as true will always be true so it shall run continuously.
The fourth answer is incorrect because the loop should run as long as the condition is true. The condition here starts as false so the loop will never be entered.
The fifth answer is incorrect because while loops do not have the same (initialise;compare;increment) structure as for loops.

# Primitive type (#62826)
/root/Java & OO Fundamentals/Platform

Java has four primitive integer storage types:

- ( ) Unsigned long, long, unsigned int, int
- ( ) long, int, short, unsigned short
- (x) long, int, short, byte
- ( ) double, float, long, int

## Explanation

 The four primitive integer data types supported by the Java programming language are: long, int, short, byte; 
 double, float are floating point types;
 boolean is false and true type;
 char is Unicode characters type;

# Platform Independency (#62850)
/root/Java & OO Fundamentals/Platform

Java can run on any Operating System providing the Java Runtime Environment is successfully installed

- (x) True
- ( ) False

## Explanation

Yes it can!
Any OS which can support the JRE can run Java. The language is platform independent in this respect.

# Java bytecode. (#62866)
/root/Java & OO Fundamentals/Platform

Java bytecode is a compiled native code for specific platform e.g Linux, which cannot be run on different OS e.g Windows?

- ( ) True
- (x) False

## Explanation

Java language is platform independent. If JVM is provided, once compiled bytecode can be run on different platforms.

# default value (#62891)
/root/Java & OO Fundamentals/Variables

What will be the output if you compile and run the following code?
```
1:  2: public class MyClass{3:     static int i;4:     public static void main(String arg[]){5:         System.out.println(i);6:     }7: }
```


- ( ) Error variable that may not be initialized
- ( ) null
- ( ) 1
- (x) 0

## Explanation

default value of int data type is zero.
http://download-llnw.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html

# Variable Scope (#62911)
/root/Java & OO Fundamentals/Scope


```
1: public static void main(String[] args) {2:     int x, y = 
10;3:     {4:         x = 
8;5:         int z = x + y;6:     }7:     System.out.println("x = " + x + ", z = " + z);8: }
```
What is the output?

- ( ) x = 8, z = 18
- ( ) x = 0, z = 18
- ( ) x = null, z = 18
- (x) The code does not compile
- ( ) It throws a runtime exception

## Explanation

The variable z is defined in block. It won't be recognized outside the block. 

# Casting (#63004)
/root/Java & OO Fundamentals/Variables

What is the result of the following code?
```

6. byte x = 
23, y = 
4;
7. int z = 
23 % 
4;
8. System.out.println(z);
```


- (x) A. 3
- ( ) B. 4
- ( ) C. 4.75
- ( ) D. Compiler error on line 6
- ( ) E. Compiler error on line 7

## Explanation

A. The code compiles fine, so D and E are incorrect. 
The value of z is the remainder of 23 divided by 4, which is 3. 
Therefore, the answer is A.

# jvm (#63312)
/root/Java & OO Fundamentals/Platform

True or false: the JVM itself is platform dependent.

- (x) True
- ( ) False

## Explanation

While the Java byte code will run on any compatible JVM regardless of platform, the JVM itself is written to run on a particular system. Therefore the JVM itself is platform-dependent.

# Instance Variables (#63319)
/root/Java & OO Fundamentals/Variables

Instance variables are defined inside the class and outside of the methods present in that same class.

- (x) True
- ( ) False

## Explanation

There are two basic scopes for variables: 
1. instance (or 'class-level') variables
2. local (or 'method') variables
Instance variables are defined inside of the class but outside of any methods.
Local variables are defined inside of a method, and potentially inside a smaller block of code such as a for loop.

# String comparison (#63613)
/root/Java & OO Fundamentals/Strings

Given the following code, please choose the correct code to substitute to declaration so the program will run correctly AND print Equals on the screen.
```
public class StringComparison {
  public static void main(String[] args) {
      String firstString;
      String secondString = null;
              firstString = "I like to swim in the pool";
      secondString = new String("I like to swim in the pool");
```
if (declaration) {
```

          System.out.println("Equals");
      } else {
          System.out.println("Not Equals");
      }
          }}
```


- ( ) firstString = secondString
- ( ) firstString == secondString
- (x) firstString.equals(secondString)
- ( ) firstString.compareTo(secondString)

## Explanation

`The &lt;b&gt;correct&lt;/b&gt; answer is: firstString.equals(secondString) will complete the code and compile succesfully. You are comparing a String that is in the &quot;pool&quot; and a String created as an instance.`The answer: firstString = secondString will produce a compilation error because you cannot convert from String to boolean.
The answer: firstString == secondString will compile succesfully but will print &quot;Not Equals&quot; because you are comparing a String that is in the &quot;pool&quot; and a String created as an instance.
The answer: firstString.compareTo(secondString) will produce a compilation error because you cannot convert from into to boolean.
Reference:
http://download.oracle.com/javase/6/docs/api/java/lang/String.html#equals(java.lang.Object)`

# Reference Variables (#63621)
/root/Java & OO Fundamentals/Variables

What is the size of a reference variable?

- ( ) 8 bits
- ( ) 4 bytes
- (x) it is JVM dependent.
- ( ) it can be determined by using sizeof() method.

## Explanation

the size of reference variable is jvm dependent. It depends on the implementation of a particular jvm.

# Overload Constructors (#63635)
/root/Java & OO Fundamentals/Platform

Constructors can be overloaded.

- (x) True
- ( ) False

## Explanation

It's common to overload constructors - define multiple constructors which differ in number and/or types of parameters.
http://leepoint.net/JavaBasics/oop/oop-45-constructor-overloading.html

# Java Beans getters convention (#63703)
/root/Java & OO Fundamentals/Properties

Considering the Java Beans naming convention and JVM > 1.4, choose the correct signature of the getters (accessors) methods:

- [x] public int getHeight() {...}
- [ ] Integer getHeight() {...}
- [ ] public int isHeight() {...}
- [ ] public boolean getAdult() {...}
- [ ] public Boolean isAdult() {...}
- [x] public boolean isAdult() {...}
- [x] public Boolean getAdult() {...}

## Explanation

All getter (accessor) methods must be public and the name should start with the "get" word (1 and 4 are correct). 
The only exception from this rule is the boolean primitive, which accessor's name can start with the "is" word (6 is correct).
Note that the Boolean is not a primitive; it is treated as an Object, therefore the "is...()" form is not allowed in this case.

# Scope (#63816)
/root/Java & OO Fundamentals/Scope


```
01: public class MyTest { 02:     private static int value = 
100;03:         04:     public static void main(String... args) {05:         increase(value);06:         System.out.println(value);07:     }08:     09:     private static void increase(int value) {10:         value += 
200;11:     }12: }
```
What is the output?

- ( ) 300
- ( ) 200
- (x) 100
- ( ) It throws an exception
- ( ) The code doesn't compile

## Explanation

`The variable &lt;i&gt;value&lt;/i&gt; in the method &lt;i&gt;increase&lt;/i&gt; refers to the method's parameter, not the static variable. The method &lt;i&gt;increase&lt;/i&gt; doesn't change the value of the static variable &lt;i&gt;value&lt;/i&gt;`

# java control and scope (#63975)
/Java (core)/Java SE - basic/Language Elements/Control Structures

What happens when we place this code into a 'main' method:
```
01: int i = 
5;02: long k = 
5L;03: if (i == 
5) {04:     int o = 
5;05:     if (o == i) {06:         System.out.println("i equals o");07:     }08: } else if (k == o) {09:     System.out.println("k equals o");10: }
```


- ( ) The code won't compile because you can't compare long and int.
- ( ) java will print text on the console:
i equals o
- (x) The code won't compile because of variables scope.
- ( ) java will print text on the console:
k equals o

## Explanation

The line:
```
} else if ( k == o ){
```
will not compile because o was defined in a different, non-parent scope.

# CaseSensitivity (#64113)
/root/Java & OO Fundamentals/Naming

Which of the following lines are valid declarations of the main() method?

- [x] `public static void main(String[] args)`
- [ ] `public static void Main(String[] args)`
- [ ] `public static void Main(String[] Args)`
- [x] `public static void main(String[] Args)`

## Explanation

Since Java is case sensitive, the keyword main must be written in lower case. So (2) and (3) are not valid declarations of the main method. 
Variable names should be written in lower case, such that they follow the coding conventions, but this is not a necessity. Hence both (1) and (4) are valid declarations of the main method.

# && operator (#64290)
/root/Java & OO Fundamentals/Operators

Consider that you have two boolean variables : 
```
a = true
```
 and 
```
b = false
```
.
```
1: 2: if(b && a)3: {4:        // some code here5: }
```
If you execute this code in a functional program, the variable 
```
a
```
 is never read in the 
```
if
```
 statement.

- (x) True
- ( ) False

## Explanation

With the logical operator &&, when the left operand invalidates the statement, the right hand is never read. It allows to optimize code to run faster.

# Html in Javadoc (#64340)
/root/Java & OO Fundamentals/Javadoc

It's impossible to use HTML tags when writing javadoc-style comments.

- ( ) True
- (x) False

## Explanation

False. You can use HTML tags when writing javadoc-style comments to improve the readability of the document.

# method signature (#64372)
/root/Java & OO Fundamentals/Methods

Consider this method :
```
public double add(int number1, int number2, double decimal, String name) {//some code}
```
The signature of this method is :

- ( ) public double add(int, int, double, String)
- ( ) public add(int, int, double, String)
- ( ) double add(int, int, double, String)
- (x) add(int, int, double, String)
- ( ) double add(int number1, int number2, double decimal, String name)
- ( ) add(int number1, int number2, double decimal, String name)
- ( ) None of the above

## Explanation

`The signature of a method is defined by its name and its arguments in the &lt;u&gt;same order&lt;/u&gt; without their names.`

# Threads Please select the category you'd like to m (#64419)
/root/Java & OO Fundamentals/Classes and Objects

A thread wants to make a second thread ineligible for execution. To do this, the first thread can call yield() method on the second thread.

- ( ) True
- (x) False

## Explanation

The yield() method is static and always causes the current thread to yield. This causes the currently executing thread to move to the Ready state. If another thread is willing to run, then this will be executed otherwise if there are not other waiting threads, the yielded thread will get to continue immediately. 

# range of values (#6458)
/root/Java & OO Fundamentals/Variables

What are the range of values for a variable of type byte?

- ( ) +2^7 to (2^7)-1
- ( ) 0 to 2^8
- ( ) -2^8 to 2^8
- (x) -2^7 to (2^7)-1
- ( ) -2^8 to (2^8)-1

## Explanation

The byte data type is an 8-bit signed two's complement integer. It has a minimum value of -128(-2^7) and a maximum value of 127((2^7)-1) (inclusive). 

# Scope (#64679)
/root/Java & OO Fundamentals/Scope

What will the result of the following code be?:
```
01: 02: public class Test{03:    public static void main(String[] args){04:       for(int i = 
0; i < 
4; i++){05:          int j = 
0;06:          j++;07:       }08:       System.out.println(j);09:    }10: }
```


- ( ) 0
- ( ) 1
- ( ) 4
- ( ) 5
- (x) Compilation error

## Explanation

The local variable, j, is declared in the for loop and ceases to exist as soon as the loop is left.

# overriding (#64704)
/root/Java & OO Fundamentals/Methods

Private final methods can be overridden.

- ( ) True
- (x) False

## Explanation

Private methods can't be overridden as they're inaccessible from subclasses. However they can be redefined. There can be simply a method with the same names and arguments in a subclass. This method is not aware of the original method with the same name in the parent class and so it doesn't matter if that parent class is final or not. If the statement was "Private final methods can be redefined", the answer would be True.

# Simple Array (#6499)
/root/Java & OO Fundamentals/Flow Control

What is the result of attempting to compile and run this code ?
```
import java.util.Arrays;public class Test {
    public static void main(String[] args) {
                  int tab[] = new int[
5];
        tab[
3]=
4;
        System.out.println(Arrays.toString(tab));
        tab[
1]=
9;
        for(int i=tab.length-
1;i>
0;i--)
            System.out.print(tab[i]); }
} 
```


- ( ) `[
0, 
9, 
0, 
4, 
0]`
04090`
- (x) `[
0, 
0, 
0, 
4, 
0]`
0409`
- ( ) `[
0, 
0, 
4, 
0, 
0]`
04090`
- ( ) `[
0, 
0, 
0, 
4, 
0]`
04090`
- ( ) `[
0, 
0, 
0, 
4, 
0]`
04009`
- ( ) Compile time error
- ( ) Runtime error

## Explanation

At first we create an Array and put there a value 4. Then we display this Array. Next step is putting value 9. At the end we display Array in reverse order WITHOUT first element.

# { } for initialization (#65070)
/root/Java & OO Fundamentals/Scope

What will be printed on first new A();
```
1:  class A{2:     {3:         System.out.println(
1);4:     }5: 6:     static {7:         System.out.println(
2);8:     }9: }
```


- (x) 2
1
- ( ) 2
2
- ( ) 1
2
- ( ) 1
- ( ) 2
- ( ) Nothing, just will be instantiation of A

## Explanation

When 
```
new A()
```
 is first executed, class A will be loaded, causing the static initialization block of class A to display 2, then an instance of A will be created, executing the instance initialization block and displaying 1.

# main class (#65071)
/root/Java & OO Fundamentals/Methods

Can we override the main method?

- ( ) True
- (x) False

## Explanation

there is no two main methods in the same class but we can have two main methods in same package

# comment (#65072)
/root/Java & OO Fundamentals/Comments

What output is displayed as the result of executing
```
System.out.println("// Looks like a comment.");
```


- (x) // Looks like a comment. 
- ( ) The statement results in a compilation error 
- ( ) Looks like a comment. 
- ( ) No output is displayed 

## Explanation

// is not considered here a comment line, since is part of a string

# IF Statements (#65084)
/root/Java & OO Fundamentals/Flow Control

Given the variables:
```
int a = 
5;int b = 
6;boolean c = true;
```
 Which of the following compiles?

- [x] 
```
if (a > b) {}
```

- [ ] 
```
if (a = b) {}
```

- [x] 
```
if (c = false) {}
```

- [x] 
```
if (c == true) {}
```


## Explanation

The condition in the IF statement should always evaluate to a boolean value.
The second expression evaluates to an integer. The rest of them evaluate to a boolean result.

# Immutibility of String (#65248)
/root/Java & OO Fundamentals/Strings

What will be the output of compiling and running this code?
```
01: public class JavaTest {02:     03:     public static void main(String[] args) {04:         05:         String p = "Java" ;06:         p.concat("lava");07:         p = p.toUpperCase();08:         String q = "test";09:         q.toUpperCase();10:         System.out.println(p + " " + q);11: 12:     }13: }
```


- ( ) JAVALAVA TEST
- ( ) javalava test
- ( ) java test
- (x) JAVA test

## Explanation

As String is immutable p.concat("lava") will create a new String object in the String pool but not assign it to any variable whereas on line 7 create a new String object which again refers to the variable p again. So now p will have the value "JAVA". Same for the line number 9 - the value is not assigned to the variable q. So the final output is "JAVA test".

# Lexicographically compare two String (#65644)
/root/Java & OO Fundamentals/Strings

To compare two strings lexicographically, which of the following String
methods should be used?

- ( ) equals
- ( ) equalsIgnoreCase
- (x) compareTo
- ( ) ==
- ( ) all above

## Explanation

lexicographically means comparing sequentially the letters that have the same position against each other. The only method which allows letter by letter comparison based on ASCI code is compareTo. equals methods compare the whole String agains each other.

# Garbage Collection (#65752)
/root/Java & OO Fundamentals/Garbage Collection

True or False: The garbage collection mechanism guarantees that a program will never run out of memory.

- ( ) True
- (x) False

## Explanation

Garbage collection does not guarantee that a program will not run out of memory. It is possible for programs to use up memory resources faster than they are garbage collected. It is also possible for programs to create objects that are not subject to garbage collection.

# String and objects passed by reference (#65772)
/root/Java & OO Fundamentals/References

Given the code:
```
public class Main {
  public static void main(String[] args) {
      String aString = "12345";
      stringModifier(aString);
      System.out.println(aString);
  }
  private static void stringModifier(String aString) {
      if(aString != null && aString.length() > 
3) {
          aString = aString.substring(
1);
      }
  }}
```
What will be the output

- [x] 12345

## Explanation

The reference passed was overwritten thus no change to the original string will be reflected, although no change can possibly done with the string as it is an immutable object.

# for without statements (#65830)
/root/Java & OO Fundamentals/Flow Control

behaves as?
```
for(; ;){
    // some code}
```


- (x) is similar to a while (true) {} 
- ( ) compile error
- ( ) does nothing
- ( ) runs once

## Explanation

for (;;) without declaration inside compiles fine.
Their behavior is infinite, emulates the action of a "while (true)"

# concat (#65891)
/root/Java & OO Fundamentals/Strings

After these two lines of code: String s = "Dolly "; 
String t = s.concat("Hello, ");
What characters will the object reference t contain? 

- ( ) "Hello, Dolly " 
- (x) "Dolly Hello, " 
- ( ) "Hello, " 
- ( ) "Dolly " 
- ( ) none of the above 

## Explanation

The concat() method appends the characters passed to it to the characters in the String responding to the method call. The concat() method creates a new String, since Strings cannot be changed once they are created. 

# For structure (#6593)
/root/Java & OO Fundamentals/Flow Control

Will the following code compile?
```
1: int y=
0;2: for (int x=
0, y=
1;
x<
10;
x++, y++) {3:    System.out.println(x+y);4: }
```


- ( ) True
- (x) False

## Explanation

You are trying to declare variable y which is already declared before, resulting in a duplicate local variable error.

# Java SE 6 API (#65985)
/root/Java & OO Fundamentals/Platform

Is the JDK a superset of the JRE?

- (x) True
- ( ) False

## Explanation

Have a look at this: http://download.oracle.com/javase/6/docs/.

# CaMeL case (#65994)
/root/Java & OO Fundamentals/Naming

Which of the following statements is an example of CaMeL case:

- (x) clearBuffer()
- ( ) clearbuffer()
- ( ) Clearbuffer()

## Explanation

A wiki article on this: http://en.wikipedia.org/wiki/CamelCase.

# Java Language Keywords (#66012)
/root/Java & OO Fundamentals/Naming

Choose all keywords in the Java programming language.

- [x] instanceof
- [x] short
- [x] void
- [x] throws
- [x] throw
- [x] default

## Explanation

Full list of keywords you can find here: http://download.oracle.com/javase/tutorial/java/nutsandbolts/_keywords.html.

# Scope of variables (#66227)
/root/Java & OO Fundamentals/Scope


```
1: public class MyCity {2:      private int myPeople;3:      public static void main(String... args) throws Exception {4:               this.myPeople = 
30;5:               myPeople++;6:               System.out.println(myPeople);7:      }8: }
```
Will this compile?

- ( ) True
- (x) False

## Explanation

Static method cannot access instance variables directly.
In static method, you mustn't use 'this'.

# modifiers cunstructors (#66275)
/root/Java & OO Fundamentals/Classes and Objects

Which modifiers can be applied to a constructor?

- [x] private
- [ ] abstract
- [ ] final
- [ ] volatile
- [ ] native
- [ ] None of the above.

## Explanation

private.
Constructors are not inherited and can not be overridden, so there is no need for the final modifier in a constructor declaration. Furthermore, an abstract constructor would be useless, since it could never be implemented. The volatile modifier can be applied to a field, but not to a constructor. Native constructors are not permitted, because it would be difficult for Java to verify that the native constructor properly invokes the superclass constructor. 

# modifiers that can be applied of a field (#66276)
/root/Java & OO Fundamentals/Variables

Which of the following modifiers can be applied to the declaration of a field?

- [ ] abstract
- [x] final
- [x] private
- [x] protected
- [x] public

## Explanation

A field is a class member. A static field is sometimes called a class variable. A non-static field is sometimes called an instance variable. A variable declaration that is immediately contained by a block such as a method body is called a local variable. The access modifiers, private, protected and public, can be applied to a field. A final field can not have its value assigned more than once. The abstract modifier may be applied to methods but not to fields. 

# Super keyword. (#66440)
/root/Java & OO Fundamentals/Scope


```
01: class A{02:    public A(){03:        System.out.println("This is A Class...");04:    }05: }06: 07: class B extends A{08:     public B(){09:        System.out.println("This is B Class...");10:        super();11:     }12: }13: 14: B bb = new B();
```
What will be an output of the code snippet?

- ( ) This is B Class...
This is A Class...
- (x) Compilation error
- ( ) This is A Class...
This is B Class...
- ( ) This is B Class...
- ( ) none of above

## Explanation

Constructor's call must be the first statement in a constructor.

# arithmetic operators (#66507)
/root/Java & OO Fundamentals/Operators

The purpose of this code is to switch values of two variables. Select correct answer to complete the code:
```
public class Arithmetic {
  public static void main(String[] args){
  int a = 
5;
  int b = 
2;
  a += b;
            //your answer }
```


- ( ) 
```
b = b - a;b = -ba = a - b;
```

- ( ) 
```
b -= a; b = -a;a = b - a;
```

- ( ) 
```
b = a - b; a = b;a = b - a;
```

- (x) 
```
b -= a; b = -b;a = a - b;
```


## Explanation

First code has an error. It lacks one semicolon.
Second answer doesn't make any sense, because it assigns "b" to "a", and in the next line variable "a" will equal 0.
Output of third answer just like a second one. It messes up with operators and leads to incorrect values.
Correct answer is D; 
int a = 5;
int b = 2;
a += b; // a = 7, b = 2
b -= a; // a = 7, b = -5;
b = -b; // b = 5;
a = a - b // a = 2, b = 5;

# scope in for loop (#66594)
/root/Java & OO Fundamentals/Scope

Given the following piece of code
```

1: int sum = 
0;
2: for (int i = 
0; i < 
10; i++) {
3:
   sum += i;
4: }
5: System.out.println("sum : " + sum);
6: System.out.println("last i : " + i);
```
, what is true?

- (x) It does not compile
- ( ) It prints:
```
 sum : 
55last i : 
10
```

- ( ) It prints:
```
 sum : 
45last i : 
9
```


## Explanation

The scope for variable 
```
i
```
 is the for loop. 
```
i
```
 cannot be accessed outside the loop in the last line of the code.

# byte and int (#66609)
/root/Java & OO Fundamentals/Variables

What will be the output?
```
1: class TestByte{2:     public static void main(String[] args) {3:         int i = 
255;4:         byte b = (byte)i;5:         int n = i+b;6:         System.out.println(n);7:     }8: }
```


- ( ) 510
- ( ) Compilation fails
- ( ) 256
- (x) 254

## Explanation

Byte's range is from -127 to 128. 255 when cast to byte makes b = -1.
Hence 255+ (-1) = 254

# Which lines will compile? (#66711)
/root/Java & OO Fundamentals/Variables

Which lines will compile?

- [ ] 
```
int i = "5";
```

- [x] 
```
int i = 
5+'3';
```

- [ ] 
```
int i = 
5+.5;
```

- [x] 
```
int i = 'a';
```


## Explanation

The first option will not compile because the String object can not be assigned to an int variable.
The second option will compile because the character will automatically be cast to an int and then added to the value 5 and assigned to i
The third option will not compile because the .5 value will result in an autocast on the value 5 before addition and therefor result in an double not an int.
The fourth option is ok for the same reason as the second

# The @see tag (#66799)
/root/Java & OO Fundamentals/Javadoc

The Javadoc tag '@see' is used to see an example of the implementation.
The above statement is true or false?

- ( ) True
- (x) False

## Explanation

Javadoc @see tags are used to create "See also" links or pointers in the documentation created by Javadoc. 
They can be just a simple text pointer to a subject, a link to a website or a reference to another piece of Javadoc like the explanation of a method which is called inside the method's Javadoc the user currently is reading. 
For more on the subject: 
<a href="">http://docs.oracle.com/javase/7/docs/technotes/tools/windows/javadoc.html#see</a>

# Which declaration of the main method below ... (#66893)
/root/Java & OO Fundamentals/Scope

Which declaration of the main method below would allow a class to be started as a standalone program. Select the one correct answer. 

- ( ) `public static int main(char args[])`
- (x) `public static void main(String args[])`
- ( ) `public static void MAIN(String args[])`
- ( ) `public static void main(String args)`
- ( ) `public static void main(char args[])`

## Explanation

Java Language Specification
http://docs.oracle.com/javase/specs/jls/se5.0/html/execution.html#12.1.4
The method main must be declared public, static, and void. It must accept a single argument that is an array of strings. This method can be declared as either
```
public static void main(String[] args)
```
 or
```
public static void main(String... args)
```


# Data types (#66998)
/root/Java & OO Fundamentals/Variables

Which of these data types size is 4 bytes?

- [x] int
- [ ] short
- [ ] long
- [x] float
- [ ] double

## Explanation

For more information http://download.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html

# What is result? (#67087)
/root/Java & OO Fundamentals/Scope


```
 public class A {
public static void main(String args[]) {
   class B {
       public
int i = 
3;
   }
  Object o = (Object) new B();
  B b = (B) o;
  System.out.println("i = " + o.i);
}}
```


- (x) Compilation fails
- ( ) i = 3
- ( ) ClassCastException
- ( ) Runtime exception

## Explanation

Object 
```
o
```
 is casted to class 
```
B
```
 but object 
```
o
```
 doesn't have a variable 
```
i
```


# What is the result? (#67211)
/root/Java & OO Fundamentals/Scope


```

01: class ScopeTest {
02:
 public static void main(String[] args) {
03:
   int y = 
2; 
04:
   if(++y>
3 | x++ == 
1) {
05:
      System.out.println("true");
06:
   } else {
07:
      System.out.println("false");
08:
   }
09:
 }
10:
 int x = 
1;
11: }
```


- ( ) true
- ( ) false
- (x) Compilation fails
- ( ) An Exception is thrown at runtime

## Explanation

Compilation fails because variable x isn't in static context.

# Constructors (#67271)
/root/Java & OO Fundamentals/Classes and Objects

Are those constructors good
```
01: public class BlackBeltFactory {02:     03:     public BlackBeltFactory(Integer i){04:         this.number = BigInteger.valueOf(i.longValue());05:     }06:     07:     private BlackBeltFactory(Long l){08:         this.number = BigInteger.valueOf(l);09:     }10:     11:     private BigInteger number;12:     13:     public static void main(String[] args) {14:     }15: }
```


- (x) True
- ( ) False

## Explanation



# Plus Operator on String Statements (#67344)
/root/Java & OO Fundamentals/Operators


```
 System.out.println("2 + 2 = " + 
2 + 
2);System.out.print("2 + 2 = " + (
2 + 
2));
```
What is the result from the code above?

- ( ) 2 + 2 = 4
2 + 2 = 4
- ( ) 2 + 2 = 22
2 + 2 = 22
- (x) 2 + 2 = 22
2 + 2 = 4
- ( ) 2 + 2 = 4
2 + 2 = 22

## Explanation

On the first statement, since no parentheses are given, 2 + 2 in the back will be considered as adding a String, so it will produce 2 + 2 = 22.
While on the second statement, (2 + 2) will be counted first and the result will be added to the String later, so it will produce 2 + 2 = 4

# Naming of variables (#67363)
/root/Java & OO Fundamentals/Naming

Which declarations compile correctly?

- [x] 
```
int a;
```

- [ ] 
```
int 
687;
```

- [ ] 
```
int a5#;
```

- [x] 
```
int $75;
```

- [x] 
```
String ifabc;
```

- [x] 
```
String abc;
```


## Explanation

Names of variables can contain numbers but are not allowed to start with numbers. Although "_" or "$" at the start is allowed, but convention is to start with a letter.
see:
http://docs.oracle.com/javase/tutorial/java/nutsandbolts/variables.html#naming

# Which are true? (#67469)
/root/Java & OO Fundamentals/Operators

Which operators will always evaluate all the operands?

- [x] &
- [x] %
- [ ] &&
- [ ] ? : 
- [x] |

## Explanation

Non-short circuit operators (|, &) always evaluate all operands.
All mathematical operators evaluate all the operands.

# equals(); (#67500)
/root/Java & OO Fundamentals/References

we should use equals() method to find two references are pointing to same object or not

- ( ) True
- (x) False

## Explanation

== should be used for that.
we can use equals() to find object's equality

# unreachable (#67504)
/root/Java & OO Fundamentals/Flow Control

Given:
```
1: class Test {2:    public static void main(String [] args) {3:       int x = 
2;4:       while (true) {5:          x--;6:       }7:       System.out.print(x);8: }
```
What is the result?

- ( ) 0
- ( ) 1
- ( ) 2
- (x) Compiletime error

## Explanation

System.out.println() is unreachable statement

# local variables (#67510)
/root/Java & OO Fundamentals/Variables

local variables should be initialized before using them

- (x) True
- ( ) False

## Explanation

we can initialize local variables at declaration or before using them,like
int 1 =10;
or
int i;
//some statements
i = 10;
System.out.println(i);
but
int i;
//some statements
System.out.println(i);
i=10; is wrong

# String Concatenation (#67600)
/root/Java & OO Fundamentals/Strings

given the following code, which of the following statement is true?
```
1: public class ConcatTest{2:     public static void main(String args[]) throws Exception {3:         String x = "Composed";4:         x.concat("String");5:         System.out.println(x);6:     }7: }
```


- ( ) The code does not compile
- ( ) The output is 
```
ComposedString
```

- (x) The output is 
```
Composed
```

- ( ) An exception is thrown

## Explanation

3 is true : the call to 
```
x.concat("String")
```
 creates a new string litteral with the value of 
```
ComposedString
```
 but it is not affected to x.1 is false : the code compiles
2 is false : cf. 1
4 is false : no exception is thrown

# Java Bytecode (#67634)
/root/Java & OO Fundamentals/Platform

Is Java bytecode an intermediate language which is typically compiled from Java?

- (x) True
- ( ) False

## Explanation

Java bytecode is an intermediate language which is typically compiled from Java, but it can also be compiled from other programming languages. 

# final (#67718)
/root/Java & OO Fundamentals/Variables

What keyword do you use to create a variable whose value cannot change

- [x] final

## Explanation

final should be used where a variable should/can not be changed. ex:
public final double radius;

# Is this loop broken? (#67846)
/root/Java & OO Fundamentals/Flow Control


```
1: int e = 
10;2: int i = 
0;3: for(; i < e--;) {4:    System.out.println(i++);5: }
```
What is the output if you run this code?

- ( ) None - run-time error
- (x) 01234
- ( ) 0123456789
( basic loop, stops at 10 )
- ( ) None - doesn't compile

## Explanation

This is a valid, fully-formed for-loop. Because the constraining variable is decremented during each loop, only half of what may be the expected values are printed.

# static method invoked from null object (#67954)
/root/Java & OO Fundamentals/Classes and Objects

Given:
```
01: 02: class B {03:     public String foo() {04:         System.out.println("foo");05:         return null;06:     }07: }08: 09: public class Test {10:     public static void main(String[] args) {11:         B b = new B();12:         try {13:             System.out.println(b.foo().valueOf("valueOf"));14:         } catch (NullPointerException e) {15:             System.out.println("A NullPointerException");16:         }17:     }18: }
```
Choose the output of the invocation.

- ( ) foo
A NullPointerException
- ( ) foo
- ( ) A NullPointerException
- (x) foo
valueOf
- ( ) foo
valueOf
A NullPointerException

## Explanation

b.foo() prints "foo" and returns a null String object. As valueOf method of String class is static, is associated with the String class, and not with the returned instance. Therefore it can be invoked and the result "valueOf" is printed.

# Primitive Types (#6825)
/root/Java & OO Fundamentals/Variables

Java methods can return only primitive types (int, double, boolean,etc).

- ( ) True
- (x) False

## Explanation

Explanation: Java methods can also return objects, such as a String.

# [B]Java Class Package Definition (#7167)
/root/Java & OO Fundamentals/Platform

In which order does a Java program has its definitions laid out?

- ( ) import, package, classname
- ( ) classname, import, package
- (x) package, import, classname
- ( ) package, classname, import

## Explanation

package, import, classname

# String immutability (#7380)
/root/Java & OO Fundamentals/Strings

What is the output of the following code?
```
1: String str = "Welcome";2: 3: str.concat(" to Java!");4: 5: System.out.println(str);
```


- ( ) A) Strings are immutable, compilation error at line 3
- ( ) B) Strings are immutable, runtime exception at line 3
- (x) C) Prints "Welcome"
- ( ) D) Prints "Welcome to Java!"

## Explanation

Strings are immutable. So str.concat("to Java!") will not append anything to str. Infact it will create another string "Welcome to Java!" and leaves it.

# Ambiguous method? (#7614)
/root/Java & OO Fundamentals/Methods

When it is part of the same program as 
```
 void newMethod (int age, String surname),
```
 the following method would be ambiguous: 
```
 void newMethod (String surname, int age).
```


- ( ) True
- (x) False

## Explanation

The second method accepts the same parameters as the first method, but in reverse order. Thus they are not ambiguous

# Class Test 4 (#7618)
/root/Java & OO Fundamentals/Classes and Objects

Given the following class, which statements can be inserted at line 1 without causing the code to fail compilation?
```
public class TestClass {
  int a;
  int b = 
0;
  static int c;
  public void m() {
      int d;
      int e = 
0;
      // Line 1
  }}
```


- [x] a++;
- [x] b++;
- [x] c++;
- [ ] d++;
- [x] e++;

## Explanation

All the instance or static variables are given a default values if they are not explicitly initialized. All numeric variable are given a value of zero or equivalent to zero (ie. 0.0 ). Booleans are initialized to false and objects are initialized to null.

# Ambiguous method? (#7676)
/root/Java & OO Fundamentals/Methods

When the following 2 methods are part of the same program are they ambiguous?
```
 void newMethod (int x, String y)String newMethod (int x, String y)
```


- (x) True
- ( ) False

## Explanation

The methods differ only in return type. They are not overloaded. 

# Abstract Method (#8618)
/root/Java & OO Fundamentals/Classes and Objects

An abstract method cannot be overridden.

- ( ) True
- (x) False

## Explanation

Abstract methods are meant to be overridden in the subclass. Abstract methods describe a behaviour but do not implement it. So the subclasses have to override it to actually implement the behaviour. A subclass may chose not to override it, in which case, the subclass will have to be abstract too.

# Variable not initialized (#864)
/root/Java & OO Fundamentals/Variables

What is the result ?
```
01: 
  public static void main(String[] args) {02:         boolean b = true;03:         int j;04:         if(b) j = 
0;05:         for(int i=
0;i<
50;++i) {06:             System.out.print(i);07:             if(i>
9) break;08:             j = i;09:         }10:         System.out.print(j);11:     }
```


- (x) Compilation fails
- ( ) Runtime error
- ( ) 012345678910
- ( ) 0123456789
- ( ) 01234567891010
- ( ) 0123456789109
- ( ) 01234567899

## Explanation

The compiler can not identify that j is initialized at line 4 because b is not final. So at line 8 it will give you a compilation error

# Compare instance of Stringbuffer (#9137)
/root/Java & OO Fundamentals/Classes and Objects

The code below works perfectly without errors. True or false?
```
StringBuffer sb1 = new StringBuffer("0123456");StringBuffer sb2 = new StringBuffer("0123456");String str1 = sb1.toString();String str2 = sb2.toString();if ( str1.equals( str2 ) ) {
  System.out.println( " str1.equals(str2) ? true" );} else {
  System.out.println( " str1.equals(str2) ? false" );}
```


- (x) True
- ( ) False

## Explanation

Instance of stringBuffer changes to string through toString().

# Java is 100% Object Oriented Language? (#9836)
/root/Java & OO Fundamentals/Platform

Java is 100% Object Oriented Language?

- ( ) True
- (x) False

## Explanation

Java is not 100% object oriented because primitive is not treats as object.

# Integer comparator (#9941)
/root/Java & OO Fundamentals/References

What will the following code output?
1: Integer f = 400;
2: Integer d = 400;
3: if(f==d)
4: System.out.println("==");
5: if(f.equals(d))
6: System.out.println("equals");

- ( ) ==
- (x) equals
- ( ) ==
equals
- ( ) Output will be empty

## Explanation

Operator "==" compares the values of the two Integer object references. Even though they contain the same primitive int values, they are two distinct objects. The equals method compares the primitive int values that the Integer objects wrap.

# OO basic principle (#9975)
/root/Java & OO Fundamentals/Encapsulation

Which OO principle does the following code snippet represent:
```
class A{
  private String name;
  public String getName() {
      return name;
  }
  public void setName(String name) {
      this.name = name;
  }}
```


- ( ) Inheritance
- (x) Encapsulation
- ( ) Polymorphism
- ( ) Abstraction
- ( ) None of above

## Explanation

The mutation and retrieval of the field "name" is encapsulated in the getName/setName methods.

