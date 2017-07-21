### Variables

```go
var x int

sum, prod := multiplesValues()
```

### Conditionals
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

### Functions
```go
// Multi return
func function() {
  return val1, val2
}
```

### Bucles
```go
for i := 0; i < 10; i++

for sum < 1000
```

### Struct

```go
type Cat struct {
  name string,
  age int
}
```

### Arrays

```go
var numbers []int

numbers[0:2]

len(numbers)
cap(numbers)
append(numbers, 0...)
i, v := range(numbers)
```


### Maps
```go
var [string]Cat

delete(map, key)
```

### Methods
```go
func (c Cat) SayHello() string{
  return "Hello "
}
```
