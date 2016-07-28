# Fundamentals of Object-Oriented Design
-  http://www.meetup.com/Google-Developers-Group-Houston/events/232310615/
-  https://github.com/gdghtown/IntroToOO

## Nygaard Classifcation
### Procedural (Imperative)
-  [Algol](https://en.wikipedia.org/wiki/ALGOL)

### Constraint (Delcarative)
-  SQL (modern example)

### Functional (Delcarative)
-  LISP

### Object Oriented
-  Simula 67

## Presenter's Working Definition
-  models a system or domain
-  utilizes late-binding polymorphism for extensibility

### Domain Modeling
-  Leveraging domain expertise leads to software that's easier to read & maintain
-  Reasonable Code: small changes in requirements == small changes in code
-  Open-Closed Principle: Code should be open for extension, but closed for modification.
-  Dependency Inversion Principle
    -  stable abstractions instead of concrete classes
    -  extend behavior polymorphically by changing concrete examples of the same *type*

### Liskov Substitution Principle (polymorphism)
 -  Subtype requirement: all Subtypes (S), must be valid examples of their Parent types (T)

### Late Binding
-  Concrete implementations are created **after** system implementation is complete.

## OO Principles

### SOLID
-  These 1st 5 are for class design. There are 6 more.

### Law of Demeter
-  Don't search for things, go directly to what you want
-  Also, Tell, don't Ask
-  Avoid "train wrecks"

### Design Patterns
-  Patterns: Effective solutions to common problems
-  avoid anti-patterns

Clarity of code comes from clarity of thought
