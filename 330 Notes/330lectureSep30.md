just practice w/ trees

```OCaml
type int_tree = Leaf | Node of int * int_tree * int_tree ;;

let tree1 = Leaf;;
let tree2 = Node(5, Node(2, Leaf, Leaf), Node(6, Leaf, Leaf));;

let max x y = if x > y then x else y;;

let rec height tree = match tree with 
    Leaf -> 0
  |Node(_, left, right) -> 1 + max (height left) (height right);;


(*make a list of left, node, right*)

let rec tree_to_list tree = 
  let rec tree_to_list_helper tree acc = match tree with
      Leaf -> acc
    | Node(n,left, right) ->  tree_to_list_helper left (n :: (tree_to_list_helper right acc))
  in tree_to_list_helper tree[];; 
  
  (* append (tree_to_list left) node (tree_to_list right) *)


  
let rec max_tree tree acc = match tree with
    Leaf -> acc
  | Node(n, l, r) -> 
      if n > acc then max (max_tree l n) (max_tree r n) else max (max_tree l acc) (max_tree r acc)



let rec insert key tree = match tree with
    Leaf -> Node(key, Leaf, Leaf) (*let, node, right , we added key to leaf*)
  | Node(n, l, r) -> 
      if key < n then insert key l else insert key r 
                                


```