# Elixir

## DataTypes

```elixir
0b1010 # Binaries
0o755 # Octals
0xFF  # Hex
6.57e-10 # Exp
"Hello" # String (bytes)
'Hełło' # Charlist (codepoints)
[1, 2, 3] # List
{ :foo, "bar" } # Tuple
%{ foo: "var" } # Map
<< 0, 1, 2 >> # Binaries
```
### Strings
```elixir
"Hello #{world}" # Interpolation
"Hello" <> "World" # Concatenate
```

### Lists
```elixir
++ # Concatenate
-- # Substract
hd # Head
tl # Tail
```

### Map
```elixir
# Declaration
%{ :a => 1, :b => 2 } == %{ a: 1, b: 2 }

# Access
map.a == Map.fetch(map, :a)

# Update
%{ map | :b => 3 }
```

## Pattern Matching
```elixir
# Lists
[head | tail] = [1, 2, 3]

# Pin Operator
^x = 2
```

## Control Flow

### Case
```elixir
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
```elixir
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
```elixir
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
```elixir
if true, do: 1 + 2, else: 1 + 3
```

## Functions and Modules

### Modules
```elixir
defmodule MyMath do
  # ...functions
end

# Alias
alias Math.List, as: Listing

# Import
import MyModule, only: [greet: 1]
import MyModule, only: :macros
import MyModule, except: [greet: 1]
import MyModule, except: :functions

# Require
require MyModule
```

### Functions
```elixir
def square(x \\ 2) do
  x * x
end

# Guards
def square(x) when x > 0 do
  x * x
end

# Inline
def inline_square(x), do: x * x

# Private
defp private_square(x), do: x * x end

# Anonymous
fn x -> x * 2 end
fn
  x, y when x > 0 -> x / 0
  x, y -> x + y
end

# Grab function
Enum.map([1, 2, 3], &Module.pow/1)
```


## Structs
```elixir
# Declaration
defmodule User
  @enforce_keys [:age]  # Required keys
  defstruct [:name, :age] # Without default values
  defstruct name: "John", age: 12
end

# Usage
%User{name: "Pedro", age: 23}
```
