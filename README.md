# Uncommon Scala Error: Private Var and Setter Exception Handling

This example showcases a potential issue when using a private variable (`_age`) with a custom setter in Scala to enforce constraints.  While this pattern is common, errors in the setter can be challenging to track if not carefully handled.

The code creates a `MyClass` with a `name` and an `age`.  The `age` is managed using a private var (`_age`) and a custom setter that throws an exception if a negative age is assigned.

The `Main` object demonstrates correct usage and error handling.

**Potential issues:**

- Failure to handle the exception thrown by the setter could result in application crashes.
- The use of a private var and a public getter/setter might be considered less idiomatic by some Scala programmers (case classes and immutable data structures are usually preferred).