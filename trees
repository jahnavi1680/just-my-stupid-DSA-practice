This is a second readme file.
I am trying to understand Data structures in this one. Since I already understand liner data structures, this is gonna start with Binary trees.

print("Try Binary tree dfs traversals")
class Node():
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
class BinaryTree():
    def __init__(self,root):
        self.root = Node(root)
    def preorder_print(self,start,traversal):
        if start:
            traversal += str(start.value) + "-"
            traversal = self.preorder_print(start.left,traversal)
            traversal = self.preorder_print(start.right,traversal)
        return traversal
    def inorder_traversal(self,start,traversal):
        if start:
            traversal = self.inorder_traversal(start.left,traversal)
            traversal += str(start.value) + "-"
            traversal = self.inorder_traversal(start.right,traversal)
        return traversal
    def postorder_traversal(self,start,traversal):
        if start:
            traversal = self.postorder_traversal(start.left,traversal)
            traversal = self.postorder_traversal(start.right,traversal)
            traversal += str(start.value) + "-"
        return traversal
tree = BinaryTree(1)
tree.root.left = Node(2)
tree.root.right = Node(3)
tree.root.left.left = Node(4)
tree.root.left.right = Node(5)
tree.root.right.left = Node(6)
tree.root.right.right = Node(7)
tree.root.right.right.right = Node(8)
print(tree.preorder_traversal(tree.root,""))


