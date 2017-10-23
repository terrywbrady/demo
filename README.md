# Kotlin Study Notes
## [Data Class](dataClass.kt)
## Sealed Class 
- It seems like a very specific feature just to avoid an else clause.
- So, the value must be in having an enum that can contain data... perhaps as an initialize class that can be re-used.
- I am imagining building blocks of a specific type (add String widget, add Date widget, add number widget)
## Generics

Java | Kotlin | Note
---|---|---
`class Foo<T>(T t)` | `class Foo<T>(t: T)` | Generic Class Definition
`Foo<Integer> foo = new Foo<Integer>(1)` | `val box: Foo<Int> = Foo<Int>(1)` | Generic class instatiation - long form
`Foo<Integer> foo = new Foo<>(1)` | `val foo: Foo(1)` | Generic class instatiation - short form, generic parameters can be inferred in Kotlin

## Variance
- Declaration-site variance - variance is declared on class def
- Use-site variance - variance is declared in usage (method def)
  - `void addAll(Collection<? extends E> items)`
  - `add(List<? super String>)` 

Java | Kotlin | Note
---|---|---
`Foo<E>`| Foo<E>|Invariant, type must match generic declaration 
`Foo<? extends E>` (Producer Extends)|`Foo<out E>`|Covariant Upper Bound 
`Foo<? super String>)` (Consumer Subtypes) |`Foo<in E>`|Contravariant Lower Bound

Note:
  - T extends ClassName supported in class def
  - ? extends ClassName supported in class def
  - ? super ClassName supported in class def
  - T super ClassName does not seem to be supported

## Star Projection
    class Foo<out TUpper>{
      fun get(): <out TUpper> {} //is this the correct meaning of TUpper? 
      fun get(): <*> {} 
      fun get(): <out Any?> {} 
    }

    class Foo<T>{
      fun set(<in Nothing>): {} 
      fun set(<*>): {} 
    }

- https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/
- https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing.html  
  - Kotlin Nothing has no equivalent in java
- https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html
  - Kotlin Unit is similar to void

## Generic Functions within a class
- create example

## Generic Constraints within a class function
- create example

## Slides
[![GitPitch](https://gitpitch.com/assets/badge.svg)](https://gitpitch.com/terrywbrady/terrywbrady-demo/kotlin?grs=github&t=white)
