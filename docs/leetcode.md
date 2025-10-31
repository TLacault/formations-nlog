# :material-lightbulb-on: Challenges & Leaderboard

!!! success "NLOG'EIRB vous propose des entraînement sur la plateforme [**Leetcode**](https://leetcode.com/problemset/)"

Leetcode est considérée comme **le standard** dans l'industrie pour se préparer aux **Tech Interviews**.
On vous propose chaque semaine une **liste de challenges à résoudre en C++** (ou autre langage si vous préférez) avec un **Leaderboard** pour suivre vos progrès et ceux de vos camarades.

## Pourquoi Leetcode :material-help-circle-outline:

- Très grande variété de **challenges pertinents** -> presque 3000
- Problèmes **classés par difficulté** (Easy, Medium, Hard) et **Topic** (Array, Tree, ...)
- Système de **test intégré** pour valider vos solutions
- Discussions et **solutions** proposées par la communauté
- **Interface utilisateur** conviviale et facile à utiliser

## Format des séances :material-timer-outline:

| Topic                                                         | Time      |
|---------------------------------------------------------------|-----------|
| Rappel & Explication des solutions de la semaine précédente   | 10 min    |
| Introduction nouveaux DSA -> théorie et schéma sur tableau    | 20 min    |
| Utilisation de la lib en C++ -> méthodes des classes etc...   | 10 min    |
| Liste de challenges à résoudre                                | 80 min    |

## Objectif :octicons-goal-16:

!!! danger "Votre mission, si toutefois vous l'acceptez, sera de résoudre 300 challenges"

Ce nombre n'est pas pris au hasard, c'est ce que la **grande majorité des pro** recommandent.
300 challenges c'est le temps que ça prend pour obtenir de bonnes connaissances générales et couvrir **l'ensemble des DSA** les plus communs.

On peut les répartir comme ceci :

| Répartition       | Objectif                                                                              |
|-------------------|---------------------------------------------------------------------------------------|
| **50 Easy**       | 3 à 5 challenges pour **introduire un nouveau DSA**                                   |
| **200 Medium**    | 15 à 20 chall pour couvrir les **différents cas d'utilisations** d'un DSA spécific    |
| **50 Hard**       | 3 à 5 challenges pour aller plus loin et **pousser votre raisonement**                |


## Travail Personel :material-code-block-tags:

!!! warning "Suivre les formations NLOG'EIRB vous procurera de bonnes bases. Mais pour devenir expert, acquerir des automatismes et reconnaitre les patternes il va falloir travailler en dehors des séances et réviser."

Chaque semaine on vous propose une **liste de challenges** à terminer pour la semaine d'après.
Vous **n'aurez pas le temps** de les finir pendant la séance et c'est normale.
Il faudra donc travailler chez vous pour en venir à bout.
On ne vous demande pas forcément de tous les terminer mais au moins de les essayer, de ^^**chercher une solution**^^ et de ^^**comprendre la correction**^^.
Je détaille la **stratégie d'apprentissage** juste après.

## Stratégie :material-strategy:

Même si l'objectif final est de savoir résoudre les **challenges Medium en 20 min**, certains vous prendront bien plus de temps au début.

!!! info "Prenez des notes - papier ou ordi - pendant tout le process, c'est important. Ca vous permetra de mieux comprendre, de réviser rapidement sans avoir à recoder et de reconnaitre certains patternes."

### 1. Phase de réflexion

Sortez votre meilleur crayon et un bloc note, c'est le moment de dessiner et chercher une solution.
Le but c'est de réfléchir à quel **Data Structure** et/ou **Algorithme** permettrait de résoudre ce problème efficacement.

!!! tip "En générale le type de Data Struct à utiliser vous est donné par la catégorie du challenge, ça donne déjà une piste !"

### 2. Programmation

Une fois que vous pensez avoir une solution -> vous pouvez coder !

N'espérez pas trouver la solution du premier coup, les batteries de tests leetcode vont tester absoluments tout les **Edge Cases**.
Améliorer votre implémentation pour que votre algo soit assez générale pour couvrir tout les cas.

### 3. Optimisation

Votre solution passe la majorité des cas mais Leetcode vous sort une **error timeout** ou vous n'etes juste pas satisfait de votre utilisation mémoire ?
Bienvenue dans l'enfer de la complexité algorithmique :material-party-popper:

??? question "Posez vous bien ces questions :"
    - Est-ce que ma data structure / mon algorithme est vraiment adaptée ?
        - **Ex Time** : je dois trier ma data struct mais j'ai une complexité `n²` -> trouve un algorithme adapté en `n log n`.
        - **Ex Space** : mon array n'est remplie qu'à 50% pendant l'execution -> utilise un vector (array de taille dynamique)
    - Est-ce que je peux réduire le nombre d'itérations / appels de fonctions ?
        - **Ex** : j'ai une boucle imbriquée -> essaye de réduire en utilisant une map pour stocker des valeurs intermédiaires
    - Est-ce que je peux utiliser une approche différente ?
        - **Ex** : essaye de déterminer si une approche **récursive** et plus adaptée qu'une approche **itérative**.

### 4. Analyse

!!! warning "Il **ne faut pas** vous forcer à bucher sur un challenge pendant 50 min -> perte de temps."

Le but c'est d'avoir compris l'enjeu du problème, ce qu'on cherche à résoudre et comment.
En plus des solutions qu'on vous fournis et des vidéo explicatives, la communautée leetcode publie des solutions pour chaque challenges.

On recommande de passez **30 min grand maximum** à résoudre un problème et **5-10 min** pour analyser une solution - bonus vous pouvez la réimplémenter vous même.
La prochaine fois que vous rencontrerez ce genre de problème vous serez capable de reconnaitre le patterne et trouver une solution adaptée.

!!! example "Attention quand vous cherhez un solution sur Leetcode"
    Il y a des flexeur sur Leetcode qui proposent des solutions super optimisées avec des algorithmes obscures qui vous placent dans le "top 1% time/space complexity" -> C'est pas ce qu'on veut.

    Cherchez une solution adaptée, compréhensible, qui fonctionne et surtout reproductible et applicable à d'autre challenges.
