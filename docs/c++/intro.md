# :material-language-cpp: Introduction

Le but de ces formations et de vous familiariser avec la syntaxe et le raisonnement C++.
C++ est un langage de programmation **compilé**, **orienté objet** et **générique**.
C'est également un superset de **C**, ce qui signifie que tout code C est aussi du code C++ valide.
Il est très utilisé en **Competitive Programming** et dans les **Tech Interviews**.

Cette formation ^^n'est pas un cours d'Orienté Objet^^. Le but est de vous apprendre à coder rapidement et efficacement en C++ et savoir utiliser la **STL**.

!!! tip "Cheat Sheet C++ sur [**QuickRed.me**](https://quickref.me/cpp.html)"

## :material-hand-wave: Hello World

Premier programme en C++ -> le classico Hello World !


```cpp title="main.cpp"
#include <iostream>

int main(int ac, char **av) {
    std::cout << "Hello World !" << std::endl;
    return EXIT_SUCCESS;
}
```

- `.cpp` l'extension des programmes C++.
    - Le premier à me faire un `main.c++` c'est ban list.
- `iostream` la lib à inclure pour pouvoir **écrire** / **lire** sur les **sorties** / **entrées** standards
- `std` des keyword pour spécifier qu'on utilise des éléments de la **Standard Library**
    - on va faire évoluer le programme pour ne pas avoir à les écrire à chaque fois
- `EXIT_SUCCESS` une simple macro héritée du C -> `#define EXIT_SUCCESS 0`
    - `EXIT_FAILURE` équivalent `#define EXIT_FAILURE 1`

## :simple-compilerexplorer: Compilation & Exécution

Pour compiler un programme C++ on utilise **`g++`** (cf. `man g++`). Fonctionne comme `gcc` et prend les mêmes arguments.

- Donc pour compiler notre programme on peut run :

```sh title="Terminal"
g++ main.cpp
```

Vérifier bien que vous êtes dans le même directory que votre programme :material-folder-outline:

On oublie les `-Wall -Wextra ...` on a pas le temps en challenge - ce n'est pas vous qui allez compiler votre code sur les plateformes, vous vous chargez uniquement du code. Surtout si c'est pour me dire `unsused ac / av parameter` :material-sleep:

Vous pouvez spécifier le nom du binaire généré avec `g++ main.cpp -o main`, mais par défault le `a.out` c'est très bien.

- On execute directement le binaire :

```sh title="Terminal"
./a.out
```

!!! tip "Vous pouvez également run votre code directement grace à l'extenssion C/C++ (en haut à droite)"

- Normalement le programme affiche sur la sortie standard :

``` title="Output"
Hello World !
```

## :material-book-cog: Namespace & STL

Pour éviter d'avoir à écrire `std::` à chaque fois qu'on utilise un élément de la **Standard Library**, on peut utiliser le mot clé `using namespace std;` au début du programme.

```cpp title="main.cpp"
#include <iostream>

using namespace std;

int main(int ac, char **av) {
    cout << "Hello World !" << endl;
    return EXIT_SUCCESS;
}
```

Vous pouvez également définir vos propres namespace

```cpp title="namespace.cpp"
#include <iostream>

namespace test {
    int val() {
        return 5;
    }
}

int main() {
    std::cout << test::val() << std::endl;
}

```
