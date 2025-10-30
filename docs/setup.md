!!! success "L'ensemble des outils recommendés sont installés sur les machines de l'ENSEIRB"

## :octicons-file-code-16: Langage de Programmation

!!! tip "NLOG'EIRB recommande d'utiliser **C++**"

- Superset de **C** -> syntax similaire et facile à apprendre
- Pas de **gestion mémoire** manuelle -> gain de temps et moins d'erreurs
- **STL** (Standard Template Library) très puissante pour les structures de données et algorithmes
- Très utilisé en Competitive Programming et dans les Tech Interviews

## :material-microsoft-visual-studio-code: Environnement de Développement (IDE)

!!! tip "NLOG'EIRB recommande d'utiliser **Visual Studio Code (VSCode)**"

- Léger et rapide
- Supporte de nombreuses extensions pour C++
- Intégration facile avec les outils de build et de débogage

### Configuration :material-tools:

1. Installer l'extension **C/C++ Extension Pack** de Microsoft

2. Formater le code avec **clang-format**
    - Télécharger [**ce fichier**](https://github.com/TLacault/formations-nlog/tree/main/resources/.clang-format) **`.clang-format`** et le placer à la racine de ton projet

    !!! info "Si tu as 2 heures à perdre, tu peux aussi [**générer ton propre fichier**](https://clang-format-configurator.site/) adapté à tes préférences."

    ???+ info "De nombreux projets open-source et entreprises partagent leur propre fichier **.clang-format**."
        - Google : [**lien**](https://github.com/TLacault/formations-nlog/tree/main/resources/google)
        - Microsoft : [**lien**](https://github.com/TLacault/formations-nlog/tree/main/resources/microsoft)


3. Save & Format automatique
    - Settings -> **`Files: Auto Save`** -> selectionne **`onFocusChange`**
    - Settings -> **`C_Cpp: Formatting`** -> selectionne **`clangFormat`**
    - Settings -> **`Editor: Format On Save`** -> Coche la case
    !!! tip "Le code sera formaté automatiquement à chaque fois que tu changes de fichier ou sauvegardes le fichier"


### Snippets :material-lightning-bolt:

!!! tip "Utiliser des **snippets** pour insérer rapidement des bouts de code fréquemment utilisés"

1. Ouvre la palette de commandes : `Ctrl + Shift + P`
2. Chercher **`Snippets`** -> **`Snippets: Configure Snippets`** -> **`cpp.json`**
3. Copier-coller le contenu de [**ce fichier**](https://github.com/TLacault/formations-nlog/tree/main/resources/cpp.json)
