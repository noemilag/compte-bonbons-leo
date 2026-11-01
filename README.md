# Halloween Dashboard · Le butin hanté de Léo 🎃

Les récoltes de bonbons d'Halloween de Léo, année après année, en chiffres et en graphiques animés.

**En ligne :** https://noemilag.github.io/halloween-dashboard/

## Les fichiers

- `index.html` : toute l'app (graphiques faits avec [d3](https://d3js.org), polices Creepster, Luckiest Guy et Fredoka de Google Fonts).
- `data/bonbons.csv` : le décompte de Léo, une ligne par sorte de bonbon et par année.
- `data/soirees.csv` : les infos de chaque soirée (heures de marche, sacs donnés à la porte).
- `icon-*.png`, `favicon-*.png`, `apple-touch-icon.png`, `manifest.webmanifest` : l'icône de l'app.

## Ajouter une nouvelle année

Pas besoin de toucher à `index.html`. Il suffit d'ajouter des lignes à la fin des deux fichiers CSV.

`data/bonbons.csv` : une ligne par sorte de bonbon.

```
annee,categorie,bonbon,quantite,gros
2027,Chocolat,Kit Kat,14,0
2027,Bonbons durs,Rockets,80,0
```

- `categorie` : Chocolat, Chips, Bonbons durs, Jujubes, Spécial ou Réglisse. Une nouvelle catégorie fonctionne aussi.
- `gros` : le nombre de formats géants compris dans la quantité (0 s'il n'y en a pas).

`data/soirees.csv` : deux lignes par année.

```
annee,mesure,valeur
2027,heures_marche,2.5
2027,sacs_donnes,60
```

Dès qu'il y a deux années, un sélecteur d'année apparaît en haut, chaque chiffre affiche l'écart avec l'année précédente et le chapitre 5 compare les récoltes.

Astuce : prends la feuille de décompte en photo et demande à Claude de l'ajouter.

Note : la page lit ses données avec `fetch`, donc elle doit être ouverte depuis GitHub Pages (ou un petit serveur local), pas en double-cliquant sur `index.html`.
