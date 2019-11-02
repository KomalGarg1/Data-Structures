# Data-Structures
Create a BST (Binary search tree).
Class BST
{
static class Node
{
int data;
Node left,right;
Node(int d)
{
data =d;
left = null;
right = null;
}
}
public Node insert(Node root, int key)
{
if(root==null)
return new Node(key);
else
{
if(key<root.data)
{
root.left = insert(root.left, key);
}
else
{
root.right = insert(root.right, key);
}
}
return root;
}
public static void inorder(Node root)
{
if(root ==null)
return;
inorder(root.left);
System.out.print(root.data + " ");
inorder(root.right);
}
public static void main(String args[])
{
Node root = null;
int a[]= {8,3,10,1,6,14,4,7,13}
for(int key:a)
{
root= insert(root, key);
}
inorder(root);
}
}
