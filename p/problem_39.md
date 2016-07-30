# Problem 39

Construct a list of all prime numbers within a range of integers. 

Example:
```
primesInRange 10 20 == [11,13,17,19]
```
## Unit Test

```
import Html 
import List


primesInRange : Int -> Int -> List Int
primesInRange low high =
    -- your implementation here
    []               
               
main =
    Html.text
        (if (test) then
            "Your implementation passed all tests."
         else
            "Your implementation failed at least one test."
        )


test : Bool
test =
    List.all (\(result, expect) -> result == expect)
        [ ( primesInRange 36, (0,0) )
        , ( primesInRange 10, (0,0) )
        , ( primesInRange -1, (0,0) )
        , ( primesInRange 1, (0,0) )
        , ( primesInRange 0, (0,0) )
        , ( primesInRange 120, (0,0) )
        , ( primesInRange 4, (0,0) )
        , ( primesInRange 24, (0,0) )
        ]     
```

##Hints
1. Modify the solution from [Problem 31](problem_31.md). 

## Solutions
[Solutions](problem_39_solutions.md) 