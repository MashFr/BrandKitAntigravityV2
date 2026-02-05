---
description: Workflow de création de l'Univers Graphique (Manifeste, Formes, Motifs, Mise en page)
---

# Workflow : Univers Graphique

Ce workflow définit le langage visuel de la marque : formes, motifs et règles de composition.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Universe** défini dans `../agent-universe.md`.
      Annonce : "Définissons la grammaire visuelle de votre monde."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md`
      - `brandkit_output/01_foundation_strategy.md`
      - `brandkit_output/02_verbal_identity.md` (Pour le Ton de voix & Manifeste)
      - `brandkit_output/03_colors.md` (Pour les Motifs)
      - `brandkit_output/04_typography.md` (Pour le Layout)

      SI (les fichiers essentiels sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Stratégie manquante. L'univers graphique doit s'appuyer sur le fondement stratégique."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Manifeste Graphique" file="@_bk/workflows/6-universe/create-graphic-universe/steps/01_concept.md" />

  <step name="Formes Primaires" file="@_bk/workflows/6-universe/create-graphic-universe/steps/02_shapes.md" />
  
  <step name="Système de Motifs" file="@_bk/workflows/6-universe/create-graphic-universe/steps/03_patterns.md" />
  
  <step name="Mise en Page & Layout" file="@_bk/workflows/6-universe/create-graphic-universe/steps/04_layout.md" />
  
  <step name="Finalisation" file="@_bk/workflows/6-universe/create-graphic-universe/steps/05_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme que l'univers graphique est enregistré dans `brandkit_output/05_graphic_universe.md`.
      Suggère de passer à la création du Moodboard (Assets) avec l'agent Aura Visuals.
    </action>
  </step>
</workflow_steps>
