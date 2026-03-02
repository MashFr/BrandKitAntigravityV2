# Mascotte de Marque : {{PROJECT_NAME}}

## 1. Phase Conceptuelle (L'Âme de la Mascotte)
- **Objectif Stratégique** : {{STRATEGIC_GOAL}}
- **Traits de Caractère** : {{CHARACTER_TRAITS}}
- **Psychologie Affective** : {{PSYCHOLOGY_FORM_LANGUAGE}} (ex: deux ovales et un triangle pour stimuler les neurones miroirs)
- **Storytelling** : {{STORYTELLING}}

---

## 2. Character Sheet (Planche de Personnage) - Prompt Initial

> *Ce prompt est destiné à générer la feuille de référence complète (face, profil, 3/4) pour établir l'Identity Locking.*

### Prompt Nanobanana Pro (Pseudo-Code)
```text
[VARIABLES]
SET SUBJECT_A = "{{MASCOT_BASE_DESCRIPTION}}"
SET STYLE_B = "{{MASCOT_STYLE_AND_LIGHTING}}"

[EXECUTE]
EXECUTE SUBJECT_A in SETTING "Studio blanc neutre" with ACTION "Character turn-around sheet: one front view, one profile view, one 3/4 view"
```

### Framework BANANA
- **B (Boundaries)** : {{BOUNDARIES}} (ex: 4K resolution, aspect ratio 16:9, neutral background)
- **A (Audience)** : {{AUDIENCE}} (ex: ajustement pour une cible B2B ou B2C)
- **N (Nuance)** : {{NUANCE}} (ex: textures matte-finish, focal f/1.8, éclairage volumétrique)
- **A (Action)** : {{ACTION}} (ex: T-pose or neutral standing pose from multiple angles)
- **N (Negatives)** : `--no text, watermarks, busy background, asymmetrical features`
- **A (Assessment)** : {{ASSESSMENT}} (ex: Justifier la régularité des proportions faciales sur les 3 vues)

---

## 3. Déclinaisons avec Identity Locking (Reference Stacking)

> **Instructions Nano Banana Pro :**
> - **Slot 1 (Reference)** : Vue de face de la Character Sheet.
> - **Slot 2 (Reference)** : Vue de profil de la Character Sheet.
> - **Slot 3 (Reference)** : Vue de 3/4 de la Character Sheet.
> - **Verrouillage** : "Garde les traits du visage et l'apparence physique exactement identiques aux Images 1, 2 et 3."

### Scène 1 : {{SCENE_1_NAME}}
> **Concept Action** : {{SCENE_1_ACTION}}

**Prompt Nano Banana (Pseudo-Code)**
```text
[VARIABLES]
SET SUBJECT_A = "La mascotte de référence (Slots 1, 2, 3)"
SET STYLE_B = "{{MASCOT_STYLE_AND_LIGHTING}}"

[EXECUTE]
Verrouillage Identité : Maintiens l'apparence exacte du personnage, y compris les traits du visage, la texture et les vêtements tout au long de l'image.
EXECUTE SUBJECT_A in SETTING "{{SCENE_1_SETTING}}" with ACTION "{{SCENE_1_ACTION}}"
```

### Scène 2 : Localisation Textuelle (Test du Rendu Typographique)
> **Concept Action** : {{SCENE_2_ACTION}} (ex: La mascotte tient un panneau ou s'appuie sur un produit avec du texte écrit)

**Prompt Nano Banana (Pseudo-Code)**
```text
[VARIABLES]
SET SUBJECT_A = "La mascotte de référence (Slots 1, 2, 3)"
SET STYLE_B = "{{MASCOT_STYLE_AND_LIGHTING}}"
SET TEXTE_RENDU = "{{SCENE_2_TEXT}}"

[EXECUTE]
Verrouillage Identité : Maintiens l'apparence exacte du personnage, y compris les traits du visage, la texture et les vêtements tout au long de l'image.
EXECUTE SUBJECT_A in SETTING "{{SCENE_2_SETTING}}" with ACTION "{{SCENE_2_ACTION_WITH_TEXT}}"
Assure-toi de rendre le texte "{{SCENE_2_TEXT}}" de manière parfaite et sans artefact.
```
