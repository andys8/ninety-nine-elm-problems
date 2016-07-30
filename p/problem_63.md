# Problem 63

We define a complete binary tree with height H as a tree where:
* levels 1,...,H-1 contain the maximum number of nodes, 
* and in level H all the nodes are "left-adjusted". 

Heaps commonly use complete binary trees as data structures or addressing schemes. We can assign an address to each node in a complete binary tree by enumerating the nodes in level-order starting at the root with number 1. For every node ```X``` with address ```A``` the following holds: The address of ```X```'s left and right successors are ```2*A``` and ```2*A+1```, respectively, if they exist. This fact can be used to elegantly construct a complete binary tree structure.
```
import Html exposing (text)


type Tree a
    = Empty
    | Node a (Tree a) (Tree a)


completeTree : Int -> a -> Tree a
completeTree count value =
-- your implementation goes here


main =
    text
        <| toString
        <| completeTree 4 'x'
  
```
Result
```
Tree 'x' (Tree 'x' (Tree 'x' Empty Empty) Empty) (Tree 'x' Empty Empty)

```
