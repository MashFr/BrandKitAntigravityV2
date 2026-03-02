---
description: Step 3 - Prompting de Scénographie (Nanobanana)
---

<step id="03_prompting">
    <action>
        Génère les prompts pour créer ces bases de mockups.
        
        **Technique "Mockup Clean"** :
        - Demande toujours une surface vide ("blank screen", "plain paper") pour faciliter l'incrustation.
        - Utilise des tokens comme `photorealistic`, `studio lighting`, `sharp focus`.
        
        Structure Nano Banana (Pseudo-Code & BANANA) :
        Utilise cette structure pour chaque mockup généré :
        ```text
        [VARIABLES]
        OBJET = "[BLANK OBJECT (ex: blank smartphone screen, plain paper)]"
        SURFACE = "[SURFACE]"
        LUMIERE_AMBIANCE = "[LIGHTING], [ATMOSPHERE]"

        [EXECUTION]
        Génère une photo haute qualité de OBJET posé sur SURFACE. Applique LUMIERE_AMBIANCE.
        Contraintes : photorealistic, studio lighting, sharp focus, blank and plain surfaces for easy replacement --no text on screen, UI elements, complex patterns on the object --ar 16:9
        ```
    </action>
</step>
