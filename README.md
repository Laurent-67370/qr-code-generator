# 🎨 Générateur de QR Code

Un générateur de QR code moderne et personnalisable avec une interface intuitive en français.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=flat&logo=javascript&logoColor=%23F7DF1E)

## 🌐 Démo en Direct

**[✨ Essayer l'application](https://laurent-67370.github.io/qr-code-generator)**

## ✨ Fonctionnalités

### 🔗 Génération de QR Codes
- **Saisie d'URL** avec validation automatique
- **Génération instantanée** avec aperçu en temps réel
- **Qualité optimisée** selon l'usage (web, impression, ultra HD)

### 📏 Tailles Personnalisables
- **200-400px** : Idéal pour web et mobile
- **500-800px** : Parfait pour l'impression
- **900-1400px** : Grande qualité
- **1500-2000px** : Ultra HD avec API haute résolution

### 🎨 Personnalisation Visuelle
- **6 palettes de couleurs** prédéfinies optimisées
- **Designs avancés** avec formes personnalisées :
  - Corps : Carré, Rond, Pointu
  - Cadres d'angle : Standard, Arrondi, Cercle
  - Centres d'angle : Carré, Rond, Losange

### 📱 Interface Moderne
- **Design responsive** adapté mobile/tablette/desktop
- **Sections pliables** pour une navigation optimisée
- **Animations fluides** et transitions élégantes
- **Accessibilité** complète (clavier, focus, lecteurs d'écran)

### 💾 Export et Partage
- **Téléchargement PNG** avec gestion CORS avancée
- **Copie de lien** directe vers le presse-papiers
- **Fallback intelligent** si le téléchargement direct échoue

## 🚀 Installation

### Méthode 1 : Clone du repository
```bash
git clone https://github.com/Laurent-67370/qr-code-generator.git
cd qr-code-generator
```

### Méthode 2 : Téléchargement direct
Téléchargez le fichier `index.html` depuis le [repository GitHub](https://github.com/Laurent-67370/qr-code-generator) et ouvrez-le dans votre navigateur.

## 🖥️ Utilisation

1. **Visitez** [laurent-67370.github.io/qr-code-generator](https://laurent-67370.github.io/qr-code-generator) ou ouvrez le fichier `index.html` dans votre navigateur
2. **Entrez** l'URL que vous souhaitez encoder
3. **Ajustez** la taille selon votre usage
4. **Personnalisez** les couleurs et le design (optionnel)
5. **Cliquez** sur "Générer mon QR Code"
6. **Téléchargez** ou copiez le lien de votre QR code

### Raccourcis Clavier
- **Entrée** : Génère le QR code depuis le champ URL
- **Tab/Shift+Tab** : Navigation entre les éléments
- **Espace/Entrée** : Sélection des options de design

## 🛠️ Technologies

### Frontend
- **HTML5** : Structure sémantique et accessibilité
- **CSS3** : Design moderne avec Flexbox/Grid, animations, responsive
- **JavaScript ES6+** : Logique applicative, gestion d'événements, APIs

### APIs Utilisées
- **[QR Server API](https://goqr.me/api/)** : Génération standard (≤600px)
- **[QuickChart API](https://quickchart.io/)** : Haute résolution (>600px)
- **[QRCode Monkey API](https://www.qrcode-monkey.com/)** : Designs avancés

### Fonctionnalités Techniques
- **Validation d'URL** native avec try/catch
- **Gestion d'erreurs** robuste avec fallbacks
- **Performance** optimisée (debouncing, lazy loading)
- **Sécurité** : Validation côté client, échappement XSS

## 📁 Structure du Projet

```
qr-code-generator/
│
├── index.html                 # Application principale (renommée depuis qr_generator.html)
├── README.md                  # Documentation
└── assets/                    # (optionnel pour version modulaire)
    ├── css/
    │   └── styles.css
    ├── js/
    │   └── app.js
    └── images/
        └── screenshots/
```

## 🎯 Cas d'Usage

### 🏢 Professionnel
- **Cartes de visite** avec liens vers portfolios
- **Menus restaurants** vers sites web
- **Événements** avec liens d'inscription
- **Marketing** pour landing pages

### 📚 Éducatif
- **Cours en ligne** avec liens vers ressources
- **Bibliothèques** pour catalogues numériques
- **Présentations** avec compléments web

### 🏠 Personnel
- **Partage WiFi** (avec générateur de liens spéciaux)
- **Réseaux sociaux** profils et contenus
- **Événements familiaux** albums photos

## 🔧 Configuration Avancée

### Modification des APIs
Dans le fichier, vous pouvez modifier les endpoints dans la section `CONFIG` :

```javascript
const CONFIG = {
    apis: {
        qrserver: 'https://api.qrserver.com/v1/create-qr-code/',
        quickchart: 'https://quickchart.io/qr',
        qrmonkey: 'https://api.qrcode-monkey.com/qr/custom'
    }
};
```

### Ajout de Couleurs
Ajoutez des options dans la section HTML des couleurs :

```html
<div class="color-option" data-fg="NOUVEAU_CODE_COULEUR" data-bg="ffffff">
    <div class="color-preview" style="background: linear-gradient(45deg, #NOUVEAU_CODE_COULEUR 50%, #fff 50%);"></div>
    <div><strong>Nouveau Nom</strong></div>
</div>
```

## 🌐 Compatibilité

### Navigateurs Supportés
- ✅ **Chrome** 80+
- ✅ **Firefox** 75+
- ✅ **Safari** 13+
- ✅ **Edge** 80+
- ✅ **Opera** 67+

### Appareils
- 📱 **Mobile** : iOS 13+, Android 8+
- 💻 **Desktop** : Windows 10+, macOS 10.14+, Linux
- 📱 **Tablette** : iPad OS 13+, Android tablets

## 🐛 Problèmes Connus et Solutions

### Téléchargement bloqué
**Problème** : Le téléchargement ne fonctionne pas  
**Solution** : L'application utilise un système de fallback automatique

### QR code flou sur mobile
**Problème** : Qualité dégradée sur petits écrans  
**Solution** : Augmentez la taille à 800px+ pour l'impression

### API indisponible
**Problème** : Service temporairement inaccessible  
**Solution** : L'application bascule automatiquement sur une API alternative

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. **Fork** le projet
2. **Créez** une branche pour votre fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. **Committez** vos changements (`git commit -m 'Add some AmazingFeature'`)
4. **Push** vers la branche (`git push origin feature/AmazingFeature`)
5. **Ouvrez** une Pull Request

### Guidelines
- Respectez l'indentation et le style existant
- Testez sur plusieurs navigateurs
- Documentez les nouvelles fonctionnalités
- Maintenez la compatibilité mobile

## 📄 License

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 👤 Auteur

**Laurent**
- GitHub: [@Laurent-67370](https://github.com/Laurent-67370)
- Portfolio: [laurent-67370.github.io](https://laurent-67370.github.io)
- Projet: [QR Code Generator](https://laurent-67370.github.io/qr-code-generator)

## 🙏 Remerciements

- **QR Server API** pour leur service gratuit et fiable
- **QuickChart** pour les QR codes haute résolution
- **QRCode Monkey** pour les designs avancés
- **La communauté open source** pour l'inspiration

## 📊 Statistiques

- **Taille** : ~45KB (HTML+CSS+JS)
- **Dépendances** : 0 (vanilla JavaScript)
- **Performance** : 95+ sur Lighthouse
- **Accessibilité** : AA WCAG 2.1

---

⭐ **N'hésitez pas à mettre une étoile si ce projet vous a été utile !**
