# Java

## DataTypes

### Basic Declaration
```java
int foo
byte foo
short foo
long foo
float foo double foo
boolean foo
char foo
```

### The final keyword
Final variables can't be reassigned to another object
```java
final int foo
```

## Control Flow
### If
```java
if (cond) {
  // ...
} else if (cond) {
  // ...
} else {
  // ...
}
```

### Ternary
```java
int foo = cond ? foo1 : foo2;
```

### While
```java
while(cond) {
  // ...
}
```

### Do..While
```java
do {
  // ...
} while(cond)
```

### For
```java
for (int i = 0; i <= n; i++) {
  // ...
}
```

### For each
```java
for (int client : clients) {
  // ...
}
```

### Switch
```java
switch(foo) {
  case 1:
    // ...
    break;
  default:
    // ...
  break;
}
```

## Errors
### Handling
```java
try {
  // ...
} catch (Exception e) {
  // ...
}
```

## Classes
### Attributes, Methods and Constructor
```java
class Cat {
  public int age;
  private int type;
  protected int foo;
  static int foo;

  // Constructor
  public Cat() {
    // ...
  }

  // methods
  public void greet() {
    // ...
  }
}
```

### Inheritance
```java
class Pepe extends Cat {
  @Override
  public void greet() {
    super(); // Call parent method
  }
}
```

### Interfaces
```java
public interface Animal {
  public void greet();
}

class Pepe implements Animal {
  // ...
}
```

### Abstracts Classes
```java
public abstract class Animal {
  // ...
}
```

### Final Classes
public final class Pepe {
  // ...
}
