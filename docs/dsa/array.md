# 🧩 Array

## 🔍 Description
Un **Array** (ou tableau) est une structure de données contiguë qui stocke des éléments de même type en mémoire.
Chaque élément est accessible directement via son **index**, ce qui rend la lecture très rapide.

## ⚙️ Opérations principales et complexités

| Opération | Description | Complexité |
|------------|--------------|-------------|
| Accès | Récupère un élément à un index donné | O(1) |
| Recherche | Parcourt le tableau pour trouver une valeur | O(n) |
| Insertion / Suppression | Nécessite un décalage des éléments | O(n) |

## :material-progress-star: Avantages
- Accès direct en O(1) grâce à l’indexation.
- Très rapide pour les lectures séquentielles.
- Simplicité d’utilisation et faible overhead mémoire.

## :material-progress-close: Inconvénients
- Taille fixe, non redimensionnable après allocation.
- Insertion/suppression coûteuses.

## :octicons-file-code-16: Exemple C++

```cpp title="array.cpp"
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};

    cout << "Premier élément: " << arr[0] << endl;
    cout << "Dernier élément: " << arr[4] << endl;

    for (int i = 0; i < 5; i++)
        cout << arr[i] << " ";
    cout << endl;
}
```

## :fontawesome-solid-brain: LeetCode Challenges

| Difficulté | Titre | Lien |
|-------------|--------|------|
| :green_square: Easy | Two Sum | [**Link**](https://leetcode.com/problems/two-sum/) |
| :green_square: Easy | Remove Duplicates from Sorted Array | [**Link**](https://leetcode.com/problems/remove-duplicates-from-sorted-array/) |
| :green_square: Easy | Merge Sorted Array | [**Link**](https://leetcode.com/problems/merge-sorted-array/) |
| :yellow_square: Medium | Maximum Subarray | [**Link**](https://leetcode.com/problems/maximum-subarray/) |
| :yellow_square: Medium | Rotate Array | [**Link**](https://leetcode.com/problems/rotate-array/) |
| :yellow_square: Medium | Product of Array Except Self | [**Link**](https://leetcode.com/problems/product-of-array-except-self/) |
| :yellow_square: Medium | Set Matrix Zeroes | [**Link**](https://leetcode.com/problems/set-matrix-zeroes/) |
| :yellow_square: Medium | 3Sum | [**Link**](https://leetcode.com/problems/3sum/) |
| :red_square: Hard | Trapping Rain Water | [**Link**](https://leetcode.com/problems/trapping-rain-water/) |
| :red_square: Hard | Merge k Sorted Lists | [**Link**](https://leetcode.com/problems/merge-k-sorted-lists/) |
