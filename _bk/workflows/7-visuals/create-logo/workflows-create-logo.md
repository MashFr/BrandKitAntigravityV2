---
description: Workflow de création de Concepts Logo (Aura Visuals)
---

# Workflow : Concepts Logo

Ce workflow génère des prompts techniques pour créer des concepts de logo vectoriels.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Recherche de la singularité. Génération de concepts vectoriels."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/01_foundation_strategy.md` (Pour l'Archétype)
      - `brandkit_output/02_verbal_identity.md` (Pour le Nom et les Initiales)
      - `brandkit_output/03_colors.md` (Pour la Palette)
      - `brandkit_output/04_typography.md` (Pour le style Typographique)
      - `brandkit_output/05_graphic_universe.md` (Pour les Formes)

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Base graphique manquante. Définissez l'Univers Graphique avant d'attaquer le logo."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Territoires Créatifs" file="@_bk/workflows/7-visuals/create-logo/steps/01_directions.md" />
  
  <step name="Prompting Vectoriel" file="@_bk/workflows/7-visuals/create-logo/steps/02_prompting.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-logo/steps/03_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme que le guide Logo est enregistré dans `brandkit_output/07_logo_prompts.md`.
      Rappelle que l'IA génère des pixels, et qu'une vectorisation manuelle sera nécessaire.
    </action>
  </step>
</workflow_steps>
