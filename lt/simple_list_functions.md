# Simple List functions
Let's learn some basic functions from the ```List``` module.
##Problem 6
```
isPalindrome' : List a -> Bool
```
Solve [Problem 6](problem_6.md) using ```List.reverse```.
##Problem 17
```
split : List a -> Int -> (List a, List a)
```
Solve [Problem 17](problem_17.md) using ```List.take``` and ```List.drop```.
##Problem 18
```
sublist : List a -> Int -> Int-> List a
```
Solve [Problem 18](problem_18.md) using ```List.take``` and ```List.drop```.
##Problem 20
Use List.take, List.drop and the append operator (++).
```
dropAt : List a -> Int -> List a
```
Solve [Problem 20](problem_20.md) using ```List.take``` and ```List.drop``` and the append operator (++) or ```List.append```.
##Problem 19
```
rotate : List a -> Int -> List a
```
Solve [Problem 19](problem_19.md) using ```List.take``` and ```List.drop``` and the append operator ```(++)``` or ```List.append```.
##Problem 21
```
insertAt : List a -> Int -> a -> List a
```
Solve [Problem 19](problem_19.md) using ```List.take```, ```List.drop```, append operator ```(++)``` and the "cons" operator ```(::)```. You may want to use split from [Problem 17](problem_17.md).