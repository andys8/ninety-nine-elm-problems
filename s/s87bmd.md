# Problem 87b Solution

```elm
{-| Given a graph and a starting node, return all nodes in depth-first order.
-}
breadthFirst : comparable -> Graph comparable -> List comparable
breadthFirst start (nodes, edges) =
    breadthFirst' [start] [] (nodes, edges)


{-| Helper function for breadthFirst that recordes visited nodes to avoid
    cyclic paths.
-}
breadthFirst' : List comparable -> List comparable -> Graph comparable -> List comparable
breadthFirst' unvisited visited ( nodes, edges ) =
    case unvisited of
        [] ->
            visited
           
        u::us ->
            let
                nextNodes = unique
                    <| List.map (snd)
                    <| (++) (List.filter (\( a, b ) -> a == u) edges)
                    <| List.map (\x -> ( snd x, fst x ))
                    <| List.filter (\( a, b ) -> b == u) edges

                newNodes = List.sort
                    <| List.filter (\x -> not (List.member x (u::visited))) nextNodes
            in
                breadthFirst' (remove u (unvisited ++ newNodes)) (visited ++ [u]) (nodes, edges)


remove : a -> List a -> List a
remove x =
  List.filter ((/=) x)
  

{-| Given a list, return all unique values in the list.
-}
unique : List comparable -> List comparable
unique list =
    Set.toList <| Set.fromList list

```
[Back to problem](../p/p87.md)
