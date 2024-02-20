Principe [[SOLID]]

Entities must depend on abstractions not on concretions.  
It states that the high level module must not depend on the low level module, but they should depend on abstractions.

[[Cohésion]]
[[Couplage]]
[[Cohésion vs. Couplage]]


#### Smells  
Dependencies between classes (vs interface)  
Monolithic architecture  
Abstraction depends on details/implementation

### 🤖 IAxplication 

> The Dependency Inversion Principle (DIP) is one of the key principles of object-oriented programming that promotes loose coupling and high cohesion in software design. It states that:
> 
> 1. **High-level modules should not depend on low-level modules. Both should depend on abstractions.**
> 2. **Abstractions should not depend on details. Details should depend on abstractions.**
>     
>In simpler terms, the DIP advocates for building software in a way that high-level components, such as business logic or user interfaces, should not directly depend on low-level components, such as databases or external services. Instead, they should depend on abstractions, which represent the essential features of the low-level compo# Hexagonal And Beyondnents without revealing their implementation details. This decoupling allows for greater flexibility, maintainability, and testability of the overall system.
>
>To achieve dependency inversion, there are two main approaches:
> 
> 1. **Using interfaces:** Interfaces define the contracts between components, specifying the methods they must implement without defining how those methods are implemented. High-level components depend on these interfaces, allowing them to interact with various implementations of the interface without being tied to any particular one.
> 2. **Using dependency injection:** Dependency injection is a technique where dependencies are provided to components externally, rather than being created or managed by the components themselves. This allows for loose coupling and makes it easy to swap out different implementations of the same interface.
>     
> Benefits of applying the Dependency Inversion Principle:
> 
> 1. **Increased testability:** By decoupling high-level components from low-level ones, it becomes easier to test the high-level logic in isolation, using mock or stub implementations for the low-level dependencies.
> 2. **Improved maintainability:** By relying on abstractions, the code becomes more readable and maintainable, as it focuses on the "what" rather than the "how" of the low-level implementations.
> 3. **Enhanced extensibility:** By decoupling components, it becomes easier to add new features or modify existing ones without affecting other parts of the system.
> 4. **Reduced code fragility:** By minimizing direct dependencies between components, the system is less susceptible to changes in the low-level components, making it more resilient and adaptable to change.
> 5. **Promotes modularity:** By relying on abstractions and interfaces, the system is naturally divided into more modular and reusable components, making it easier to manage and understand. 
> 
> In conclusion, the Dependency Inversion Principle is a valuable tool for designing software that is testable, maintainable, extensible, and adaptable to change. By decoupling high-level components from low-level ones and relying on abstractions, developers can create software that is more robust, flexible, and easier to evolve over time.