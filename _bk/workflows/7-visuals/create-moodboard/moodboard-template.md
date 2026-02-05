# Moodboard & Prompts : {{PROJECT_NAME}}

## 1. Direction Artistique (Visual Brief)
- **Concept** : {{VISUAL_CONCEPT}}
- **Atmosphère** : {{ATMOSPHERE_KEYWORDS}} (ex: Cinematographic, Golden Hour, High Contrast...)
- **Palette** : {{COLOR_PALETTE_REF}}

---

## 2. Master Prompts (Nanobanana)

### Hero Shot (Plan Large / Ambiance)
> **Sujet** : {{HERO_SUBJECT}}
> **Action** : {{HERO_ACTION}}
> **Contexte** : {{HERO_CONTEXT}}
> **Lumière/Style** : {{HERO_LIGHTING}}
> **Paramètres** : `--ar 16:9 --style raw`

```
{{HERO_PROMPT_FULL}}
```

### Portrait / Produit (Plan Moyen)
> **Sujet** : {{PORTRAIT_SUBJECT}}
> **Action** : {{PORTRAIT_ACTION}}
> **Lumière** : {{PORTRAIT_LIGHTING}}
> **Paramètres** : `--ar 4:5 --style raw`

```
{{PORTRAIT_PROMPT_FULL}}
```

### Texture / Détail (Plan Macro)
> **Sujet** : {{DETAIL_SUBJECT}}
> **Matière** : {{DETAIL_MATERIAL}}
> **Lumière** : {{DETAIL_LIGHTING}}
> **Paramètres** : `--ar 1:1 --tile` (si texture répétable)

```
{{DETAIL_PROMPT_FULL}}
```

---

## 3. Spécifications Techniques
- **Modèle de base** : Nanobanana (Flux standard)
- **Ratio d'aspect** :
    - Paysage : `--ar 16:9`
    - Portrait : `--ar 4:5`
    - Carré : `--ar 1:1`
- **Tokens de Style "Negative"** (à éviter) :
    - {{NEGATIVE_PROMPT}} (ex: blurry, low quality, distorted...)
