# Binary Trees 
#### Common Terminology
Node - A node is the individual item/data that makes up the data structure
Root - The root is the first/top Node in the tree
Left Child - The node that is positioned to the left of a root or node
Right Child - The node that is positioned to the right of a root or node
Edge - The edge in a tree is the link between a parent and child node
Leaf - A leaf is a node that does not contain any children
Height - The height of a tree is determined by the number of edges from the root to the bottommost node

#### Traversals
An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

###### Depth First 
 Depth first traversal is where we prioritize going through the depth (height) of the tree first. 
 - three methods for depth first traversal:
 Pre-order: `root >> left >> right`
In-order: `left >> root >> right`
Post-order: `left >> right >> root`
###### Breadth First
Breadth first traversal iterates through the tree by going through each level of the tree node-by-node
#### Binary Search Trees
A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

