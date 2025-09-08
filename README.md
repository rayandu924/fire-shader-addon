# 🔥 Fire Shader Addon

Addon d'effet de feu animé en temps réel pour MyWallpaper utilisant WebGL avec des paramètres entièrement personnalisables.

## ✨ Fonctionnalités

- **Effet de feu réaliste** : Utilise des shaders WebGL pour un rendu fluide
- **Entièrement personnalisable** : Couleurs, intensité, vitesse, échelle
- **Performance optimisée** : WebGL2 pour un rendu 60fps
- **Responsive** : S'adapte à toutes les résolutions d'écran
- **Intégration MyWallpaper** : Communication temps réel avec l'interface

## 🎮 Paramètres

### Couleurs
- **Couleur Principale** : Orange-rouge principal du feu
- **Couleur Secondaire** : Rouge foncé des flammes intenses
- **Couleur de Fond** : Arrière-plan (généralement noir)

### Animation
- **Intensité** : Contrôle la force générale de l'effet (0.0-2.0)
- **Vitesse** : Vitesse de montée des flammes (0.0-1.0)
- **Turbulence** : Niveau de chaos dans le mouvement (0.0-2.0)

### Rendu
- **Échelle** : Taille des détails (1.0-15.0, plus petit = plus de détails)
- **Opacité** : Transparence globale (0.0-1.0)

## 🚀 Installation

1. Téléchargez ou clonez ce repository
2. Assurez-vous d'avoir tous les fichiers requis :
   - `index.html`
   - `script.js` 
   - `styles.css`
   - `addon.json`
   - `preview.png` (à ajouter)
3. Créez une release GitHub avec un tag de version
4. Ajoutez l'URL du repository dans MyWallpaper

## 🔧 Développement

Le shader utilise plusieurs techniques :
- **Fractional Brownian Motion (FBM)** pour le bruit fractal
- **Interpolation cubique** pour des transitions fluides  
- **Multicouches de bruit** pour la complexité visuelle
- **Gradient dynamique** pour l'effet de flamme qui monte

### Structure du code

```javascript
// Shaders
- Vertex Shader : Position des vertices
- Fragment Shader : Calcul des couleurs pixel par pixel

// Classes principales
- FireShaderAddon : Gestionnaire principal
- WebGL setup : Initialisation du contexte
- Settings management : Gestion des paramètres temps réel
```

## 📋 Compatibilité

- **WebGL2** requis (navigateurs modernes)
- **Toutes résolutions** supportées
- **Performance** : ~60fps sur hardware moderne

## 🎨 Personnalisation

L'addon suit les conventions MyWallpaper :
- Communication via `postMessage`
- Paramètres définis dans `addon.json`
- Design responsive avec unités relatives
- Intégration transparente

## 📝 Licence

Créé pour MyWallpaper - Inspiré du code de démonstration fourni, entièrement réécrit pour éviter les problèmes de droits d'auteur.