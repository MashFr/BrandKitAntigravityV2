---
description: Step 3 - Prompting Iconographique (Nanobanana)
---

<step id="03_prompting">
    <action>
        Définit un UN SEUL prompt "Master Template" (Pseudo-Code) qui servira pour toutes les icônes selon le framework BANANA.

        **Contraste & Lisibilité (Priorité Absolue)** :
        - Les icônes doivent avoir un niveau de contraste élevé (High Contrast) et des silhouettes claires.
        - Bannir les traits trop fins (no thin lines), les couleurs pastel sur fond clair sans contour, et les détails minuscules (no intricate micro-details).
        
        **Liberté de Style** :
        - Le style photographique, vectoriel, 3D, Isométrique, Glassmorphism, etc. doit être choisi pour coller **exactement** à la marque.
        
        **Règle d'Or (BANANA + Pseudo-Code)** :
        Structure attendue pour le Master Prompt :
        ```text
        [VARIABLES]
        SUJET = "[INSERER_SUJET_ICI]"
        COULEUR_LUMIERE = "[Décrire couleurs et éclairage exacts]"
        STYLE_MATIERE = "[Décrire le style: 3D isometric clay, thick line art, glassmorphism, etc.]"

        [EXECUTION]
        Génère une icône représentant SUJET. Applique le STYLE_MATIERE avec COULEUR_LUMIERE.
        Contraintes : highly legible, strong contrast, clear recognizable silhouette, pure white background, centered icon --no messy micro-details, low contrast, faint colors, thin lines --ar 1:1
        ```

        - Ajuste les variables `COULEUR_LUMIERE` et `STYLE_MATIERE` avec les descriptions exactes du style de la marque.
        - Laisse le placeholder `[INSERER_SUJET_ICI]` tel quel dans le modèle.
    </action>
</step>
