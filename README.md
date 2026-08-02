# qLag.github.io

Le site développeur racine, servi sur **https://qlag-apps.fr**.

Le fichier `CNAME` porte le domaine : le supprimer ferait retomber le site sur
`qlag.github.io` et casserait l'URL déclarée dans la Play Console.

Il existe pour une raison précise : **AdMob cherche `app-ads.txt` à la racine du
domaine déclaré comme site web sur la fiche Play**, jamais dans un sous-dossier. Le
dépôt `legal` est servi sous `/legal/` et ne peut donc pas héberger ce fichier.

## app-ads.txt

Une seule ligne, celle fournie par AdMob :

```
google.com, pub-9368372314588950, DIRECT, f08c47fec0942fa0
```

`pub-9368372314588950` est la référence éditeur AdMob. Elle est publique par nature —
c'est tout l'objet du fichier : déclarer qui est autorisé à vendre notre inventaire
publicitaire. Sans lui, une partie des acheteurs refuse d'enchérir.

Ne pas y ajouter de commentaire au-dessus de la ligne, ne pas le renommer, ne pas le
déplacer. Le robot AdMob peut mettre jusqu'à 24 heures à le relire après publication.

## Les pages

- `index.html` — la vitrine, une carte par application.
- `qelm/` — la page de présentation de « Quelle est la marque ? ».
- `style.css` — une seule feuille pour tout le site.
- `assets/<app>/` — icône et captures, redimensionnées à 640 px de large.

Les politiques de confidentialité ne sont **pas** ici : elles vivent dans le dépôt
`legal`, servi sous `/legal/`, et leurs URL sont déjà déclarées dans la Play Console.
Ne les déplacez pas — une URL de politique qui tombe en 404 fait retirer l'application.

## Ajouter une application

Un dossier `<app>/` avec son `index.html`, un dossier `assets/<app>/` pour les images,
et une carte de plus dans la liste de la page d'accueil. Rien d'autre à toucher.
