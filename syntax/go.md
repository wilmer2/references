# Go

## Declarations

```go
var foo int
var foo int = 42
var foo, bar int = 42, 104
foo := 42
const foo int
```

## Built-in Types
```go
bool
string
int int8 int16 int32 int64
uint uint8 uint16 uint32 uint64
byte // alias for uint8
float32 float64
complex64 complex128
```

### Arrays
```go
var foo [2]int // Declare only
var foo = [2]int{42, 104} // Declare and initialize
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

### If
```go
if condition {
  // ...
} else if condition {
  // ...
}

// With declaration
if v := n + 1; condition {
  // ...
}
```

### Switch
```go
switch foo {
  case "foo":
    // ...
  default
   // ...
}

// With declaration
switch v := n + 1; v {
   v > 25:
    // ...
}
```

### For
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

## Concurrency

### Goroutine
```go
go greet() // Start routine
```

### WaitGroup
```go
var wg sync.WaitGroup
wg.add(n)

go func() {
  defer wg.Done()
}

wg.Wait()
```

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
unbuff := make(chan int)
buff := make(chan string, 10)

// Adding data
unbuff <- data

// Receiving data
data := <- unbuff // Wait for data and assignate

// Closing
close(channel)
```

#### Passing channel as param
```go
func (c chan int) {
  //...code
}
```
