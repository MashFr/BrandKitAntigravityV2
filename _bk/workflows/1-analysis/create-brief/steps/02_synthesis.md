---
description: Génération du Brand Brief
---

<step id="02_synthesis">
  <action>
    Remercie l'utilisateur pour ces éléments structurants.
    
    Compile les informations collectées pour remplir le template `@brand-bried-template.md`.
    
    Remplace les placeholders suivants par les réponses de l'utilisateur :
    - {{PROJECT_NAME}} -> Nom du projet (demandé ou déduit)
    - {{VISION}}
    - {{MISSION}}
    - {{TARGET_AUDIENCE}}
    - {{PAIN_POINT}}
    - {{VALUE_1}}, {{VALUE_2}}, {{VALUE_3}}
    - {{BRAND_PERSONALITY}}
    - {{TONE_OF_VOICE}} -> Déduit de la personnalité
    - {{AESTHETIC_KEYWORDS}} -> Déduit de l'ensemble
    
    Génère le fichier final : `brandkit_output/00_brand_brief.md`.
    Affiche le contenu du fichier généré à l'utilisateur pour validation.
  </action>
</step>
