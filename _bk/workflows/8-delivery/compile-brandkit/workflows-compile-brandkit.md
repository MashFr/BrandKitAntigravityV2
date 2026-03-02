---
description: Workflow Compile BrandKit (Aura Compiler)
---

# Workflow : Compile BrandKit

Ce workflow rassemble tous les textes de la marque en un document "Charte Graphique" unifié, structuré, et expurgé de tout bruit technique. 

<workflow_steps>
  <step name="Initialisation">
    <action>
      Active le persona **Aura Compiler** défini dans `../agent-compiler.md`.
      Annonce : "Initialisation d'Aura Compiler. Préparation de la structure de livraison de la Charte Graphique."
    </action>
  </step>

  <step name="Création Arborescence" file="@_bk/workflows/8-delivery/compile-brandkit/steps/01_structure.md" />
  
  <step name="Compilation & Filtrage" file="@_bk/workflows/8-delivery/compile-brandkit/steps/02_compilation.md" />

  <step name="Clôture">
    <action>
      Confirme que la charte graphique est prête dans le dossier sécurisé.
      Informe l'utilisateur qu'il peut déplacer ses ressources générées dans les dossiers correspondants, puis utiliser le second workflow `/populate-assets`.
    </action>
  </step>
</workflow_steps>
