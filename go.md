# Go

## Data types

```go
var x int

sum, prod := multiplesValues()
```
### Arrays
```go
numbers := [5]int # Basic declaration
numbers := [...]{1, 2, 3} # Calculated size
```

### Slices
Los slices funcionan bajo referencia, si no con copiados serán mutados

```go
numbers := []int
numbers[0:2]

// Methods
len(numbers)
cap(numbers)
append(numbers, 0)
append(numbers, numbers2...)
```

### Maps
```go
map[string]string


// Methods
delete(map, key)

// Retrieve if exsit
val, exist := colors["blue"]
```

## Control Flow
```go
if condition {
  // ...
} else if condition {
  // ...
}

switch foo {
  case condition:
    // ...
  default
   // ...
}
```

## Functions
```go
// Multi return
func function() {
  return val1, val2
}
```

## Bucles
```go
for i := 0; i < 10; i++

for sum < 1000
```
## Structs
```go
type Cat struct {
  name string,
  age int
}
```
### Methods
```go
// Value receiver
func (c Cat) SayHello() string{
  return "Hello"
}

// Pointer receiver
func (c *Cat) SayHello() string{
  return "Hello"
}
```

### Methods Sets
```go
Methods Receivers         Values
-----------------------------------
(t T)                     T and *T
(t *T)                    *T

```

### Type Embedding
```go
type user struct {
  name string
  email string
}

type admin struct {
  user
  roles []string
}
```

### Interfaces
```go
type notifier interface {
  notify()
}
```
