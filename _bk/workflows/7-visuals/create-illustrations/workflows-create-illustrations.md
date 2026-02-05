---
description: Workflow de création du Système d'Illustration (Aura Visuals)
---

# Workflow : Système d'Illustration

Ce workflow définit le style illustratif de la marque et génère les prompts pour créer les visuels clés.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Donner corps à l'imaginaire. Création de votre système d'illustration."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md`
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/03_colors.md`
      - `brandkit_output/05_graphic_universe.md`

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Contexte insuffisant. Veuillez définir l'Univers Graphique et les Couleurs avant de créer des illustrations."
      }
      SINON {
          Charge les fichiers avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Style d'Illustration" file="@_bk/workflows/7-visuals/create-illustrations/steps/01_art_direction.md" />
  
  <step name="Métaphores Visuelles" file="@_bk/workflows/7-visuals/create-illustrations/steps/02_concepts.md" />
  
  <step name="Prompting" file="@_bk/workflows/7-visuals/create-illustrations/steps/03_prompting.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-illustrations/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme la création de `brandkit_output/09_illustrations.md`.
      Suggère de tester les visuels dans Nanobanana.
    </action>
  </step>
</workflow_steps>
