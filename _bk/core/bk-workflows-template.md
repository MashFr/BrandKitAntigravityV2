---
description: [Description du workflow]
---

# Workflow : [Titre du Workflow]

[Description détaillée de l'objectif de ce workflow et de ce qu'il accomplit pour l'utilisateur.]

<workflow_steps>
  <!-- Étape d'initialisation : Activation du Persona -->
  <step name="Initialisation">
    <action>
      Active le persona **[Nom de l'Agent]** défini dans `../[nom-fichier-agent].md`.
      Rappel des principes :
      - [Principe 1]
      - [Principe 2]
      
      Annonce l'objectif : "[Phrase d'accroche pour l'utilisateur]" 
    </action>
  </step>

  <!-- Étape de vérification et chargement des dépendances -->
  <step name="Chargement des Fichiers">
    <action>
      Vérifie la présence des fichiers suivants :
      - `[chemin/fichier_requis.md]`

      SI (les fichiers sont absents) {
          Arrête le workflow.
          Informe l'utilisateur : "⚠️ Fichiers manquants. Veuillez exécuter le workflow [Nom du Workflow Précédent] pour générer [Fichier Manquant] avant de continuer."
      }
      SINON {
          Charge les fichiers en contexte avec `view_file`.
          Passe à l'étape suivante.
      }
    </action>
  </step>
  
  <!-- Étape interne définie directement dans le workflow -->
  <step name="[Nom Étape 1]">
    <action>
      [Action précise à effectuer]
      [Question à poser ou commande à exécuter]
    </action>
  </step>
  
  <!-- Étape externalisée dans un fichier (recommandé pour les étapes complexes) -->
  <step name="[Nom Étape 2]" file="@_bk/workflows/[nom-dossier-workflow]/steps/[nom-fichier-etape].md" />
  
  <!-- Étape de clôture -->
  <step name="Clôture">
    <action>
      Confirme que [Livrable] est finalisé.
      Suggère la prochaine étape logique : [Nom du prochain workflow].
    </action>
  </step>
</workflow_steps>
