---
description: Workflow de création du Traitement Image & Vidéo (Aura Universe)
---

# Workflow : Traitement Image & Vidéo

Ce workflow définit la signature visuelle "post-production" de la marque pour garantir une cohérence entre tous les contenus fixes et animés.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Universe** défini dans `../agent-universe.md`.
      Annonce : "Définissons le filtre à travers lequel votre monde sera perçu. Création de votre signature image et vidéo."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/03_colors.md`
      - `brandkit_output/05_graphic_universe.md`
      - `brandkit_output/06_moodboard_prompts.md`

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Base visuelle manquante. Veuillez définir le Moodboard et l'Univers Graphique avant de régler le traitement d'image."
      }
      SINON {
          Charge les fichiers avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Signature Photographique" file="@_bk/workflows/6-universe/create-image-treatment/steps/01_photography.md" />
  
  <step name="Signature Motion" file="@_bk/workflows/6-universe/create-image-treatment/steps/02_motion.md" />
  
  <step name="Tokens & Technique" file="@_bk/workflows/6-universe/create-image-treatment/steps/03_tokens.md" />
  
  <step name="Finalisation" file="@_bk/workflows/6-universe/create-image-treatment/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme la création de `brandkit_output/13_image_video_treatment.md`.
    </action>
  </step>
</workflow_steps>
