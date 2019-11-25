# SOLID
SOLID principles for kids.

## [S]ingle Responsibility Principle
Class must have only one reason to change and only one responsibility.

__Entites must not modify database, it's repository's job, do not make _Swiss Army knife_ class__

## [O]pen Closed Principle
Code must be open for extension and closed for modification.

__Consider discount class, if you use `switch/case` or `if/else` in order to handle different types of discount, you violated this principle, because if a new type of discount is added, you have to add new `case/else` to the class. you can use interfaces, e.g: `IDiscount` and add `Calculate` method to it, then add a class for each type of discounts, if a new type of discount is added, you just need to add new class for it and there is no need to touch other discount classes.__

## [L]iskov Substitution Principle
Derived classes must be substitutable for their base classes.

__A `Square` is a `Rectangle`, so inheriting form `Rectangle` class to make a `Square` makes sense, right? okay, can you use `Square` anywhere you expect a `Rectangle`?__ _See: [this Stackoverflow answer](https://stackoverflow.com/a/584732/3367974)_

## [I]nterface Segregation Principle
Clients should not be forced to depend upon interfaces that they don't use.

__Consider you have an interface called `IFile` with 2 methods, `Read` and `Write`, and now you want to add a class for reading file, not writing file, e.g: `FileReader`, if you use `IFile` interface for this class, you have to implement `Write` method too, and that's the problem.__

## [D]ependency Inversion Principle
High level modules should not depend on low level modules; both should depend on abstractions. Abstractions should not depend on details.  Details should depend upon abstractions.

__High level classes should not work directly with low level classes, they should work with them through interfaces. for example in ASP.NET MVC, `ProductController` should not work directly with `ProductRepository`, it should use `IProductRepository`__
