# Go

## Data types

```go
const x = 25
var a, b int

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

### Conditionals
```go
if condition {
  // ...
} else if condition {
  // ...
}

// With declaration
if v := n + 1; n < 5 {
  // ...
}

switch foo {
  case condition:
    // ...
  case value + 5:
    // ...
  default
   // ...
}
```

### Bucles
```go
for i := 0; i < n i ++ {
  // ...
}

for count < 500 {
  // ...
}

// Forever
for {
  // ...
}

// Iterate over slices and maps
for i, v := range numbers {
  // ...
}

```


## Functions
```go
func function(a, b int) (sum, multi int) {
  return a + b, a * b
}
```

### Defer
Call a function before return, can have more than one


## Structs
```go
type Cat struct {
  name string,
  age int
}
```
## Methods
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

## Concurrancey

### Atomic functions
```go
atomic.AddInt64(&counter, 1)
atomic.StoreInt64(&shutdown, 23)
atomic.LoadInt64(&shutdown)
```

### Mutex
```go
mutex.Lock() {
  // ...code
}

mutex.Unlock()
```
### Channels
```go
unbuffered := make(chan int)
buffered := make(chan string, 10)

// Methods
unbufferred <- 1 // Add data to channel
data, ok := <- unbuffered // Get data from channel
close(unbuffered)
```

#### Passing channel as param
```go
func (c chan int) {
  //...code
}
```
