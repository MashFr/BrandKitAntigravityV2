---
description: Workflow de création de la Signature Iconographique (Aura Visuals)
---

# Workflow : Signature Iconographique

Ce workflow définit le style des icônes de la marque et génère les prompts pour les créer.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Définissons la grammaire de vos signes. Création de votre set d'icônes propriétaire."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md`
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/04_typography.md` (Pour l'harmonie des traits)
      - `brandkit_output/05_graphic_universe.md` (Pour les formes)

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Contexte insuffisant. Veuillez définir la Typographie et l'Univers Graphique avant de créer les icônes."
      }
      SINON {
          Charge les fichiers avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Grammaire Iconographique" file="@_bk/workflows/7-visuals/create-icons/steps/01_style.md" />
  
  <step name="Sélection du Set" file="@_bk/workflows/7-visuals/create-icons/steps/02_set.md" />
  
  <step name="Prompting" file="@_bk/workflows/7-visuals/create-icons/steps/03_prompting.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-icons/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme la création de `brandkit_output/08_iconography.md`.
      Suggère de tester les icônes dans Nanobanana.
    </action>
  </step>
</workflow_steps>
