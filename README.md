# 🍹The Kombucha Programming Language

Kombucha is a experimental programming language.
A combination between [Elixir](https://elixir-lang.org/) and [Gleam](https://gleam.run/).

```elixir
module Brew {
  pub strong() {
    "This is a Kombucha Brewed in 30 days!"
  }
}
Brew.strong()
```

## Features

- Transpiles down to _Elixir_. Is essentially _Elixir_ with some _Gleam_ ideas on top.
- All functions within a _module_ are private by default. Must be made public explicitly with `pub` keyword.
- Can have constants with `const` keyword.
- `module` instead of `defmodule`.
- `struct` instead of `defstruct`.
- `macro` instead of `defmacro`.
- `/*` and `*/` multiline comments.
- Curly braces `{}` for blocks instead of `do` and `end`.
