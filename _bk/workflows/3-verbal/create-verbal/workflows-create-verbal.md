---
description: Workflow complet d'Identité Verbale (Naming, Tagline, Tonalité)
---

# Workflow : Identité Verbale

Ce workflow conçoit une identité verbale propriétaire qui différencie immédiatement la marque.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Verbal** défini dans `../agent-verbal.md`.
      Annonce : "Donnons une voix à votre vision. Nous allons créer un univers verbal unique."
    </action>
  </step>

  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `brandkit_output/00_brand_brief.md`
      - `brandkit_output/01_foundation_strategy.md`

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Fichiers manquants. Veuillez exécuter les workflows [Create Brand Brief] et [Create Foundation] pour générer les fichiers requis avant de continuer."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Naming Stratégique" file="@_bk/workflows/3-verbal/create-verbal/steps/01_naming.md" />
  
  <step name="Taglines" file="@_bk/workflows/3-verbal/create-verbal/steps/02_taglines.md" />
  
  <step name="Charte Sémantique" file="@_bk/workflows/3-verbal/create-verbal/steps/03_lexique.md" />
  
  <step name="Résonance & Synthèse" file="@_bk/workflows/3-verbal/create-verbal/steps/04_resonance.md" />
  
  <step name="Clôture">
    <action>
      Confirme que l'identité verbale est enregistrée dans `brandkit_output/02_verbal_identity.md`.
    </action>
  </step>
</workflow_steps>
