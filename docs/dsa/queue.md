# :material-format-list-bulleted: Queue

## :material-magnify: Description
Une **Queue** est une structure FIFO (First-In, First-Out).
Les éléments sont traités dans l'ordre d'arrivée. Utilisée pour les BFS, la gestion de tâches, et les buffers.

## :fontawesome-solid-list-check: Opérations principales et complexités

| Opération | Description | Complexité |
|-----------|-------------|------------|
| push/enqueue | Ajouter un élément à la fin | O(1) |
| pop/dequeue  | Retirer l'élément en tête | O(1) |
| front        | Accéder à l'élément en tête | O(1) |
| recherche    | Trouver une valeur (scan) | O(n) |

## :material-progress-star: Avantages vs autres structures
- Ordre naturel pour le traitement séquentiel (jobs, BFS).
- Moins d'overhead pour insertion/suppression en tête que vector (si on utilise std::deque ou std::queue).

## :material-progress-close: Inconvénients
- Accès limité aux éléments internes (nécessite copie/popping pour itérer).
- Pas adapté pour accès aléatoire.

## :octicons-file-code-16: Exemples C++

### Instanciation & opérations basiques
```cpp title="queue_basics.cpp"
// using <queue>
queue<int> q;
q.push(1);
q.push(2);
int first = q.front(); // 1
q.pop(); // retire 1
bool empty = q.empty();
```

### Utilisation avec deque pour accès bidirectionnel
```cpp title="deque_example.cpp"
#include <deque>

deque<int> dq;
dq.push_back(1);
dq.push_front(0);
dq.pop_front();
dq.pop_back();
```

### BFS (parcours largeur)
```cpp title="bfs.cpp"
queue<Node*> q;
q.push(root);
while (!q.empty()) {
    Node* cur = q.front(); q.pop();
    // process cur
    if (cur->left) q.push(cur->left);
    if (cur->right) q.push(cur->right);
}
```

### Sliding window (utilisation d'une deque pour optimiser)
```cpp title="sliding_window.cpp"
deque<int> dq; // stocke indices
for (int i = 0; i < n; ++i) {
    // remove out of window
    while (!dq.empty() && dq.front() <= i - k) dq.pop_front();
    // maintain decreasing order
    while (!dq.empty() && nums[dq.back()] < nums[i]) dq.pop_back();
    dq.push_back(i);
    if (i >= k - 1) ans.push_back(nums[dq.front()]);
}
```

## :fontawesome-solid-brain: LeetCode Challenges

|Difficulté|Titre|Lien|
|-|-|-|
| :green_square: Easy | Implement Queue using Stacks | [**Link**](https://leetcode.com/problems/implement-queue-using-stacks/) |
| :green_square: Easy | Number of Recent Calls | [**Link**](https://leetcode.com/problems/number-of-recent-calls/) |
| :green_square: Easy | Moving Average from Data Stream | [**Link**](https://leetcode.com/problems/moving-average-from-data-stream/) |
| :yellow_square: Medium | Sliding Window Maximum | [**Link**](https://leetcode.com/problems/sliding-window-maximum/) |
| :yellow_square: Medium | Design Circular Queue | [**Link**](https://leetcode.com/problems/design-circular-queue/) |
| :yellow_square: Medium | Rotting Oranges | [**Link**](https://leetcode.com/problems/rotting-oranges/) |
| :red_square: Hard | Shortest Path in a Grid with Obstacles Elimination | [**Link**](https://leetcode.com/problems/shortest-path-in-a-grid-with-obstacles-elimination/) |
| :red_square: Hard | LFU Cache | [**Link**](https://leetcode.com/problems/lfu-cache/) |
