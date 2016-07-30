# Problem 34
Calculate Euler's totient function phi(m).

Euler's totient function phi(m) is defined as the number of positive integers``` r (1 <= r < m)``` that are coprime with ```m```.

For example: 
>  if m = 10   
>  then totients of m = 1,3,7,9   
>  and phi of m = 4

Note the special case: phi(1) = 1.

## Unit Test
```
import Html 
import List


totient :  Int -> Int
totient a b = 
    -- your implementation here
    0

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
        [ ( totient 10, 4 )
        , ( totient 25, 20 )
        , ( totient 120, 32 )
        , ( totient 0, 0 )
        , ( totient 1600, 640)
        , ( totient 37, 36 )
        , ( totient 330, 80)
        , ( totient 65934, 19440)
        , ( totient 1313, 1200)
        , ( totient 45, 24)
        , ( totient -23, 0 )
        ]        
```
## Hints
1. Use ```coprime``` from [Problem 33](problem_33.md) with ```List.filter```.
## Solutions
[Solutions](problem_34_solutions.md)