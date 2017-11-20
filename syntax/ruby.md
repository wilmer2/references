# Ruby

## Control Flow

### Conditionals
```ruby
if cnd and cnd2
  # ...
elsif cnd3
  # ...
end

unless cnd
  # ...
end

case foo
  when cnd
    # ...
  else
    # ...
end
```

### Bucles
```ruby
for i in 1..5 do
  # ...
end

while cnd do
  # ...
end

begin
  # ...
end while cnd
```

### Guard Clause
```ruby
puts "Hello" if cnd
```

## Functions
```go
def foo(a, b, *args)
  # ...
end
```

### Lambdas
```go
lmd = -> (name) { puts name }
```
### Aliases
```ruby
def foo()
  # ...
end

alias var foo
```

## Blocks
```ruby
def foo(&b)
  b.call()
end

def foo
  yield
end
```

## Classes

```ruby
class Pug < Dog
  attr_reader :var
  attr_accessor :fee
  attr_writer :sim

  def initialize(foo)
    @foo = foo
  end

  def foo=(value)
    @foo = "parsed #{value}"
  end

  private

  def calc
    # ...
  end

  protected

  def operate
    # ...
  end
end
```

## Errors
```ruby
begin
  raise UnknownError, 'Yep one error'
rescue UnknownError
  # ...
end
```
