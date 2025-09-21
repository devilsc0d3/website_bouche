# Site Web Entreprise Bouche JC & Patricia

## Description du Projet

Site web vitrine pour l'**Entreprise Bouche JC & Patricia**, spécialisée dans les services de chauffage, climatisation, plomberie et rénovation de salle de bain avec plus de 30 ans d'expérience.

**URL du site :** https://bouche-jc.fr  
**Version de développement :** https://devilsc0d3.github.io/website_bouche/front/web/

## 🛠️ Technologies Utilisées

- **HTML5** - Structure sémantique
- **CSS3** - Styles personnalisés et responsive design
- **JavaScript** - Animations et interactions
- **Bootstrap 5.3.3** - Framework CSS pour la responsivité
- **GSAP** - Animations avancées
- **Video HTML5** - Vidéo de fond en header

## 📁 Structure du Projet

```
website_bouche/
├── README.md
├── robots.txt                    # Configuration SEO pour les robots
├── sitemap.xml                   # Plan du site pour les moteurs de recherche
├── .htaccess                     # Configuration serveur Apache
└── front/
    ├── css/                      # Feuilles de style
    │   ├── index_stylesheet.css
    │   ├── about_stylesheet.css
    │   ├── colors_stylesheet.css
    │   ├── footer_stylesheet.css
    │   ├── mention-legales.css
    │   └── sitemap_stylesheet.css
    ├── img/                      # Images et médias
    │   ├── icon/                 # Icônes et logos
    │   └── photo/                # Photos des réalisations
    ├── js/
    │   └── animation.js          # Animations GSAP
    └── web/                      # Pages HTML
        ├── index.html            # Page d'accueil
        ├── about.html            # Page activités/services
        ├── mention-legal.html    # Mentions légales
        ├── sitemap.html          # Plan du site
        └── 404.html              # Page d'erreur 404
```

## 🎯 Fonctionnalités Implémentées

### 1. Design & UX

- ✅ Design responsive (mobile-first)
- ✅ Vidéo de fond en header avec fallback image
- ✅ Animations fluides avec GSAP
- ✅ Interface utilisateur moderne et professionnelle
- ✅ Navigation intuitive avec menu hamburger mobile

### 2. Pages Principales

- ✅ **Page d'accueil** (`/`) - Présentation de l'entreprise et services
- ✅ **Page activités** (`/about`) - Détail des services (chauffage, plomberie, climatisation, salle de bain)
- ✅ **Page mentions légales** (`/mention-legal`) - Informations légales
- ✅ **Page plan du site** (`/sitemap`) - Navigation structurée
- ✅ **Page 404** - Gestion des erreurs

### 3. Services Présentés

- 🔥 **Chauffage** - Installation et maintenance chaudières gaz/fioul
- 🚿 **Plomberie** - Pose et réparation
- 🛁 **Salle de bain** - Rénovation complète
- ❄️ **Climatisation & Pompe à chaleur** - Installation et maintenance

## 🔍 Optimisation SEO

### Meta Tags et Structure

- ✅ Balises meta description optimisées
- ✅ Titres H1-H6 structurés
- ✅ Attributs alt pour toutes les images
- ✅ Liens canoniques pour éviter le contenu dupliqué
- ✅ Langue française définie (`lang="fr"`)
- ✅ Meta viewport pour la responsivité
- ✅ Favicon personnalisé

### Contenu SEO

- ✅ Mots-clés ciblés : "chauffage", "plomberie", "climatisation", "salle de bain", "Vallègue", "31290"
- ✅ Contenu riche et informatif
- ✅ Structure sémantique HTML5
- ✅ URLs propres et explicites

## 📄 Configuration robots.txt

Le fichier `robots.txt` est configuré pour optimiser l'indexation :

```txt
User-agent: *
Allow: /
Sitemap: http://www.bouche-jc.fr/sitemap.xml
```

**Fonctionnalités :**

- ✅ Autorise tous les robots d'indexation
- ✅ Référence le sitemap XML
- ✅ Aucune restriction d'accès

## 🗺️ Sitemap.xml

Le sitemap XML facilite l'indexation par les moteurs de recherche :

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://www.bouche.fr</loc>
        <lastmod>2025-09-12</lastmod>
        <changefreq>monthly</changefreq>
        <priority>1.00</priority>
    </url>
    <url>
        <loc>https://www.bouche.fr/about</loc>
        <lastmod>2025-09-12</lastmod>
        <changefreq>monthly</changefreq>
        <priority>0.80</priority>
    </url>
</urlset>
```

**Configuration :**

- ✅ Page d'accueil priorité maximale (1.0)
- ✅ Pages secondaires priorité élevée (0.8)
- ✅ Fréquence de mise à jour mensuelle
- ✅ Dates de dernière modification actualisées

## ⚙️ Configuration .htaccess

Le fichier `.htaccess` gère la réécriture d'URLs et la sécurité :

```apache
RewriteEngine On

# Redirection des routes propres
RewriteRule ^$ front/web/index.html [L]
RewriteRule ^about$ front/web/about.html [L]
RewriteRule ^mention-legal$ front/web/mention-legal.html [L]
RewriteRule ^sitemap$ front/web/sitemap.html [L]

# Gestion des erreurs 404
ErrorDocument 404 /front/web/404.html

# Protection contre le hotlinking d'images
RewriteCond %{HTTP_REFERER} !^$
RewriteCond %{HTTP_REFERER} !bouche-jc\.fr [NC]
RewriteRule \.(jpg|jpeg|png|gif)$ - [F]
```

**Fonctionnalités :**

- ✅ URLs propres sans extension `.html`
- ✅ Redirection automatique vers les bonnes pages
- ✅ Page 404 personnalisée
- ✅ Protection des images contre le vol de bande passante
- ✅ Amélioration de l'expérience utilisateur

## 📱 Responsive Design

- ✅ Breakpoints Bootstrap optimisés
- ✅ Navigation mobile avec menu hamburger
- ✅ Images adaptatives
- ✅ Vidéo responsive en header
- ✅ Grille flexible pour les services
- ✅ Typographie responsive

## 🚀 Performance

### Optimisations

- ✅ Chargement asynchrone des scripts
- ✅ Compression des images
- ✅ CDN pour Bootstrap et GSAP
- ✅ CSS minifié en production
- ✅ Lazy loading implicite pour les vidéos

### Métriques

- ⚡ Temps de chargement optimisé
- 📱 Compatibilité mobile excellente
- 🎯 Core Web Vitals optimisés

## 🔗 Informations de Contact

**Entreprise Bouche JC & Patricia**

- 📍 Adresse : Vallègue, 31290
- 📞 Jean-Christophe : 06 46 45 08 49
- 📞 Patricia : 06 11 52 44 43
- 📧 Email : jcbouche@orange.fr

## 🎨 Identité Visuelle

- **Logo** : Logo personnalisé de l'entreprise
- **Couleurs principales** : Dégradé bleu/violet (#5043c9)
- **Typographie** : Bootstrap default avec personnalisations
- **Icônes** : Icônes personnalisées pour chaque service

## 🔧 Installation et Déploiement

1. **Cloner le repository**

   ```bash
   git clone https://github.com/devilsc0d3/website_bouche.git
   ```

2. **Structure des fichiers**
   - Placer tous les fichiers à la racine du serveur web
   - S'assurer que `.htaccess` est actif (serveur Apache)

3. **Configuration DNS**
   - Pointer le domaine vers le serveur
   - Configurer les sous-domaines si nécessaire

4. **Validation**
   - Tester les redirections d'URLs
   - Vérifier le sitemap dans Google Search Console
   - Valider le robots.txt

## 🛡️ Sécurité

- ✅ Protection contre le hotlinking d'images
- ✅ Headers de sécurité via .htaccess
- ✅ Validation HTML/CSS
- ✅ Liens externes sécurisés

## 📈 SEO et Analytics

### Points d'amélioration futurs

- [ ] Intégration Google Analytics
- [ ] Données structurées Schema.org

---

_Version 1.0 - Septembre 2025_
