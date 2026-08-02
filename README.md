# qLag.github.io

Le site développeur racine, servi sur `https://qlag.github.io/`.

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

## index.html

Une page d'accueil minimale. Elle n'a pas d'autre fonction que d'éviter un 404 à la
racine : un domaine développeur qui ne répond pas est un mauvais signal, pour le robot
comme pour un joueur curieux.
