


### Functional Programming Concepts <sup><img src="../images/602px-Haskell-Logo.svg.png" width=37 height=26><img></sup>

|  operator   |   Haskell Type <sup><img src="../images/602px-Haskell-Logo.svg.png" width=37 height=26><img></sup>   |  Elm Type <sup><img src="../images/elm-logo.png" width=28px height=28px><img></sup> |
|:-----------:|-------------------------------------------------------|------------|
| `$`         |  `($) :: (a -> b) -> a -> b`                          | `(<\|) <function> : (a -> b) -> a -> b` |
| `.`         |  `(.) :: (b -> c) -> (a -> b) -> a -> c`              | `(<<) <function> : (b -> c) -> (a -> b) -> a -> c` |
| `<>`        |  `(<>) :: Semigroup a => a -> a -> a`                 |          |




## REPL

### Haskel <sup><img src="../images/602px-Haskell-Logo.svg.png" width=37 height=26><img></sup> `ghci`

```
ghci> :type ($)
($) :: (a -> b) -> a -> b
```

### Elm <sup><img src="../images/elm-logo.png" width=28px height=28px><img></sup> `elm-repl`

```
> (<|)
<function> : (a -> b) -> a -> b
```

## Examples

- [X] Application Operator `$`

Elm <sup><img src="../images/elm-logo.png" width=28px height=28px><img></sup>

```
> List.map (\x -> x+1) <| [1,2,3,4]
```

Haskel <sup><img src="../images/602px-Haskell-Logo.svg.png" width=37 height=26><img></sup> 

```
ghci> fmap (\x -> x+1) $ [1,2,3,4]
```

```
> List.map ((\x -> x+1) >> (\x -> x+2)) [1,2,3,4] 
[4,5,6,7] : List number
```

|  operator   |   Haskell Type <sup><img src="../images/602px-Haskell-Logo.svg.png" width=37 height=26><img></sup>   |  Elm Type <sup><img src="../images/elm-logo.png" width=28px height=28px><img></sup> |
|:-----------:|-------------------------------------------------------|------------|
| `$`         |  `fmap (\x -> x+1) $ [1,2,3,4]`                          | `> List.map (\x -> x+1) <| [1,2,3,4]` |