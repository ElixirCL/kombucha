# 🍹The Kombucha Programming Language

[Kombucha](https://en.wikipedia.org/wiki/Kombucha) is a experimental programming language.
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
- All functions within a _module_ are private by default (defined with `fun`). Must be made public explicitly with `pub` keyword.
- Can have constants with `const` keyword.
- `module` instead of `defmodule`.
- `struct` instead of `defstruct`.
- `macro` instead of `defmacro`.
- `guard` instead of `defguard`.
- `/*` and `*/` multiline comments.
- Curly braces `{}` for blocks instead of `do` and `end`.
- `$myfunc()` instead of `myfunc.()` for anonymous functions.

## Why?

Is a simple parser implemented in _Elixir_. Maybe it can help learners or a good exercise.

## License

![MPLv2](https://img.shields.io/badge/License-MPL%20v2-blue.svg)

## Credits

![Proudly Coded in - 🇨🇱 Chile](https://img.shields.io/badge/Proudly_Coded_in-🇨🇱_Chile-white?style=for-the-badge)
![Made With ❤️ By - Ninjas.cl](https://img.shields.io/badge/Made_With_❤️_By-Ninjas.cl-2ea44f?style=for-the-badge)
