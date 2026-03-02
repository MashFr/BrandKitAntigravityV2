---
description: Workflow Populate Assets (Aura Compiler)
---

# Workflow : Populate Assets

Ce workflow parcourt la structure de dossiers `assets/` créées par la Charte Graphique (Aura Compiler) pour repérer les fichiers réels ajoutés par l'utilisateur, puis met à jour dynamiquement la Charte Graphique avec leurs chemins exacts.

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Compiler** défini dans `../agent-compiler.md`.
      Annonce : "Inspection de l'arborescence des assets. Préparation au liage des médias avec la Charte Graphique principale."
    </action>
  </step>

  <step name="Scan et Liaison" file="@_bk/workflows/8-delivery/populate-assets/steps/01_populate.md" />

  <step name="Clôture">
    <action>
      Informe des assets trouvés et correctement liés dans la Charte Graphique.
      Signale si certains placeholders de la charte n'ont pas encore reçu de fichiers.
      Confirme que la Charte Graphique est prête à l'emploi et enrichie visuellement.
    </action>
  </step>
</workflow_steps>
