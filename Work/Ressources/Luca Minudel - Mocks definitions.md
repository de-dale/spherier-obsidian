---
ressource:
  - 📰 Article
author:
  - "[[Luca Minudel]]"
link:
  - https://github.com/lucaminudel/TDDwithMockObjectsAndDesignPrinciples/blob/master/Slides/TDD-SOLID.pdf
trello: 
relates:
  - "[[Test Doubles]]"
---

## Test Double
In automated unit testing replaces an object on which the class under test depends
Can be a Stub, a Mock a Spy

## Test Stub
Has configurable canned responses.
Is used to control the indirect input to the
class under test

## Strict Mock
Has configurable expectations.
Test fails when expected msg is not sent.
Test fails when unexpected msg is sent.
Used for verifying messages sent by the
class under test


LSP – Liskov Substitution Principle
methods that use a base class must be able
to use instances of derived classes without
knowing it: all the derived classes must
honor the contract defined by the base class