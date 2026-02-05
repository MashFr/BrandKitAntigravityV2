---
description: Workflow de définition des Fondations Stratégiques (Why, Archétypes, Valeurs)
---

# Workflow : Fondations Stratégiques

Ce workflow permet de définir l'ADN profond de la marque avec l'aide de l'expert **Aura Strategy**.

<workflow_steps>
<step name="Initialisation">
  <action>
    Active le persona **Aura Strategy** défini dans `../aura_brand_strategist.md`.
    Annonce : "Bienvenue. Nous allons définir la structure porteuse de votre marque. Prêt à creuser ?"
  </action>
</step>

<step name="Chargement des Fichiers">
  <action>
    Vérifie la présence des fichiers suivants :
    - `brandkit_output/00_brand_brief.md`

    SI (les fichiers sont absents) {
        Arrête le workflow.
        Informe l'utilisateur : "⚠️ Fichiers manquants. Veuillez exécuter le workflow [Create Brand Brief] pour générer [00_brand_brief.md] avant de continuer."
    }
    SINON {
        Charge les fichiers en contexte avec `view_file`.
        Passe à l'étape suivante.
    }
  </action>
</step>

<step name="Le Cercle d'Or" file="@_bk/workflows/2-strategy/create-foundation/steps/01_golden_circle.md" />

<step name="Archétypes Jungiens" file="@_bk/workflows/2-strategy/create-foundation/steps/02_archetypes.md" />

<step name="Manifeste des Valeurs" file="@_bk/workflows/2-strategy/create-foundation/steps/03_values.md" />

<step name="Proposition de Valeur & Synthèse" file="@_bk/workflows/2-strategy/create-foundation/steps/04_emotional_value.md" />

<step name="Clôture">
  <action>
    Confirme que la stratégie est enregistrée dans `brandkit_output/01_foundation_strategy.md`.
    Félicite l'utilisateur pour ce travail de fond.
  </action>
</step>
</workflow_steps>
