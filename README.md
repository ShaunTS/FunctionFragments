# FunctionFragments
The `FunctionFragment[+A, -B]` trait extends and works very similarly to `PartialFunction[+A, -B]`.

By implementing a strategic override of the `isDefinedAt(x: A): Boolean` method inherited from `PartialFunction`, the `FunctionFragment` trait allows for more general purpose use of partial functions. That is to say, FunctionFragments will not throw a `MatchError` if pattern matching fails within the scope of the function logic IF it has been lifted into a full function.
