# Problem 48
Write a function that can take any number of boolean variables
```
import Html exposing (text)

truthTableN : Int -> ([Bool]) -> String 
-- your implementation goes here

main = 
  text 
  <| toString 
  <| truthTableN 3 (\[a,b,c] -> a and' (b or' c) equ' a and' b or' a and' c)

```

Result
```
True  True  True  True
True  True  False True
True  False True  True
True  False False True
False True  True  True
False True  False True
False False True  True
False False False True
```
