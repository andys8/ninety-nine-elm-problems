# Problem 9

Convert a list to a list of lists where repeated elements of the source list are packed into sublists. Elements that are not repeated should be placed in a one element sublist.

##Example
```
pack [1,1,1,2,3,3,3,4,4,4,4,5,6,6] ==
    [ [1,1,1]
    , [2]
    , [3, 3, 3]
    , [4, 4, 4, 4]
    , [5]
    , [6, 6]
    ]
```

##Unit Test
```elm

import Html exposing (text)
import List 


pack : List a -> List (List a)
pack xs =
    -- your implementation goes here
    [[]]


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
        [ pack [1, 1, 1, 1, 2, 5, 5, 2, 1] == [[1, 1, 1, 1], [2], [5, 5], [2], [1]]
        , pack [2, 1, 1, 1] == [[2], [1, 1, 1]]
        , pack [2, 2, 2, 1, 1, 1] == [[2, 2, 2], [1, 1, 1]]
        , pack [1] == [[1]]
        , pack [] == [[]]
        , pack [ "aa", "aa", "aa" ] == [ ["aa", "aa", "aa"] ]
        , pack [ "aab", "b", "b", "aa" ] == [ ["aab"], ["b", "b"], ["aa"] ]
        ]
```

## Hints
1. Solve [Problem 17](problem_17.md). See if you can create variants of the core List functions you used in Problem 17 to solve this problem. 

## Solutions
[Solutions](problem_9_solutions.md)