# Basics of Elixir

## Functional language
Uses lots of functions
```iex> greeting = fn (place) -> "Hello, #{place}!" end````

## Maps
Are like hashes in Ruby, but with % sign in front
```iex> person = %{"name" => "Roberto", "age" => 56, "gender" => "Male"}
%{"age" => 56, "gender" => "Male", "name" => "Roberto"}```
