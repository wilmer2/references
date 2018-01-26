# Kotlin

## Declaration
```kotlin
// Mutables
var n: Int = 42

// No mutables
val n: Int = 42

// Nullable
var n: Int? = 42
````

## Built-in Types
```kotlin
Double
Float
Long
Int
Short
Char
```

## Packages
### Declaration
```kotlin
package foo.Bar
```

### Import
```kotlin
import foo.Bar
import foo.Bar as Kar
import foo.*
```

## Arrays
```kotlin
```

## Functions
### Declaration
```kotlin
fun sum(a: Int, b: Int): Int {
  return a + b
}
```

### Inline Return
```kotlin
fun sum(a: Int, b: Int) = a + b
```

## Control Flow
### If
```kotlin
if (condition) {
  // ...
} else {
  // ...
}

// Inline
val foo = if (a < b) a else b

// Blocked Expression
val max = if (a > b) {
  a
} else {
  b
}
```

### When
```kotlin
when (foo) {
  42 -> a //...
  43, 44 -> b // Multiple
  in 1..10 -> // Use in
  is String -> // Use is
  parseInt(s) -> // Expressions
  else -> {
    // Block Expression
  }
}

// Direct Booleans
when {
  x.isOdd() ->
  x.isEven() ->
  else ->
}
```

### For
```kotlin
for (cat: Cat in cats) {
  // ...
}
```

### While
```kotlin
while (condition) {
  // ...
}

do {
  // ...
} while (condition)
```

## Classes

```kotlin
class Pug {
  // ...
}
```

### Properties
```kotlin
class Pug {
  val name: String = "pepe"
}
```

### Primary Constructor
```kotlin
class Pug(name: String = "Pepe") {
  init {
    // Constructr code
  }
}
```

### Inheritance
All classes are final on kotlin by default, for inheritance requires de `open` keyword
```kotlin
open class Dog

class Pug : Dog {
  // ...
}
```
#### Overriding Methods
Requires `open` keyword on parent method
```kotlin
class Pug: Dog {
  override fun greet() {
    super.greet() // Call to parent
  }
}
```

#### Overriding Properties
Requires `open` keyword on parent propery
```kotlin
class Pug: Dog {
  override val name: String = "pepe"
}
```

### Inner Classes
```kotlin
class Pug {
  inner class Pepe {
    fun foo() {
      super@Pug.greet() // Call to parent method
    }
  }
}
```