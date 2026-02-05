---
description: Workflow de création de Scénographies & Mockups (Aura Visuals)
---

# Workflow : Scénographies & Mockups

Ce workflow définit l'environnement de présentation de la marque et génère des bases de mockups propriétaires.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Mise en scène de l'identité. Création de vos environnements de présentation."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/03_colors.md`
      - `brandkit_output/05_graphic_universe.md`
      - `brandkit_output/06_moodboard_prompts.md` (Crucial pour la cohérence lumineuse)

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Cohérence impossible. Veuillez définir le Moodboard avant de générer des mockups."
      }
      SINON {
          Charge les fichiers avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Set Design" file="@_bk/workflows/7-visuals/create-mockups/steps/01_scenography.md" />
  
  <step name="Sélection Objets" file="@_bk/workflows/7-visuals/create-mockups/steps/02_objects.md" />
  
  <step name="Prompting Mockup" file="@_bk/workflows/7-visuals/create-mockups/steps/03_prompting.md" />
  
  <step name="Finalisation" file="@_bk/workflows/7-visuals/create-mockups/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme la création de `brandkit_output/10_mockups_scenography.md`.
    </action>
  </step>
</workflow_steps>
