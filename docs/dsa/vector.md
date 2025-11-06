# :material-lightning-bolt: Vector

## 🔍 Description
Un **Vector** est une version dynamique d’un **Array**.
Il permet de stocker des éléments contigus tout en **redimensionnant** automatiquement sa taille lors des insertions.

## ⚙️ Opérations principales et complexités

| Opération | Description | Complexité |
|------------|--------------|-------------|
| Accès | Lecture d’un élément via un index | O(1) |
| Recherche | Recherche d’une valeur donnée | O(n) |
| Insertion à la fin (`push_back`) | Ajout d’un élément à la fin | Amortie O(1) |
| Insertion/Suppression ailleurs | Nécessite un décalage | O(n) |

## :material-progress-star: Avantages
- Taille dynamique contrairement aux tableaux.
- Supporte de nombreuses méthodes utiles (e.g. `push_back`, `pop_back`, `size`).
- Compatible avec les algorithmes STL (`sort`, `find`, etc.).

## :material-progress-close: Inconvénients
- Réallocation possible (copie complète en mémoire).
- Moins performant qu’un tableau statique pour certaines opérations très bas niveau.

## :octicons-file-code-16: Exemple C++

```cpp title="vector.cpp"
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> v = {1, 2, 3};
    v.push_back(4);
    v.push_back(5);

    cout << "Taille: " << v.size() << endl;
    cout << "Dernier élément: " << v.back() << endl;

    for (int x : v)
        cout << x << " ";
    cout << endl;
}
```

## :fontawesome-solid-brain: LeetCode Challenges

| Difficulté | Titre | Lien |
|-------------|--------|------|
| :green_square: Easy | Move Zeroes | [**Link**](https://leetcode.com/problems/move-zeroes/) |
| :green_square: Easy | Best Time to Buy and Sell Stock | [**Link**](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) |
| :green_square: Easy | Contains Duplicate | [**Link**](https://leetcode.com/problems/contains-duplicate/) |
| :yellow_square: Medium | Container With Most Water | [**Link**](https://leetcode.com/problems/container-with-most-water/) |
| :yellow_square: Medium | Longest Substring Without Repeating Characters | [**Link**](https://leetcode.com/problems/longest-substring-without-repeating-characters/) |
| :yellow_square: Medium | Group Anagrams | [**Link**](https://leetcode.com/problems/group-anagrams/) |
| :yellow_square: Medium | Subarray Sum Equals K | [**Link**](https://leetcode.com/problems/subarray-sum-equals-k/) |
| :yellow_square: Medium | Sort Colors | [**Link**](https://leetcode.com/problems/sort-colors/) |
| :red_square: Hard | Median of Two Sorted Arrays | [**Link**](https://leetcode.com/problems/median-of-two-sorted-arrays/) |
| :red_square: Hard | Sliding Window Maximum | [**Link**](https://leetcode.com/problems/sliding-window-maximum/) |
