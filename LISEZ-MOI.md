# Suivi de Zone — application installable

Ce dossier contient la version PWA de Suivi de Zone. Elle peut être publiée gratuitement avec GitHub Pages et installée sur Android ou un ordinateur compatible.

## Fichiers

- `index.html` : application Suivi de Zone (version de travail fournie).
- `manifest.webmanifest` : nom, icônes et paramètres d’installation.
- `sw.js` : mise en cache des fichiers nécessaires au lancement hors ligne.
- `icons/` : icônes Android, Apple et favicon.
- `.nojekyll` : évite que GitHub Pages ignore certains fichiers.

## Publier avec GitHub Pages

1. Connectez-vous à https://github.com/ et créez un nouveau dépôt, par exemple `suivi-de-zone`.
2. Choisissez un dépôt **Public** si vous utilisez GitHub Pages gratuit avec un compte personnel, puis créez le dépôt.
3. Dans le dépôt, utilisez **Add file → Upload files** et téléversez tous les fichiers et dossiers de ce dossier. Le fichier `index.html` doit se trouver à la racine du dépôt, pas dans un sous-dossier supplémentaire.
4. Validez l’envoi avec **Commit changes**.
5. Ouvrez **Settings → Pages**.
6. Dans **Build and deployment**, choisissez **Deploy from a branch**, puis la branche `main` et le dossier `/(root)`. Cliquez sur **Save**.
7. Attendez la publication. GitHub affichera l’adresse de l’application, généralement `https://VOTRE-NOM.github.io/suivi-de-zone/`.
8. Ouvrez cette adresse sur le téléphone Android avec **Google Chrome** et laissez l’application se charger entièrement une première fois avec Internet.
9. Dans Chrome, ouvrez le menu `⋮`, puis choisissez **Installer l’application** ou **Ajouter à l’écran d’accueil**. Le libellé dépend de la version de Chrome.
10. Lancez ensuite l’application depuis son icône. Pour vérifier le hors-ligne, ouvrez-la une fois en ligne, attendez quelques secondes, fermez-la, activez le mode avion et relancez-la.

## À savoir sur les données

- GitHub héberge les fichiers de l’application, mais **ne centralise pas automatiquement les données saisies**.
- Les données restent stockées dans le navigateur/appareil utilisé. Pour les partager entre assemblées, utilisez les fonctions d’exportation et d’importation prévues dans l’application.
- Installez/ouvrez l’application sur le bon appareil et faites régulièrement des sauvegardes exportées.
- N’effacez pas les données du navigateur et ne désinstallez pas l’application sans avoir exporté une sauvegarde.
- La première ouverture et l’installation nécessitent Internet. Après la mise en cache initiale, l’application shell peut s’ouvrir hors ligne.
- Une mise à jour du code publié sur GitHub peut être récupérée par le service worker à l’ouverture suivante ; fermez puis rouvrez l’application si une mise à jour ne semble pas appliquée.

## Sécurité

Le mot de passe d’administration intégré à une application HTML côté client ne constitue pas un coffre-fort sécurisé. Ne publiez pas de données personnelles de membres dans le dépôt GitHub. Le dépôt ne doit contenir que le code de l’application, jamais les fichiers exportés de membres, rapports nominatifs ou sauvegardes.

## Limites de cette livraison

Cette livraison prépare une PWA hébergeable sur GitHub Pages. Elle ne génère pas un APK Android et ne publie pas automatiquement l’application dans un compte GitHub. L’installation PWA se fait depuis le navigateur.
