# Problem 2

Implement the function ```penultimate``` to find the next to last element of a list.

##Example
```
  penultimate [1..4] == Just 3
```

## Unit Test
```elm
import Html exposing (text)
import List
import Maybe


penultimate : List a -> Maybe a
penultimate xs =
    -- your implementation goes here
    Nothing


main =
    text
        (if (test) then
            "Your implementation passed all tests."
         else
            "Your implementation failed at least one test."
        )


test : Bool
test =
    List.all ((==) True)
        [ penultimate [1..4] == Just 3 
        , penultimate [ 1, 2 ] == Just 1 
        , penultimate [ 1 ] == Nothing 
        , penultimate [] == Nothing 
        , penultimate [ "a", "b", "c" ] == Just "b" 
        , penultimate [ "a" ] == Nothing 
        ]
```

## Hints
Here are a hints for two different solutions.
1. Use recursion.
2. What can you to a list to make [List.head](http://package.elm-lang.org/packages/elm-lang/core/1.0.0/List#head) solve this problem? 

##Solutions 
[Solutions](problem_2_solutions.md)