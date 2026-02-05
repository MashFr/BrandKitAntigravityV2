---
description: Workflow de création de Data-Viz Esthétique (Aura Visuals)
---

# Workflow : Data-Viz Esthétique

Ce workflow définit une manière propriétaire de visualiser l'information et génère des prompts de "Data-Art".

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Transformer les données en poésie visuelle. Création de votre système de Data-Viz."
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
          Informe l'utilisateur : "⚠️ Contexte insuffisant. Veuillez définir l'Univers Graphique et les Couleurs avant de créer de la Data-Viz."
      }
      SINON {
          Charge les fichiers avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Esthétique des Données" file="@_bk/workflows/7-visuals/create-dataviz/steps/01_style.md" />
  
  <step name="Métaphores de Données" file="@_bk/workflows/7-visuals/create-dataviz/steps/02_charts.md" />
  
  <step name="Prompting Data-Art" file="@_bk/workflows/7-visuals/create-dataviz/steps/03_prompting.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-dataviz/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme la création de `brandkit_output/11_aesthetic_dataviz.md`.
    </action>
  </step>
</workflow_steps>
