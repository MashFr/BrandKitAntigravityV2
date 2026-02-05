---
description: Workflow de création de la Palette de Couleurs (Psychologie, Harmonie 60-30-10, Accessibilité)
---

# Workflow : Palette de Couleurs

Ce workflow définit l'univers chromatique de la marque, en alliant psychologie et contraintes techniques.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Colors** défini dans `../agent-colors.md`.
      Annonce : "Entrons dans le spectre visible. Nous allons traduire votre stratégie en lumière et en couleur."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md`
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/02_verbal_identity.md`

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Fichiers manquants. Veuillez exécuter les workflows précédents (Brief, Foundation, Verbal) pour assurer la cohérence stratégique."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Stratégie Psychologique" file="@_bk/workflows/4-colors/create-palette/steps/01_psychology.md" />
  
  <step name="Génération Palettes" file="@_bk/workflows/4-colors/create-palette/steps/02_generation.md" />
  
  <step name="Check Accessibilité" file="@_bk/workflows/4-colors/create-palette/steps/03_accessibility.md" />
  
  <step name="Finalisation & Guide" file="@_bk/workflows/4-colors/create-palette/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme que la palette est enregistrée dans `brandkit_output/03_colors.md`.
    </action>
  </step>
</workflow_steps>
