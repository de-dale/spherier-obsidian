En [[Programmation Orientée Objet]], on parle également de **ploymorphisme**.

Poly means many  and morphs means forms. So anything which has multiple forms is called polymorphism.

In computer science terms, any entity like operator or method or constructor which takes many forms and can be used for multiple tasks is called as polymorphism.

For example, '+'operator can be used for addition of two numbers as well as for concatenation of two strings.

In Java, there are two types of polymorphism : static polymorphism and dynamic polymorphism.

Any entity which shows polymorphism during compilation is called **static** polymorphism.
Operator overloading, method overloading and constructor overloading are best examples of static polymorphism.

```java
// Method Overloading

class Sample {
	void anyMethod(int i) {
		...
	}
	
	void anyMethod(String s) {
		...
	}
}
```

Any entity which shows polymorphism at runtime is called **dynamic** polymorphism.
Method overriding is the best example of dynamic polymorphism.

```java
// Method Overriding

class Sample {
	void anyMethod() {
		...
	}
}

class SubSample extends Sample {

	@Override
	void anyMethod() {
		...
	}
}
```
#OOP 