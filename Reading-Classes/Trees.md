# <span style="color:Violet "> Trees </span>
## <span style="color:DarkSeaGreen"> What is a Tree Data Structure in Python? </span>
A Tree is a Data structure in which data items are connected using references in a hierarchical manner. 
Each Tree consists of a root node from which we can access each element of the tree. Starting from the root node, 
each node contains zero or more nodes connected to it as children. A simple binary tree can be depicted as seen in the 
following figure.

![Trees](https://www.pythonforbeginners.com/wp-content/uploads/tree1.png)

## <span style="color:DarkSeaGreen"> Parts of a Tree Data structure </span>

A tree consists of a root node, leaf nodes and internal nodes. 
Each node is connected to its chile via a reference, which is called an edge.

**Root Node**: Root node is the topmost node of a tree. It is always the first node created while creating the tree, 
and we can access each element of the tree starting from the root node. 
In the above example, the node containing element 50 is the root node.

**Parent Node**: The parent of any node is the node which references the current node. In the above example, 
50 is the parent of 20 and 45, 20 is parent of 11, 46 and 15. 
Similarly, 45 is the parent of 30 and 78.

**Child Node**: Child nodes of a parent node are the nodes at which the parent node is pointing using the references. 
In the example above, 20 and 45 are children of 50. 
The nodes 11, 46, and 15 are children of 20 and 30 and 78 are children of 45.

**Edge**: The reference through which a parent node is connected to a child node is called an edge. 
In the above example, each arrow that connects any two nodes is an edge.

**Leaf Node**: These are those nodes in the tree which have no children. 
In the above example, 11, 46, 15, 30, and 78 are leaf nodes.

**Internal Nodes**: Internal Nodes are the nodes which have at least one child. 
In the above example, 50, 20 and 45 are internal nodes.

## <span style="color:DarkSeaGreen">Inserting into a Tree </span>
To insert into a tree we use the same node class created above and add an insert class to it. 
The insert class compares the value of the node to the parent node and decides to add it as a left node or a right node.
Finally, the PrintTree class is used to print the tree.

## Example
     class Node:
         def __init__(self, data):
            self.left = None
            self.right = None
            self.data = data

         def insert(self, data):
         # Compare the new value with the parent node
           if self.data:
             if data < self.data:
                if self.left is None:
                     self.left = Node(data)
                else:
                     self.left.insert(data)
            elif data > self.data:
               if self.right is None:
                  self.right = Node(data)
               else:
                  self.right.insert(data)
           else:
               self.data = data

          # Print the tree
          def PrintTree(self):
            if self.left:
               self.left.PrintTree()
               print( self.data),
            if self.right:
               self.right.PrintTree()

         # Use the insert method to add nodes
         root = Node(12)
         root.insert(6)
         root.insert(14)
         root.insert(3)
         root.PrintTree()

        Output : 3 6 12 14


## <span style="color:DarkSeaGreen"> Traversing a Tree </span>
The tree can be traversed by deciding on a sequence to visit each node. 
As we can clearly see we can start at a node then visit the left sub-tree first and right sub-tree next. 
Or we can also visit the right sub-tree first and left sub-tree next. 
Accordingly there are different names for these tree traversal methods.


