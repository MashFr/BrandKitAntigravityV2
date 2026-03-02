---
description: Workflow de création de Mascotte de Marque (Aura Visuals)
---

# Workflow : Mascotte de Marque

Ce workflow génère la méthodologie et les prompts techniques pour créer une mascotte de marque en utilisant l'IA Nano Banana Pro, selon le framework BANANA et le verrouillage d'identité (Identity Locking).

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Visuals** défini dans `../agent-visuals.md`.
      Annonce : "Ingénierie de la précision. Création de la mascotte de marque."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/01_foundation_strategy.md` (Pour l'Archétype et la psychologie)
      - `brandkit_output/02_verbal_identity.md` (Pour la personnalité et le storytelling)
      - `brandkit_output/03_colors.md` (Pour la palette)
      - `brandkit_output/05_graphic_universe.md` (Pour le style visuel)

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Base stratégique manquante. Définissez l'Univers Graphique et la Fondation avant d'attaquer la mascotte."
      }
      SINON {
          Charge les fichiers en contexte via `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Phase Conceptuelle" file="@_bk/workflows/7-visuals/create-mascot/steps/01_directions.md" />
  
  <step name="Prompting & Framework BANANA" file="@_bk/workflows/7-visuals/create-mascot/steps/02_prompting.md" />
  
  <step name="Identity Locking & Variantes" file="@_bk/workflows/7-visuals/create-mascot/steps/03_identity_locking.md" />
  
  <step name="Clôture">
    <action>
      Rédige le document final `brandkit_output/visuals/09_mascot_prompts.md` en utilisant le template `mascot-template.md`.
      Confirme que le guide Mascotte est enregistré.
    </action>
  </step>
</workflow_steps>
