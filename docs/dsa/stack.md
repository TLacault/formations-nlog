# :material-format-list-bulleted: Stack

## :material-magnify: Description
Un **Stack** est une structure LIFO (Last-In, First-Out).
On y empile des éléments et on les dépile dans l'ordre inverse d'insertion. Utilisé pour les appels récursifs, l'évaluation d'expressions, et les backtracks.

## :fontawesome-solid-list-check: Opérations principales et complexités

| Opération | Description | Complexité |
|-----------|-------------|------------|
| push      | Ajouter un élément au sommet | O(1) |
| pop       | Retirer l'élément au sommet | O(1) |
| top/peek  | Consulter l'élément au sommet sans le retirer | O(1) |
| recherche | Trouver une valeur (scan) | O(n) |

## :material-progress-star: Avantages vs autres structures
- Simplicité et performances constantes pour push/pop par rapport à une file ou un vector quand on n'a besoin que du sommet.
- Idéal pour gérer la récursion manuelle, undo/redo, et parsing d'expressions.

## :material-progress-close: Inconvénients
- Accès limité (seul le sommet est directement accessible).
- Pas adapté si on a besoin d'accès aléatoire ou d'insertion au milieu.

## :octicons-file-code-16: Exemples C++

### Instanciation & opérations basiques
```cpp title="stack_basics.cpp"
#include <stack>

stack<int> st;
st.push(10);
st.push(20);
scan(st);

int top = st.top(); // 20
cout << "\ntop of the stack -> " << top << endl;

st.pop(); // retire 20
st.pop(); // retire 10

// check si la stack est vite
if (st.empty())
    cout << "stack is empty" << endl;
```

### Itération (décomposition dans un conteneur temporaire)
```cpp title="stack_iterate.cpp"
// Stack temporaire -> parcourir sans perdre les éléments
stack<int> tmp;
while (!st.empty()) {
    int x = st.top();
    cout << x << endl;
    tmp.push(x);
    st.pop();
}

// restore
while (!tmp.empty()) {
    st.push(tmp.top());
    tmp.pop();
}
```

### Utilisation pour évaluation d'expression postfix (RPN)
```cpp title="rpn_eval.cpp"
stack<int> st;
for (char c : tokens) {
    if (isdigit(c)) st.push(c - '0');
    else {
        int b = st.top(); st.pop();
        int a = st.top(); st.pop();
        if (c == '+') st.push(a + b);
        if (c == '-') st.push(a - b);
        if (c == '*') st.push(a * b);
        if (c == '/') st.push(a / b);
    }
}
int result = st.top();
```

### Backtracking (exemple conceptuel)
```cpp title="backtrack.cpp"
// push state before exploring, pop to restore
st.push(state);
explore();
st.pop(); // rollback
```

## :fontawesome-solid-brain: LeetCode Challenges

|Difficulté|Titre|Lien|
|-|-|-|
| :green_square: Easy | Valid Parentheses | [**Link**](https://leetcode.com/problems/valid-parentheses/) |
| :green_square: Easy | Min Stack | [**Link**](https://leetcode.com/problems/min-stack/) |
| :green_square: Easy | Implement Queue using Stacks | [**Link**](https://leetcode.com/problems/implement-queue-using-stacks/) |
| :yellow_square: Medium | Evaluate Reverse Polish Notation | [**Link**](https://leetcode.com/problems/evaluate-reverse-polish-notation/) |
| :yellow_square: Medium | Next Greater Element II | [**Link**](https://leetcode.com/problems/next-greater-element-ii/) |
| :yellow_square: Medium | Largest Rectangle in Histogram | [**Link**](https://leetcode.com/problems/largest-rectangle-in-histogram/) |
| :red_square: Hard | Trapping Rain Water | [**Link**](https://leetcode.com/problems/trapping-rain-water/) |
| :red_square: Hard | Sliding Window Maximum | [**Link**](https://leetcode.com/problems/sliding-window-maximum/) |
