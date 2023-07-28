# The Kombucha Programming Language

```elixir
defmodule Kombucha do
  defp transform(token) do
      case token do
          "module" <> rest -> "defmodule" <> rest
          "{" <> rest -> "do" <> rest
          "}" <> rest -> "end" <> rest
          "pub" <> rest -> "def" <> rest
          token -> token
    end
  end

  defp tokenize(input) do
    input 
    |> String.trim()
    |> String.replace("\n", " \n ")
    |> String.split(~r/(?<=[()\s;=+\-*\/]|[()])/)
    |> Enum.filter(&(&1 != "" && &1 != " "))
    |> Enum.map(&(transform(&1)))
    |> Enum.join()
    |> Code.eval_string()
    |> then(fn {result, _} -> result end)
  end

  def eval(input), do: tokenize(input)
end
```

```elixir
Kombucha.eval("""
module Brew {
  pub strong() {
    "This is a Kombucha Brewed in 30 days!"
  }
}
Brew.strong()
""")
```
