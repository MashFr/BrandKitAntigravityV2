# Scénographie & Mockups Propriétaires : {{PROJECT_NAME}}

## 1. Direction Scénographique
- **Ambiance de Set** : {{SET_ATMOSPHERE}} (ex: Studio minimaliste, Setup extérieur, Bureau créatif...)
- **Lumière & Ombres** : {{LIGHTING_STYLE}} (ex: Hard shadows, Soft daylight, Studio lighting...)
- **Surfaces & Textures** : {{SURFACE_MATERIALS}} (ex: Béton brossé, Papier recyclé, Verre dépoli...)

---

## 2. Set de Mockups (Shot List)

### Mockup Digital (Hardware)
> **Appareil** : {{MOCKUP_DIGITAL_DEVICE}}
> **Contexte** : {{MOCKUP_DIGITAL_CONTEXT}}
```text
[VARIABLES]
OBJET = "{{MOCKUP_DIGITAL_DEVICE}} with a blank screen"
SURFACE = "{{SURFACE_MATERIALS}}"
LUMIERE_AMBIANCE = "{{LIGHTING_STYLE}}, {{SET_ATMOSPHERE}}"

[EXECUTION]
Génère une photo haute qualité de OBJET posé sur SURFACE. Applique LUMIERE_AMBIANCE.
Contraintes : photorealistic, studio lighting, sharp focus, blank and plain screens for easy replacement --no text on screen, UI elements, complex patterns on the screen --ar 16:9
```

### Mockup Print / Packaging
> **Objet** : {{MOCKUP_PRINT_OBJECT}}
> **Détail** : {{MOCKUP_PRINT_DETAIL}}
```text
[VARIABLES]
OBJET = "{{MOCKUP_PRINT_OBJECT}}, blank plain surface"
SURFACE = "{{SURFACE_MATERIALS}}"
LUMIERE_AMBIANCE = "{{LIGHTING_STYLE}}, {{SET_ATMOSPHERE}}"

[EXECUTION]
Génère une photo haute qualité de OBJET posé sur SURFACE. Applique LUMIERE_AMBIANCE. Détail : {{MOCKUP_PRINT_DETAIL}}.
Contraintes : photorealistic, studio lighting, sharp focus, blank and plain surfaces for easy replacement --no text on object, logos, complex patterns on the object --ar 16:9
```

### Scène de Marque (Lifestyle/Setup)
> **Concept** : {{MOCKUP_SCENE_CONCEPT}}
```text
[VARIABLES]
SUJET = "{{MOCKUP_SCENE_CONCEPT}}"
SURFACE = "{{SURFACE_MATERIALS}}"
LUMIERE_AMBIANCE = "{{LIGHTING_STYLE}}, {{SET_ATMOSPHERE}}"

[EXECUTION]
Génère une photo haute qualité représentant SUJET sur SURFACE. Applique LUMIERE_AMBIANCE.
Contraintes : photorealistic, studio lighting, sharp focus, cohesive lifestyle shot --no people faces, logos, text, low quality --ar 16:9
```

---

## 3. Guide Technique Nanobanana
- **Tokens "Clean"** : `high resolution`, `commercial photography`, `studio setup`, `depth of field`.
- **Paramètres** : `--ar 16:9`, `--style raw`.
- **Note** : Ces images servent de base pour incruster vos designs réels (Photoshop).
