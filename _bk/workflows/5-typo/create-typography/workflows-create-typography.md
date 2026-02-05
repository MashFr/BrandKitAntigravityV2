---
description: Workflow de création de la Charte Typographique (Choix, Pairing, Hiérarchie)
---

# Workflow : Charte Typographique

Ce workflow définit la structure textuelle de la marque, assurant lisibilité et caractère.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Typography** défini dans `../agent-typography.md`.
      Annonce : "Donnons une forme à vos mots. Architecture et lisibilité d'abord."
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
          Informe l'utilisateur : "⚠️ Fichiers manquants. La typographie dépend de la Stratégie et du Ton de voix. Exécutez les workflows précédents."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <step name="Analyse Voix" file="@_bk/workflows/5-typo/create-typography/steps/01_analysis.md" />
  
  <step name="Pairing Polices" file="@_bk/workflows/5-typo/create-typography/steps/02_pairing.md" />
  
  <step name="Hiérarchie & Échelle" file="@_bk/workflows/5-typo/create-typography/steps/03_hierarchy.md" />
  
  <step name="Finalisation & Guide" file="@_bk/workflows/5-typo/create-typography/steps/04_finalization.md" />
  
  <step name="Clôture">
    <action>
      Confirme que la charte typographique est enregistrée dans `brandkit_output/04_typography.md`.
    </action>
  </step>
</workflow_steps>
