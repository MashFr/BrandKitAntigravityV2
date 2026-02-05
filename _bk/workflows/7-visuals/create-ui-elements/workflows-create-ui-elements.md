---
description: Workflow de création d'Éléments d'Interface (Aura Visuals)
---

# Workflow : Éléments d'Interface (UI)

Ce workflow définit l'esthétique de l'interface utilisateur et génère des concepts de composants UI cohérents.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Structurer l'expérience. Création de votre système d'éléments UI."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md`
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/03_colors.md`
      - `brandkit_output/04_typography.md`
      - `brandkit_output/05_graphic_universe.md`

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Contexte insuffisant. Veuillez définir la Typographie et l'Univers Graphique avant de créer des éléments UI."
      }
      SINON {
          Charge les fichiers avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Style UI" file="@_bk/workflows/7-visuals/create-ui-elements/steps/01_ui_style.md" />
  
  <step name="Composants Critiques" file="@_bk/workflows/7-visuals/create-ui-elements/steps/02_components.md" />
  
  <step name="Prompting UI" file="@_bk/workflows/7-visuals/create-ui-elements/steps/03_prompting.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-ui-elements/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme la création de `brandkit_output/12_ui_elements.md`.
    </action>
  </step>
</workflow_steps>
