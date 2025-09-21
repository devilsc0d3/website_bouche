# Site Web Entreprise Bouche JC & Patricia

## Présentation

Site vitrine pour l'**Entreprise Bouche JC & Patricia** : chauffage, climatisation, plomberie, rénovation de salle de bain. Plus de 30 ans d'expérience à Vallègue (31290).

**URL principale :** https://bouche-jc.fr

## 🚀 Fonctionnalités principales

- Design responsive (mobile, tablette, desktop)
- Vidéo de fond en header (page d'accueil)
- Animations GSAP
- Menu hamburger mobile
- Bouton "remonter en haut" sur la page activités
- Carrousels d'images pour chaque service
- Navigation rapide et plan du site
- Mentions légales et page 404 personnalisée

## 🛠️ Technologies

- HTML5, CSS3 (custom + Bootstrap 5.3.3)
- JavaScript (animations, interactions)
- GSAP (animations avancées)
- SVG pour icônes et flèches

## 📁 Structure du projet

```
website_bouche/
├── README.md
├── robots.txt
├── sitemap.xml
├── .htaccess
└── front/
    ├── css/
    │   ├── index_stylesheet.css
    │   ├── about_stylesheet.css
    │   ├── colors_stylesheet.css
    │   ├── footer_stylesheet.css
    │   ├── mention-legales.css
    │   └── sitemap_stylesheet.css
    ├── img/
    │   ├── icon/
    │   └── photo/
    ├── js/
    │   └── animation.js
    └── web/
        ├── index.html
        ├── about.html
        ├── mention-legal.html
        ├── sitemap.html
        ├── 404.html
        └── 403.html
```

## � Design & Accessibilité

- Couleurs principales : dégradé bleu/violet (#5043c9)
- Icônes personnalisées pour chaque service
- Typographie Google Fonts + Bootstrap
- Contraste et lisibilité optimisés
- Boutons et éléments tactiles adaptés mobile

## 🖥️ Pages et contenus

- **Accueil** : présentation, vidéo, services
- **Activités** : carrousels, descriptions détaillées, bouton scroll-to-top
- **Mentions légales**
- **Plan du site**
- **404/403** : pages d’erreur personnalisées

## 🔍 SEO & Performance

- Balises meta description et titre optimisées
- Attributs alt sur toutes les images
- Liens canoniques
- robots.txt et sitemap.xml configurés
- URLs propres via .htaccess
- Chargement asynchrone des scripts
- CDN pour Bootstrap et GSAP
- Images compressées et lazy loading

## 🗺️ Configuration serveur

**.htaccess**

```apache
RewriteEngine On
RewriteRule ^$ front/web/index.html [L]
RewriteRule ^about$ front/web/about.html [L]
RewriteRule ^mention-legal$ front/web/mention-legal.html [L]
RewriteRule ^sitemap$ front/web/sitemap.html [L]
ErrorDocument 404 /front/web/404.html
RewriteCond %{HTTP_REFERER} !^$
RewriteCond %{HTTP_REFERER} !bouche-jc\.fr [NC]
RewriteRule \.(jpg|jpeg|png|gif)$ - [F]
```

## Formatage du code avec Prettier

Prettier permet de formater automatiquement le code du projet pour garantir une cohérence de style.

### Installation

Si Prettier n'est pas installé, lancez :

```bash
npm install --save-dev prettier
```

### Lancer Prettier

Pour formater tous les fichiers du projet, utilisez :

```bash
npx prettier --write .
```

Cela va formater tous les fichiers compatibles dans le dossier courant.

## 📱 Responsive design

- Breakpoints Bootstrap + media queries custom
- Menu mobile, grille flexible, images et vidéos adaptatives

## 🔗 Contact

- **Adresse** : Vallègue, 31290
- **Jean-Christophe** : 06 46 45 08 49
- **Patricia** : 06 11 52 44 43
- **Email** : jcbouche@orange.fr

## 🛡️ Sécurité

- Protection hotlinking images
- Validation HTML/CSS
- Liens externes sécurisés

## 📈 Améliorations futures

- [ ] Intégration Google Analytics

---

_Version 1.1 – Septembre 2025_
