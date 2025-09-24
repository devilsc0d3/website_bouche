# Sommaire

[Présentation du projet](#présentation-du-projet)

[Fonctionnalités du projet](#fonctionnalités-du-projet)

[Technologies utilisées](#technologies-utilisées)

[Optimisation SEO](#optimisation-seo)

[Fichier .htaccess (pour serveurs Apache)](#fichier-htaccess-pour-serveurs-apache)

[Installer et utiliser Prettier](#installer-et-utiliser-prettier)

[clear cache](#forçage-du-clear-cache-avec-v2)

## Fonctionnalités du projet

Ce site web vitrine intègre de nombreuses fonctionnalités modernes pour offrir une expérience optimale aux utilisateurs et améliorer la visibilité sur le web :

- **Responsivité** : Affichage adapté à tous les écrans (ordinateurs, tablettes, mobiles) grâce à Bootstrap 5 et des feuilles de style personnalisées.
- **Optimisation SEO** :
  - Fichier `robots.txt` pour guider les moteurs de recherche
  - Fichier `sitemap.xml` pour l’indexation des pages
  - Balises JSON-LD (schema.org) pour les données structurées
  - Balises canonical pour éviter le contenu dupliqué
  - Balises meta description sur chaque page
- **Dark mode** : Possibilité d’afficher le site en mode sombre pour le confort visuel (via CSS et/ou JavaScript).
- **Personnalisation des couleurs** : Utilisation de plusieurs palettes de couleurs et d’un fichier dédié (`colors_stylesheet.css`).
- **Animations** : Effets d’apparition et transitions pour dynamiser l’interface (`animation.js`).
- **Navigation fluide** : Bouton de retour en haut, menu clair et accessible.
- **Sécurité et performance** :
  - Redirections HTTPS et gestion de l’URL canonique via `.htaccess`
  - Gestion du cache pour accélérer le chargement
  - Protection des fichiers sensibles
- **Formatage du code** : Utilisation de Prettier pour garantir un code propre et homogène.
- **Accessibilité** : Structure HTML sémantique et bonnes pratiques pour faciliter l’accès à tous.
- **Organisation claire des fichiers** : Séparation des pages, styles, scripts et images pour une maintenance facilitée.

---

# Présentation du projet

Ce projet est un site web vitrine pour une entreprise spécialisée dans les domaines du chauffage, de la climatisation, de la plomberie et de la rénovation de salle de bain. Il a pour objectif de présenter les services proposés, les réalisations, ainsi que de faciliter la prise de contact avec les clients.

## Technologies utilisées

Le projet utilise les technologies et outils suivants :

- **HTML5** : Structure des pages web
- **CSS3** : Mise en forme et design (fichiers personnalisés et Bootstrap 5)
- **JavaScript** : Animations et interactions (fichier `animation.js`)
- **Bootstrap 5** : Framework CSS pour la responsivité et les composants UI
- **Prettier** : Outil de formatage du code

Les fichiers sont organisés dans le dossier `front/` :

- `web/` : Pages HTML
- `css/` : Feuilles de style CSS
- `js/` : Scripts JavaScript
- `img/` : Images et icônes

---

## Optimisation SEO

Le site a été optimisé pour le référencement naturel (SEO) grâce à plusieurs techniques :

### 1. Fichier `robots.txt`

Permet d'indiquer aux moteurs de recherche quelles pages peuvent être explorées :

```
User-agent: *
Allow: /
Sitemap: http://www.bouche-jc.fr/sitemap.xml
```

### 2. Fichier `sitemap.xml`

Liste les URLs importantes du site pour faciliter l'indexation par les moteurs de recherche :

```xml
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
		<url>
				<loc>https://www.bouche.fr</loc>
				<lastmod>2025-09-22</lastmod>
				<changefreq>monthly</changefreq>
				<priority>1.00</priority>
		</url>
		<url>
				<loc>https://www.bouche.fr/about</loc>
				<lastmod>2025-09-22</lastmod>
				<changefreq>monthly</changefreq>
				<priority>0.80</priority>
		</url>
</urlset>
```

### 3. Balise JSON-LD (schema.org)

Intégration de données structurées pour décrire l'entreprise et améliorer la compréhension du site par Google :

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "LocalBusiness",
    "name": "Entreprise Bouche Jc & Patricia",
    "image": "https://bouche-jc.fr/front/img/icon/logo-c.png",
    "description": "Services de chauffage, climatisation, plomberie, pose de pompe à chaleur et rénovation de salle de bain avec plus de 30 ans d'expérience.",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Vallègue",
      "postalCode": "31290",
      "addressCountry": "FR"
    },
    "telephone": "+33 6 46 45 08 49",
    "email": "jcbouche@orange.fr",
    "url": "https://bouche-jc.fr"
  }
</script>
```

### 4. Balise Canonical

Permet d'indiquer l'URL principale d'une page pour éviter le contenu dupliqué :

```html
<link rel="canonical" href="https://bouche-jc.fr" />
```

---

Ces éléments permettent d'améliorer la visibilité du site sur les moteurs de recherche et d'assurer une indexation optimale.

---

## Fichier `.htaccess` (pour serveurs Apache)

Le fichier `.htaccess` permet de configurer le serveur web Apache pour améliorer la sécurité, la performance et le SEO du site. Voici quelques usages courants :

- **Redirections 301** : Rediriger les anciennes URLs vers les nouvelles pour conserver le référencement.
- **Forcer le HTTPS** : Assurer que toutes les pages sont accessibles en HTTPS pour la sécurité et le SEO.
- **Définir l’URL canonique** : Éviter le contenu dupliqué en redirigeant vers l’URL principale.
- **Gestion du cache** : Améliorer la vitesse de chargement en contrôlant la mise en cache des fichiers.
- **Protection des fichiers sensibles** : Restreindre l’accès à certains fichiers ou dossiers.

Exemple de redirection vers HTTPS et gestion de l’URL canonique :

```apache
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}/$1 [R=301,L]

# Redirection vers l’URL canonique
RewriteCond %{HTTP_HOST} ^www\.bouche-jc\.fr [NC]
RewriteRule ^(.*)$ https://bouche-jc.fr/$1 [R=301,L]
```

Le fichier `.htaccess` doit être placé à la racine du site sur un serveur Apache. Il est essentiel pour contrôler le comportement du site et optimiser le référencement.

---

## Installer et utiliser Prettier

Prettier est un outil de formatage automatique du code qui permet d'assurer une cohérence et une lisibilité optimale dans tous les fichiers du projet.

### Installation

1. Ouvrir un terminal à la racine du projet.
2. Installer Prettier en tant que dépendance de développement :

```bash
npm install --save-dev prettier
```

### Utilisation

1. Pour formater tous les fichiers du projet, exécuter :

```bash
npx prettier --write .
```

2. Pour formater un fichier spécifique :

```bash
npx prettier --write chemin/vers/fichier.js
```

### Intégration avec VS Code

Il est recommandé d'installer l'extension Prettier dans Visual Studio Code pour un formatage automatique à chaque sauvegarde :

- Chercher "Prettier - Code formatter" dans le marketplace des extensions VS Code
- Installer l'extension
- Activer le formatage à la sauvegarde dans les paramètres :
  - `"editor.formatOnSave": true`

---

# Forçage du clear cache avec ?v=2

Pour s'assurer que les utilisateurs reçoivent toujours la dernière version des fichiers statiques (CSS, JS, images), le projet utilise le versioning dans les liens des ressources, par exemple :

```html
<link href="/front/css/index_stylesheet.css?v=2" rel="stylesheet" />
```

L'ajout du paramètre `?v=2` (ou tout autre numéro de version) dans l'URL permet de forcer le navigateur à recharger le fichier au lieu d'utiliser une version mise en cache. À chaque mise à jour importante d'un fichier, il suffit d'incrémenter ce numéro pour garantir que tous les visiteurs voient les modifications immédiatement.

Cette technique est particulièrement utile pour éviter les problèmes d'affichage liés au cache lors de la publication de nouvelles versions du site.
