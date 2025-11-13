# :material-pine-tree: Binary Tree

## :material-magnify: Description
**Binary Tree** (arbre binaire) -> une structure de données hiérarchique où chaque **nœud** possède au maximum **deux enfants** : un **gauche (left)** et un **droit (right)**.

Les arbres binaires sont à la base de nombreuses structures avancées comme les **Binary Search Trees (BST)**, les **Heaps**, ou encore les **Segment Trees**.

Ils sont fondamentaux en algorithmique pour représenter des relations hiérarchiques, effectuer des recherches rapides, ou manipuler des structures récursives.

## :fontawesome-solid-list-check: Opérations principales et complexités

| Opération | Description | Complexité moyenne |
|------------|--------------|--------------------|
| Insertion | Ajout d’un nœud dans l’arbre | **O (log n)** |
| Recherche | Trouver un élément | **O (log n)** |
| Suppression | Retirer un nœud | **O (log n)** |
| Parcours (DFS/BFS) | Exploration complète | **O (n)** |

> ⚠️ Les complexités supposent un **arbre équilibré**.
> Dans le pire cas (arbre dégénéré), les opérations peuvent monter à **O(n)**.

## :material-progress-star: Avantages

- Structure récursive idéale pour représenter des hiérarchies ou relations ordonnées.
- Efficace pour la recherche, l’insertion et la suppression lorsqu’équilibré.
- Sert de base à de nombreuses structures optimisées (AVL, Red-Black Tree, Heap…).

## :material-progress-close: Inconvénients

- Peut devenir inefficace sans équilibrage.
- Nécessite une bonne compréhension de la récursivité.

## :octicons-file-code-16: Exemple C++

```title="Arbre Binaire"
    1
   / \
  2   3
 / \
4  5
```

??? "Template C++"

    ```cpp title="binary_tree.cpp"
    #include <queue>
    #include <iostream>

    using namespace std;

    // Data Structure
    struct Node {
            int val;
            Node* left;
            Node* right;

            Node(int x) : val(x), left(nullptr), right(nullptr) { }
    };

    // Traversals - Recursive
    void inorder(Node* root) {
        if (!root) return;

        inorder(root->left);

        cout << root->val << " ";

        inorder(root->right);
    }

    void preorder(Node* root) {
        if (!root) return;

        cout << root->val << " ";

        preorder(root->left);
        preorder(root->right);
    }

    void postorder(Node* root) {
        if (!root) return;

        postorder(root->left);
        postorder(root->right);
        cout << root->val << " ";
    }

    // Program
    int main() {
        // Instantiation
        Node* root = new Node(1);

        // Insertion
        root->left = new Node(2);
        root->right = new Node(3);
        root->left->left = new Node(4);
        root->left->right = new Node(5);

        cout << "Inorder traversal: ";
        inorder(root);
        cout << endl;

        cout << "Preorder traversal: ";
        preorder(root);
        cout << endl;

        cout << "Postorder traversal: ";
        postorder(root);
        cout << endl;

        return 0;
    }
    ```

🌲 Types de Parcours

|Type	|Description	|Exemple|
|-|-|-|
|Inorder |	Gauche → Racine → Droit	|4 2 5 1 3|
|Preorder |	Racine → Gauche → Droit	|1 2 4 5 3|
|Postorder |	Gauche → Droit → Racine|4 5 2 3 1|
|Level-order (BFS)|	Parcours niveau par niveau|	1 2 3 4 5|

## :fontawesome-solid-brain: LeetCode Challenges

|Difficulté	|Titre	|Lien|
|-|-|-|
| :green_square: Easy	|Maximum Depth of Binary Tree	| [**Link**](https://leetcode.com/problems/maximum-depth-of-binary-tree/)|
| :green_square: Easy	|Symmetric Tree	| [**Link**](https://leetcode.com/problems/symmetric-tree/)|
| :green_square: Easy	|Invert Binary Tree	| [**Link**](https://leetcode.com/problems/invert-binary-tree/)|
| :yellow_square: Medium	|Binary Tree Level Order Traversal	| [**Link**](https://leetcode.com/problems/binary-tree-level-order-traversal/)|
| :yellow_square: Medium	|Construct Binary Tree from Preorder and Inorder Traversal	| [**Link**](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)|
| :yellow_square: Medium	|Validate Binary Search Tree	| [**Link**](https://leetcode.com/problems/validate-binary-search-tree/)|
| :yellow_square: Medium	|Lowest Common Ancestor of a Binary Tree	| [**Link**](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)|
| :yellow_square: Medium	|Binary Tree Zigzag Level Order Traversal	| [**Link**](https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/)|
| :red_square: Hard	|Serialize and Deserialize Binary Tree	| [**Link**](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/)|
| :red_square: Hard	|Binary Tree Maximum Path Sum	| [**Link**](https://leetcode.com/problems/binary-tree-maximum-path-sum/)|
