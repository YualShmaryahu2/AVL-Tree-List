AVLNode Class:
The AVLNode class is class that executes nodes. Each node has a “real” child (left,right) or a virtual one. 
Every node has a parent but in this case the father could be None. Unlike many cases, there is no key in 
this class but the rest is the as every node discussed in class. 
Methods: 
getLeft() : returns the left child of a node. O(1)
getRight(): returns the right child of a node. O(1)
getParent(): returns the parent of a node. O(1)
getValue(): returns the value of a node. O(1)
getHeight(): returns the height of a node. O(1)
getSize(s): returns the size of a node. O(1)
setLeft(new_node): sets the left child of a node to new_node .O(1)
setRight(new_node): sets the right child of a node to new_node .O(1)
setParent(new_node): sets the parent of a node to new_node. O(1)
setValue(value): sets the value of a node to value. O(1)
setHeight(h): sets the height of a node to h. O(1)
setSize(size): sets the size of a node to size. O(1)
min(): returns the first node that does not have a left child. Under the assumption that we operate on 
AVL Tree list the method iterates at most O(logN) times and in each iteration we operate getLeft() - O(1). 
So – O(logN)
max(): returns the first node that does not have a right child. Under the assumption that we operate on 
AVL Tree list the method iterates at most O(logN) times and in each iteration we operate getRight() -
O(1). So – O(logN)
getPredecessor(): returns the predecessor the same as we did in class. the only action in each iteration is 
when we operate getParent(). Under the assumption that we operate on AVL Tree list the method 
iterates at most O(logN) times and in each iteration we operate getParent() - O(1). So – O(logN). O(logN)
getSuccessor(): returns the successor the same as we did in class. the only action in each iteration is 
when we operate getParent(). Under the assumption that we operate on AVL Tree list the method 
iterates at most O(logN) times and in each iteration we operate getParent() - O(1). So – O(logN). O(logN)
isRealNode(): return whether the node is real or virtual. O(1)
getBalanceFactor() : return the height of its left node minus the height of its right node. O(1)
AVLTreeListClass:
rotations_counter(): returns the number of rotations the tree had executed so far. O(1)
select(i), Tree_select_rec(node,i): select calls to Tree_select_rec(root,i): with root and i (index). This 
method executes the same as select from the class. There fore it’s O(logN).
empty(): returns whether the root is real node. O(1)
getTreeRoot(): returns the root of the class. O(1)
getVirtualNode(): returns a virtual node. The virtual node is being created when the constructor is being 
called. It has height of -1 and represents “None”. O(1)
retrieve(): returns the value of the node in the i’th index. O(log(i)
Insert(): Inserts val at position I in the list. O(log(n))
Delete(): Step A: we find the item using select, let’s call it x. Let P be the parent of x. We delete x from 
the tree the same way as BST and move to step B with p. O(logn)
Step B: we iterate every parent of the node and if the parent has balance factor == 2 or == -2. We 
perform a rotation as needed. We keep doing so with p.parent until we get to the root. As explained in 
the class this is O(logn)
First(): returns the value of the firstNode in the list, using firstNode(). O(log(n)) 
Last(): returns the value of the firstNode in the list, using lastNode(). O(log(n))
firstNode(): returns the first Node in the list, by going down on the left spine of the tree. O(log(n))
LastNode(): returns the last Node in the list, by going down on the right spine of the tree. O(log(n))
listToArray(): returns an array representing list, using recursion- like in order traversal we saw in class. 
O(n)
length(): the length of the list is the size of the root. The method returns it. O(1) 
sort(): return a new tree of the same list but sorted. For sorting the list, the method uses mergesort 
algorithm (that is implemented in the class) . O(nlog(n))(mergesort) + O(log(n))(inserts) = O(nlog(n))
permutation(): Using Listtoarray we create an array with the value of the list. Then, with the help of 
fisher yeate algorithm we shuffle the array. In order to create the tree it uses a method 
creattreeinlineartime() that takes O(n) that operates the same way as creating AVL tree from a sorted 
array as explained in the class .O(N)
concat(): Concat the list given as a paremeter to self list. In order to do so we find the differences 
between the heights of the lists. If self height>=another height we iterate to the right node of self root 
until we find the first node whose height is <= than the another list, let’s call this node first_node and 
the subtree of it T1. We create a new node , let’s call it x. Then, we join(T1,T2,X) as explained int the 
class. After that, we update the height and size of every parent starting from x and perform a rotation if 
needed. As Explained in the class all of this takes O(logn).
If self height<another height , we iterate to the left node of self root until we find the first node whose 
height is <= than the self list height. let’s call this node first_node and the subtree of it T1. We create a 
new node , let’s call it x. Then, we join(T1,T2,X) as explained int the class. After that, we update the 
height and size of every parent starting from x and perform a rotation if needed. As Explained in the 
class all of this takes O(logn).
makeNewTree(): creates new tree in O(1)
search(): return the first index that contains val (-1 if not found). O(n)
getRoot(): returns the root of the tree. O(1)
fixSize(): fixing the sizes of a node and its parents(by adding 1) (going up to the root) after inserting new 
node. O(log(n))
fixSizeDelete(): fixing the sizes of a node and its parents(by decreasing 1) (going up to the root) after 
inserting new node. O(log(n))
fix_and_rotate(): This is an important method used to balance the tree after operations like insert delete 
and concat. The method finds out in which balance factor situation the tree is in and calls the needed 
rotations if necessary. The method works in O(1) 
rightRotation(): rotates the subtree by changing some of the pointers as we saw in class in O(1)
leftRotation(): rotates the subtree by changing some of the pointers as we saw in class in O(1)
UpdateParentsHeight():updates the node’s parents height adding 1 when needed(checked by balance 
factor) O(log(n)) in case the root is the last one to update.
updateParentsHeightDelete(): Updating the height of every node after deletion. O(logn)
setRoot(): sets the root of a tree. O(1)
merge(),def mergesort(): As explained ins cs 1001, sorting a list using mergesort technique. O(1)
createtreeinlineartime(): Create tree using recursion from “sorted” array. As explained in class we create 
an AVL tree with O(n)
height_fixer(): going to “leftist” node in the tree and update all of it’s parent heights.O(logn)
Randomize() : function that returns a randomize array using Fisher Yates algorithm. O(n)
Balanceheightandsize(): balance height and size of node and all of its parent. O(logn)
