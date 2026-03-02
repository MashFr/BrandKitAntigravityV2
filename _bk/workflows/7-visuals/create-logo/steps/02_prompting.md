---
description: Step 2 - Prompting Vectoriel (Nanobanana)
---

<step id="02_prompting">
    <action>
        Transforme les 3 pistes en prompts Nanobanana en utilisant le framework BANANA et le Pseudo-Code Prompting.
        
        **Framework BANANA pour les Logos** :
        - **B - Boundaries** : `white background`, `1:1 square ratio`
        - **A - Audience/Vibe** : (ex: modern tech startup, luxury brand)
        - **N - Nuances** : `flat vector logo`, `no gradients`
        - **A - Action (Mise en page)** : `centered icon`
        - **N - Négatifs** : `--no realistic, photo, 3d, shading, complex details`
        - **A - Assessment** : `highly legible at small sizes`
        
        **Typographie** : Si le logo contient du texte, mettre le mot exact entre guillemets doubles (ex: "NOM_MARQUE") et décrire la police (ex: bold sans-serif).
        
        **Structure du prompt (Pseudo-Code)** :
        ```text
        [VARIABLES]
        SUJET = "[Description de l'élément central]"
        COULEUR = "[Palette précise, HEX si possible]"
        STYLE = "[Style détaillé (ex: flat vector, minimalist)]"
        TEXTE = "[Texte entre guillemets et description typo (Optionnel)]"

        [EXECUTION]
        Génère SUJET en utilisant COULEUR et applique le STYLE. Ajoute TEXTE en dessous. 
        Contraintes : white background, centered icon, highly legible. --no realistic, photo, 3d, shading --ar 1:1
        ```
    </action>
</step>
