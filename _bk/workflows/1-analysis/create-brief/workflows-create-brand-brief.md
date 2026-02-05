---
description: Workflow de création d'un Brand Brief synthétique
---

# Workflow : Création du Brand Brief

Ce workflow guide l'utilisateur à travers la définition des piliers fondamentaux de sa marque.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura** défini dans `../agent-product-architect.md`.
      Annonce l'objectif : "Nous allons cristalliser l'ADN de votre marque en un document de référence unique."
    </action>
  </step>

  <step name="Chargement des Templates">
    <action>
      Vérifie la présence du template :
      - `_bk/workflows/1-analysis/create-brief/brand-bried-template.md`

      SI (le template est absent) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Template manquant."
      }
      SINON {
          Charge le fichier avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
    
  <step name="Interview" file="@_bk/workflows/1-analysis/create-brief/steps/01_interview.md" />
    
  <step name="Synthèse" file="@_bk/workflows/1-analysis/create-brief/steps/02_synthesis.md" />
    
  <step name="Clôture">
    <action>
      Confirme que le brief est enregistré dans `brandkit_output/00_brand_brief.md`.
    </action>
  </step>
</workflow_steps>