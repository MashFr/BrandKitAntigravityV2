---
description: Step 2 - Compilation, Filtrage & Placeholders
---

<step id="02_compilation">
    <action>
        Assemble et purifie les documents du BrandKit pour former la Charte Graphique finale.
        
        1. **Lecture des sources** :
           - Lis tous les fichiers `.md` produits dans le dossier `brandkit_output` (ex : `00_brand_brief.md`, `01_foundation_strategy.md`, `03_colors.md`, `05_graphic_universe.md`, etc.).

        2. **Filtrage et Nettoyage (RÈGLE STRICTE)** :
           - Synthétise le contenu de manière fluide (Stratégie -> Identité Verbale -> Couleurs -> Typographie -> Univers Visuel).
           - **EXCLUSION OBLIGATOIRE : Retire tous les "Prompts IA" (Midjourney, ChatGPT, etc.) ainsi que les blocs d'instructions techniques qui étaient destinés à la génération.** La charte finale ne doit contenir que le fond et la forme de la marque.

        3. **Ajout des Placeholders** :
           - À l'endroit où des images pertinentes illustrent le propos (ex: logo, couleurs, éléments graphiques), ajoute des espaces réservés (placeholders) en syntaxe Markdown pointant vers l'arborescence d'assets créée à l'étape 1.
           - *Exemple* : `![Logo Principal Placeholder](./assets/logo/logo-principal.png)` ou `![Illustration Ambiance](./assets/illustrations/ambiance-1.png)` ou `![Icône Valeur](./assets/icones/icone-valeur.svg)`.

        4. **Sauvegarde** :
           - Écris ce contenu final dans le fichier `charte-graphique/charte-graphique.md`.
    </action>
</step>
