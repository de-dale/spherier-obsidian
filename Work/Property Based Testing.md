[[TDD]]

Invariant fonction ou 

https://youtube.com/watch?v=shngiiBfD80

Tests : exampla based testing
**Property** : something which is always truc under specified circumstances

Tips :
1. write tests backwards (depuis l'"assert vers le given)
2. Specify valid input completely
3. Use ports and adapters for external dependencies
4. **Expect failure. Create failure**
5. **Ask the hard questions**
6. Output all the useful things
7. **Create the visibility you need**
8. fix the test, fix the mental model
9. Make the test reveal why it failed

d. Test the API
**e. Define Success**

Port and adapter 
=> provide an implementation that fit the port

Generated inputs AND properties of output

Relational property : compares two outputsd

[[Tidy First#Beneficially Relating Elements]]
> Behavior :
> - input/output pairs
> - invariants
>
> -- Structure and Behavior, p.61


# 🤖 IA

> ## What is Property-Based-Testing ?

Property-Based Testing (PBT) is a software testing approach that focuses on verifying properties that your code should always hold, rather than testing specific code paths with predefined inputs.

Here's a breakdown of the key points:

- **Focus on Properties:** Instead of writing tests for individual scenarios, PBT defines properties that your code's behavior must always adhere to. These properties are expressed in a concise and reusable way.
- **Randomized Input Generation:** PBT leverages a testing framework to automatically generate a large number of random inputs for your code. This helps uncover edge cases and unexpected behaviors that might be missed with manually crafted test cases.
- **Less Prone to Bias:** Since the inputs are randomized, PBT is less susceptible to the biases that can creep in when testers write specific test cases based on their assumptions.
- **Higher Code Coverage:** The random test data generation in PBT can lead to a higher level of code coverage compared to traditional testing methods.

Here's an analogy to understand PBT better:

Imagine testing a vending machine. Traditionally, you might write tests for specific inputs like valid coins or selecting a specific product. However, with PBT, you define a property like "the vending machine should dispense the selected product when a valid payment is made." Then, the testing framework automatically feeds the vending machine with various combinations of coins and product selections to verify the property holds true.

PBT offers several benefits:

- **Improved Code Quality:** By focusing on properties, PBT encourages developers to think more deeply about how their code should behave under various conditions.
- **Increased Confidence:** The random nature of input generation helps uncover hidden bugs and edge cases, leading to a more robust codebase.
- **Reduced Maintenance:** Since PBT tests focus on properties, they are less likely to break when the code undergoes changes, unlike tests that rely on specific code paths.

Here are some things to keep in mind about PBT:

- **Not a replacement:** PBT is not a complete replacement for traditional testing methods. It's best used in conjunction with other testing approaches.
- **Learning Curve:** Setting up and understanding PBT frameworks might require some initial investment in learning.
- **Property Definition:** Defining clear and concise properties is crucial for the effectiveness of PBT.

Overall, Property-Based Testing is a powerful technique for improving software quality and increasing confidence in your code's correctness.


### 🔗 Ressources

https://medium.com/criteo-engineering/introduction-to-property-based-testing-f5236229d237
https://github.com/ythirion/journey-to-property-based-testing
https://xtrem-tdd.netlify.app/Flavours/Testing/pbt
https://yoan-thirion.gitbook.io/knowledge-base/software-craftsmanship/code-katas/improve-your-software-quality-with-property-based-testing/a-journey-to-property-based-testing

https://blog.ippon.fr/2021/10/06/property-based-testing-ou-linsuffisance-des-tests-unitaires/
https://medium.com/criteo-engineering/introduction-to-property-based-testing-f5236229d237