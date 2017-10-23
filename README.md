# Kotlin Study Notes
## [Data Class](dataClass.kt)
## Sealed Class 
- It seems like a very specific feature just to avoid an else clause.
- So, the value must be in having an enum that can contain data... perhaps as an initialize class that can be re-used.
- I am imagining building blocks of a specific type (add String widget, add Date widget, add number widget)
## Generics

Java | Kotlin | Note
---|---|---
class Foo<T>(T t) | class Foo<T>(t: T) | Generic Class Definition
Foo<Integer> foo = new Foo<Integer>(1) | val box: Foo<Int> = Foo<Int>(1) | Generic class instatiation - long form
Foo<Integer> foo = new Foo<>(1) | val foo: Foo(1) | Generic class instatiation - short form, generic parameters can be inferred in Kotlin
void addAll(Collection<? extends E> items)||Covariant (Producer Extends)
List<? super String> ||Contravariant (Consumer Subtypes)

  
## Slides
[![GitPitch](https://gitpitch.com/assets/badge.svg)](https://gitpitch.com/terrywbrady/terrywbrady-demo/kotlin?grs=github&t=white)
