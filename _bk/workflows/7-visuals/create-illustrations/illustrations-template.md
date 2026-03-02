# Système d'Illustration : {{PROJECT_NAME}}

## 1. Direction Artistique (Illustration Style)
- **Style Visuel** : {{ILLUSTRATION_STYLE_NAME}} (ex: Ligne claire, Collage digital, Aquarelle abstraite, 2D Flat...)
- **Palette de Couleur** : {{ILLUSTRATION_COLORS}}
- **Texture & Grain** : {{ILLUSTRATION_TEXTURE}}

---

## 2. Template de Prompt (Master)
Utilisez ce template pour créer de nouvelles illustrations cohérentes. Remplacez simplement la description entre crochets.

```text
[VARIABLES]
SCENE = "[DESCRIPTION DE LA SCÈNE]"
ART_STYLE = "{{ILLUSTRATION_STYLE_NAME}}"
PALETTE = "{{ILLUSTRATION_COLORS}}"
LUMIERE_COMPO = "{{ILLUSTRATION_TEXTURE}}"

[EXECUTION]
Génère une illustration représentant SCENE. Applique le ART_STYLE avec PALETTE.
Assure-toi d'utiliser LUMIERE_COMPO.
Contraintes : artistic illustration, cohesive narrative --no icons, logos, mascots, 3d characters, ui mockups, photorealistic --ar 16:9 --style raw
```
> *Exemple : Remplacer `[DESCRIPTION DE LA SCÈNE]` par "Two colleagues brainstorming on a whiteboard in a modern office".*

---

## 3. Catalogue d'Illustrations (9 Prompts Prêts à l'Emploi)
Voici 9 variations prêtes à être générées pour couvrir vos besoins (Site Web, Slides, Blog...) :

{{ILLUSTRATION_PROMPTS_LIST}}

---

## 3. Guide de Prompting (Nanobanana)
- **Tokens de Style** : `{{STYLE_TOKENS}}`
- **Artist References** (Optionnel) : `in the style of {{ARTIST_NAME}}`
- **Technical Specs** : `--ar 16:9`, `--style raw`, `--v 6.0` (ou équivalent Nanobanana)

---

## 4. Spécifications de Sortie
- **Format** : {{OUTPUT_FORMAT}}
- **Usage recommandé** : {{USAGE_RECOMMENDATION}}
