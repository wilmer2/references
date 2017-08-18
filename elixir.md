# Elixir

## DataTypes

```
0b1010 # Binaries
0o755 # Octals
0xFF  # Hex
6.57e-10 # Exp
```

### Strings
```
.reverse/1
.length/1
.at/2
```

### Lists
```
++ # Concatenate
-- # Substract
hd/1 # Head
tl/1 # Tail
```

### Ranges
```
1..50
```

### Tuples
```
{ 1, "hello", :ok }
tupe_size(tuple) # 1: tuple
elem(tuple, index)
put_elem(tuple, index, el)
```

## Functions and Modules

### Modules
```
defmodule MyMath do
  ...functions
end
```

### Functions
```
def square(x) do
  x * x
end
```

### Functions inline
```
def inline_square(x), do: x * x
```

### Private functions

```
defp private_square(x) do
  x * x
end
```

### Anonymous Functions
```
fn x -> x * 2 end # Anonymous
&(&1 * &1) # Shorter syntax
```

### Grabbing functions
```
Enum.map([1, 2, 3], &Module.pow/1)
```
