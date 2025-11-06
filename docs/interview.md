# :fontawesome-solid-handshake: Tech Interviews

L'un des buts principaux de ces formations est de vous préparer aux entretients techniques.

!!! warning "Savoir résoudre les challenges n'est qu'un partie de l'interview !"

Résoudre un challenge medium en 20 minutes ne suffit pas -> les interviews suivent un schéma bien précis.

### 0. Ennoncé du problème

!!! question "Quel est le problème ?"

L'interviewer vous présente le problème à résoudre.

!!! info "Prenez des notes pendant cette phase, ça vous aidera à structurer votre pensée."

- N'hésitez pas à **poser des questions** pour clarifier l'énoncé
- Reformulez le problème avec vos propres mots pour être sûr d'avoir bien compris
- Pensez à **vérifier les contraintes** (taille des inputs, types de données, ...)
- Discutez des **cas limites** et des **exemples** pour bien cerner le problème

### 1. Approche Simple - Brute Force :material-draw:

!!! question "Comment résoudre le problème ^^simplement^^"

- Dans un premier temps on veut trouver une solution **rapidement et simple d'implémentation**.
Ici le but c'est de partager avec le recruteur son raisonnement.
- Pensez à **expliquer chaque étape** de votre réflexion et **justifier vos choix** de Data Structure et d'Algorithme.
- Une fois l'approche simple trouvée, discutez de sa **complexité temporelle et spatiale**.
- Demandez **confirmation** au recruteur.

Maintenant que vous avez bien cerné le problème, vous devriez avoir pensé à une **solution plus optimale qui utilise un DSA plus adapté**.

Si c'est le cas, vous pouvez le préciser au recruteur.

^^2 cas de figure^^ :

- le recruteur dit : tu peux déjà commencer par coder la première solution -> Step 2
- le recruteur dit : explique comment tu résoudrait ce problème d'une manière plus efficace -> directement Step 3

### 2. Programation

!!! question "Résolution du problème"

Après avoir validé l'approche, vous pouvez commencer à coder.

- N'hésitez pas à **penser à voix haute** pour partager votre raisonnement avec le recruteur.
Ca montre que vous maitrisez le sujet et ça aide à comprendre votre logique.
- Commencez par **définir la structure générale** de votre code (fonctions, classes, etc.).
- Implémentez votre solution étape par étape.
- Une fois le code terminé, **relisez-le** pour vérifier qu'il n'y a pas d'erreurs évidentes.

!!! danger "Quelques trucs à éviter"
    - Evite de paraphraser ton code -> `cout << nums[i] << endl;` ici on affiche la case n°i de l'array nums
    - Le recruteur veux savoir comment tu réfléchis, ne reste pas silencieux

### 3. Amélioration & Optimisation

!!! question "Comment résoudre le problème ^^efficacement^^ ?"

- Le recruteur valide votre implémentation et vos explication.
- Il y a de grandes chances pour qu'il vous demande d'améliorer votre solution et de trouver une manière de réduire la complexité temps / espace.
- On applique de raisonement du `Step 1` : explique à vois haute, tu peux même dessiner. Démontre comment une nouvelle Data Structure ou un autre algorithme serait plus adapté.

    !!! success "Tu as le droit de ne pas avoir de meilleur solution, ils sont habitués ça peut être la pression. Ils te donneront un indice pour te mettre sur la voie."

- Le recruteur ne va pas systématiquement te demander de programmer cette solution. Son but c'est d'évaluer ta capacité de réflexion.
- S'il te demande quand même de l'implémenter, force à toi -> back to `Step 2`.

### 4. Modification du Problème / Autre Approche

!!! question "Un nouveau problème ???"

- Tout les recruteurs ne le font pas forcément, mais certains te demanderons comment tu aurais résolu le problème après l'avoir reformulé.
- D'autre peuvent également te demander d'imaginer une autre approche pour le même problème
    - si ton implémentation est rapide mais consomme beaucoup de mémoire (backtracking etc...) propose une approche plus lente mais plus optimale en terme d'espace.
    - si ton approche est itérative refléchis à une solution récursive
    - trouve une autre DSA qui permettrai de résoudre le problème avec la même Time/Space Complexity.

### 5. Conclusion & FeedBack

!!! question "Les futures problèmes ?"

- A la fin de l'exercice, n'hésitez pas à demander des retours sur votre performance. Le recruteur le fera surement de lui même.
- Prenez note des questions posées par le recruteur et des solutions proposées, cela pourra vous aider lors de prochains entretiens.

## Recap
