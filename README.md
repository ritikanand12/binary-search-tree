Check if a Binary Tree is a BST in C

This project implements a program in C to check whether a given binary tree satisfies the properties of a Binary Search Tree (BST) using the range (min–max) method.

📌 Description

A Binary Search Tree (BST) is a binary tree in which:

All nodes in the left subtree are less than the root node.

All nodes in the right subtree are greater than the root node.

Both left and right subtrees must also be BSTs.

This program verifies the BST property recursively using minimum and maximum value constraints.

🧠 Algorithm Used (Range Method)

The function isBST(root, min, max) works as follows:

If the node is NULL, return 1 (true).

If the node’s value is not within the range (min, max), return 0 (false).

Recursively check:

Left subtree with range (min, root->data)

Right subtree with range (root->data, max)

Return true only if both subtrees satisfy BST conditions.

📂 Code Structure
🔹 Structure Definition
struct Node {
    int data;
    struct Node *left, *right;
};

Each node contains:

data → value stored in node

left → pointer to left child

right → pointer to right child

🔹 Functions
newNode(int value)

Allocates memory for a new node

Initializes left and right pointers to NULL

isBST(struct Node* root, int min, int max)

Recursively checks whether the tree satisfies BST properties

🌳 Tree Used in Program

The tree created in main():

           50
         /    \
       30      70
      /  \    /  \
    20   40  60   80

This tree satisfies all BST properties.

▶️ Sample Output
Tree is a BST
⚙️ How to Compile and Run
1️⃣ Compile
gcc check_bst.c -o check_bst
2️⃣ Run
./check_bst
⏱️ Time & Space Complexity

Time Complexity: O(N)
(Each node is visited once)

Space Complexity: O(H)
(Recursive call stack, where H = height of the tree)

📚 Concepts Covered

Binary Tree

Binary Search Tree (BST)

Recursion

Min–Max Range Validation

Tree Traversal Logic

⚠️ Important Note

This implementation does not allow duplicate values in the BST.

Uses INT_MIN and INT_MAX from <limits.h> as initial range values.

👨‍💻 Author

Ritik Chauhan

If you want, I can also provide:

BST validation using Inorder Traversal

Menu-driven BST program (Insert, Delete, Search)

Comparison README (Normal Binary Tree vs BST)
