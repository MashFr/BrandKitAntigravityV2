---
description: Workflow de création du Moodboard & Prompts (Aura Visuals)
---

# Workflow : Moodboard & Prompts

Ce workflow génère les prompts (Nanobanana) pour créer les assets visuels du moodboard.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Initialisation des protocoles visuels. Traduction de la stratégie en lumière."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md` (Pour le Produit/Service)
      - `brandkit_output/01_foundation_strategy.md` (Pour l'Archétype)
      - `brandkit_output/02_verbal_identity.md` (Pour le Ton)
      - `brandkit_output/03_colors.md` (Pour la palette)
      - `brandkit_output/05_graphic_universe.md` (Pour le style global)

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Données visuelles manquantes. Veuillez définir l'Univers Graphique et les Couleurs avant de générer des images."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Direction Artistique" file="@_bk/workflows/7-visuals/create-moodboard/steps/01_art_direction.md" />
  
  <step name="Ingénierie des Prompts" file="@_bk/workflows/7-visuals/create-moodboard/steps/02_prompt_engineering.md" />
  
  <step name="Shot List (Hero, Portrait, Detail)" file="@_bk/workflows/7-visuals/create-moodboard/steps/03_shot_list.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-moodboard/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme que le guide de prompts est enregistré dans `brandkit_output/06_moodboard_prompts.md`.
      Encourage l'utilisateur à tester les prompts dans Nanobanana.
    </action>
  </step>
</workflow_steps>
