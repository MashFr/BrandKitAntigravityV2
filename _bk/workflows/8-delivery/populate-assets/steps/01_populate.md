---
description: Step 1 - Scan des Répertoires et Liaison Markdown
---

<step id="01_populate">
    <action>
        Analyse les fichiers graphiques insérés par l'utilisateur et lie le document Master.
        
        1. **Scanne de l'arborescence** : 
           - Inspecte le dossier `charte-graphique/assets/` et tous ses sous-dossiers (`logo/`, `illustrations/`, `icones/`, etc.).
           - Liste tous les fichiers qui s'y trouvent avec leur chemin relatif (ex : `./assets/logo/logo-definitif.jpg`).

        2. **Identification des correspondances** :
           - Ouvre le fichier de rendu principal `charte-graphique/charte-graphique.md`.
           - Parcours le Markdown à la recherche des balises d'images ("placeholders") générées précédemment.

        3. **Substitution Dynamique** :
           - De manière logique, pour chaque type de placeholder (ex : placeholder de logo), déduis quel fichier réel trouvé dans le sous-dossier correspondant (`assets/logo/`) doit venir le remplacer.
           - Remplace l'URL fictive du placeholder par le chemin relatif réel vers le fichier existant.
           - S'il y a plus d'extensions (par exemple plus de fichiers présents dans le dossier que de placeholders dans le document), ajoute-les dynamiquement à la fin de la section appropriée.

        4. **Sauvegarde** :
           - Sauvegarde les modifications apportées à `charte-graphique.md`.
    </action>
</step>
