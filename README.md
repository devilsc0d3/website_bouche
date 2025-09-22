
# Sommaire
1. Présentation du projet
2. Fonctionnalités principales
3. Technologies utilisées
4. Structure du projet
5. Design & Accessibilité
6. SEO & Référencement
     - robots.txt
     - sitemap.xml
     - JSON-LD (schema.org)
7. Performance
8. Configuration serveur (explications .htaccess)
9. Formatage du code (Prettier)
10. Sécurité

---

## 1. Présentation du projet
Ce site vitrine présente les services d'une entreprise spécialisée dans le chauffage, la climatisation, la plomberie et la rénovation de salle de bain. Il met en avant l'expertise, les réalisations et les moyens de contact.

## 2. Fonctionnalités principales
- Pages dédiées pour chaque service
- Galerie d'images et vidéos
- Formulaire de contact
- Mentions légales
- Sitemap et robots.txt pour le SEO
- Gestion des erreurs personnalisées (404, 403)

## 3. Technologies utilisées
- HTML5, CSS3
- JavaScript (animations)
- Apache (configuration serveur via .htaccess)
- Prettier (formatage du code)

## 4. Structure du projet
```
front/
    css/         # Feuilles de style
    img/         # Images et vidéos
    js/          # Scripts JS
    web/         # Pages HTML
robots.txt     # Fichier d'indexation SEO
sitemap.xml    # Plan du site pour les moteurs
.htaccess      # Configuration serveur Apache
README.md      # Documentation
```

## 5. Design & Accessibilité
- Design moderne, responsive et épuré
- Contrastes respectés pour la lisibilité
- Navigation claire et accessible au clavier
- Balises ARIA et alternatives textuelles pour les images

## 6. SEO & Référencement
### robots.txt
Permet de contrôler l'accès des robots d'indexation. Exemple :
```
User-agent: *
Disallow: /front/
Allow: /front/web/
Sitemap: https://votre-domaine/sitemap.xml
```

### sitemap.xml
Liste toutes les pages importantes pour faciliter l'indexation par Google et autres moteurs.

### JSON-LD (schema.org)
Ajout de données structurées pour enrichir l'affichage dans les résultats de recherche :
```html
<script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "LocalBusiness",
    "name": "Entreprise Bouche",
    "image": "https://votre-domaine/front/img/icon/logo-b.png",
    "address": {
        "@type": "PostalAddress",
        "streetAddress": "Adresse de l'entreprise",
        "addressLocality": "Ville",
        "postalCode": "Code Postal",
        "addressCountry": "FR"
    },
    "telephone": "Numéro de téléphone",
    "url": "https://votre-domaine/"
}
</script>
```
À placer dans la balise `<head>` de la page principale.

## 7. Performance
- Optimisation des images (formats adaptés, compression)
- Chargement asynchrone des scripts
- Mise en cache via configuration serveur

## 8. Configuration serveur (.htaccess)
- Redirections propres pour chaque route
- Gestion des erreurs personnalisées
- Sécurisation des accès aux images
- Explications détaillées dans le fichier `.htaccess`

## 9. Formatage du code (Prettier)
Pour garantir une base de code homogène :
- Installer Prettier : `npm install --save-dev prettier`
- Ajouter un fichier `.prettierrc` pour la configuration
- Utiliser l'extension VS Code pour le formatage automatique

## 10. Sécurité
- Protection contre le hotlinking d'images
- Gestion des erreurs serveur
- Respect des bonnes pratiques Apache
- Validation des entrées utilisateur (si formulaire)

---

Pour toute question ou contribution, merci de contacter l'administrateur du projet.
