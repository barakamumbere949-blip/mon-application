# Blocal Store — Télécharge. Découvre. Profite.

Boutique d'applications Android (APK) et de logiciels PC. HTML5 / CSS3 / JavaScript natif, sans dépendance.

## Identité visuelle
- Logo : sac de boutique doré + flèche de téléchargement (`assets/img/logo.svg`, `favicon.svg`).
- Palette inspirée du drapeau : bleu `#0B63D8`, or `#F7C910`, rouge `#CE1021` (variables CSS en haut de `assets/css/style.css`).
- Animations : héros animé avec téléphone d'aperçu, apparition au défilement, survols. Désactivées automatiquement si l'utilisateur réduit les animations.

## Fiche application
Aperçu des images avec légendes (FR/EN) et visionneuse plein écran (flèches, clavier, balayage) · description ·
fonctionnalités · nouveautés de la version · informations (version, taille, mise à jour, éditeur, langues, Android min) ·
permissions Android · configuration requise PC · SHA-256 · licence, parrainage et commissions (gérés par l'application) ·
partage · autres applications.

## Structure
- `index.html`, `assets/` : site public (aucun code d'administration)
- `catalog.json` : applications visibles (publiées ET vérifiées) + WhatsApp + lien du groupe
- `admin-prive/` : administration LOCALE (ignorée par Git, jamais en ligne)

## Tester dans VS Code
Ouvrir le dossier > extension « Live Server » > Open with Live Server.
Admin : http://127.0.0.1:5500/admin-prive/admin.html (mot de passe de 12 caractères à la 1re visite).

## Publier une application
1. Admin > Ajouter : plateforme, lien https du fichier, prix, descriptions, fonctionnalités, nouveautés,
   permissions, 4 à 6 captures AVEC légendes, tutoriels (« Titre | https://lien »), licence et parrainage.
2. « Calculer taille + SHA-256 » depuis le fichier, tester, cocher les 5 vérifications, « Enregistrer et publier ».
3. Admin > Sauvegarde > Exporter catalog.json, remplacer celui de la racine, puis git push.

## Avant la mise en ligne
- `demo:true` → `demo:false` dans `assets/js/app.js`.
- Admin > Paramètres : WhatsApp d'assistance et lien du groupe.
- Compléter la page légale. Activer la double authentification sur GitHub / Netlify.
