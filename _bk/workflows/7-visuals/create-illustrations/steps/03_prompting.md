---
description: Step 3 - Prompting Illustratif (Nanobanana)
---

<step id="03_prompting">
    <action>
        Génère les prompts pour Nanobanana en respectant STRICTEMENT les contraintes suivantes :

        **CONTRAINTES CRITIQUES (SÉCURITÉ)** :
        - **INTERDIT** : Icônes, Logotypes, Mascottes, Personnages 3D mignons, Mockups d'interface.
        - **OBLIGATOIRE** : Illustrations purement artistiques, scènes complètes, composition narrative.
        - Le style doit être cohérent avec la direction artistique définie à l'étape 01.

        **SORTIE ATTENDUE** :
        Tu dois générer le contenu pour remplir le template `brandkit_output/visuals/10_illustrations.md`.

        1.  **TEMPLATE MAÎTRE** :
            - Un prompt générique avec un placeholder `[DESCRIPTION DE LA SCÈNE]` que l'utilisateur pourra remplacer.
            - Doit inclure tous les tokens de style, medium, éclairage et composition.

        2.  **CATALOGUE (9 ILLUSTRATIONS)** :
            - Génère 9 prompts COMPLETS et VARIÉS pour couvrir les besoins du site web et des présentations.
            - Exemples de sujets (à adapter au projet) :
                - Hero Section (Accueil) - Scène large et impactante.
                - Feature Spotlight - Focus sur un concept clé du produit.
                - About Us / Vision - Représentation abstraite des valeurs.
                - Blog Post Header - Sujet éducatif ou informatif.
                - 404 Error Page - Concept ludique ou métaphorique (mais pas de mascotte !).
                - Success State - Célébration subtile.
                - Background Texture - Élément décoratif subtil.
                - Data Visualization - Représentation artistique de données.
                - Community / Social - Interaction humaine stylisée.

        **Structure des Prompts (Nano Banana BANANA + Pseudo-Code)** :
        Respecte la structure suivante pour le Master Template et les déclinaisons :
        ```text
        [VARIABLES]
        SCENE = "[DESCRIPTION DE LA SCÈNE]"
        ART_STYLE = "[Style détaillé de l'étape 01]"
        PALETTE = "[Couleurs de l'étape 01]"
        LUMIERE_COMPO = "[Eclairage, texture et composition]"

        [EXECUTION]
        Génère une illustration représentant SCENE. Applique le ART_STYLE avec PALETTE.
        Assure-toi d'utiliser LUMIERE_COMPO.
        Contraintes : artistic illustration, cohesive narrative --no icons, logos, mascots, 3d characters, ui mockups, photorealistic --ar 16:9 --style raw
        ```
    </action>
</step>
