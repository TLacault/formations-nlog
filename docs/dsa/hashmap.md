# 🗺️ Hash Map

## 🔍 Description
Une **Hash Map** (ou `unordered_map` en C++) est une structure de données associant **clé → valeur**.
Elle repose sur une **fonction de hachage** permettant un accès **quasi-instantané** aux éléments.

## ⚙️ Opérations principales et complexités

| Opération | Description | Complexité moyenne |
|------------|--------------|--------------------|
| Insertion | Ajout d’une paire clé/valeur | O(1) |
| Recherche | Accès à la valeur via la clé | O(1) |
| Suppression | Retrait d’un élément | O(1) |

## :material-progress-star: Avantages
- Accès et insertion ultra rapides (en moyenne O(1)).
- Pas besoin de parcours pour retrouver une valeur via la clé.
- Idéal pour compter des occurrences, stocker des relations clé/valeur, ou faire du caching.

## :material-progress-close: Inconvénients
- Pas d’ordre garanti sur les clés.
- Peut provoquer des collisions (rare mais possible).

## :octicons-file-code-16: Exemple C++

```cpp title="hashmap.cpp"
#include <iostream>
#include <unordered_map>
using namespace std;

int main() {
    unordered_map<string, int> score;

    score["Alice"] = 90;
    score["Bob"] = 85;

    cout << "Score de Alice: " << score["Alice"] << endl;

    for (auto &p : score)
        cout << p.first << " : " << p.second << endl;
}
```

!!! tip "Utlise `map` au lieu de `unordered_map` pour avoir des clé triées par valeur -> nombre / alpha_num"

## :fontawesome-solid-brain: LeetCode Challenges

| Difficulté | Titre | Lien |
|-------------|--------|------|
| :green_square: Easy | Two Sum | [**Link**](https://leetcode.com/problems/two-sum/) |
| :green_square: Easy | Valid Anagram | [**Link**](https://leetcode.com/problems/valid-anagram/) |
| :green_square: Easy | Intersection of Two Arrays | [**Link**](https://leetcode.com/problems/intersection-of-two-arrays/) |
| :yellow_square: Medium | Subarray Sum Equals K | [**Link**](https://leetcode.com/problems/subarray-sum-equals-k/) |
| :yellow_square: Medium | Top K Frequent Elements | [**Link**](https://leetcode.com/problems/top-k-frequent-elements/) |
| :yellow_square: Medium | Longest Substring Without Repeating Characters | [**Link**](https://leetcode.com/problems/longest-substring-without-repeating-characters/) |
| :yellow_square: Medium | Group Anagrams | [**Link**](https://leetcode.com/problems/group-anagrams/) |
| :yellow_square: Medium | 4Sum II | [**Link**](https://leetcode.com/problems/4sum-ii/) |
| :red_square: Hard | LFU Cache | [**Link**](https://leetcode.com/problems/lfu-cache/) |
| :red_square: Hard | Minimum Window Substring | [**Link**](https://leetcode.com/problems/minimum-window-substring/) |
