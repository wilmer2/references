# Elixir

## DataTypes

```
0b1010 # Binaries
0o755 # Octals
0xFF  # Hex
6.57e-10 # Exp
"Hello" # Strings
[1, 2, 3] # List
{ foo: 'bar' } # Tuple
```
### Strings
```
"Hello #{world}" # Interpolation
"Hello" <> "World" # Concatenate
```

### Lists
```
++ # Concatenate
-- # Substract
hd # Head
tl # Tail
```

## Pattern Matching
```
[head | tail] = [1, 2, 3]
^x = 2 # Pin operator for rebound
```

## Control Flow

### Case
```
case foo do
  pattern ->
    # Code
  pattern when bar > 0 ->
    # Extra condition
  ^bar ->
    # Pattern exisiting variable
  _ ->
    # Any
end
```

### Cond
```
cond do
  2 + 2 == 5 ->
    # ...
  2 * 2 == 3 ->
    # ...
  true ->
    # ...
end
```

### if and unless
```
if cond do
  # ...
else
  # ...
end

unless cond do
  # ...
end
```

### do/end blocks
```
if true, do: 1 + 2, else: 1 + 3
```

## Functions and Modules

### Modules
```
defmodule MyMath do
  # ...functions
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
# Anonymous
fn x, y -> x * 2 end

# Anonymous with guards
fn
  x, y when x > 0 -> x / 0
  x, y -> x + y
end

# Shortcut
&(&1 * &1) # Shorter syntax
```

### Grabbing functions
```
Enum.map([1, 2, 3], &Module.pow/1)
```
