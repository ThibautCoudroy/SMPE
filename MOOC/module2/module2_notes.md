## Module 2

### Module 2.1

Exemple d'études dont les résultats ont été controversés.

Je connaissais déjà la première histoire (notamment grace à [la vidéo de ScienceEtonnante](https://youtu.be/yeX_Zs7zztY?si=OUk__7fL6lGyh3-c)) et des politiques du monde entier se basaient de cette statistique erronnée, par "mégarde" d'après les auteurs (bizarrement cela arrangeait la conclusion).

Deuxième exemple sur l'IRM où le bruit n'était pas assez pris en considération.

Autre exemple sur un bug dans un logiciel, mais au final c'est surtout la méthodologie à revoir.

Dernier exemple en cristallographie : Reprise d'un code qui était incorrect et qui a ainsi engendré un souci au niveau de l'analyse.

### Module 2.2

Différents critères à propos de pourquoi c'est difficile de tout faire proprement :

- Manque d'informations (expliciter ses sources, données, choix) => Cahier de laboratoire peut aider
- Mauvaise utilisation de l'ordinateur (tableur alors que ce n'est pas forcèment adapté à cause de macro et formatage automatique) + de logiciels dont on ne sait pas si le contenu est correct
- Manque de riqueur / organisation (backup, historique, etc.)
- Dimension culturelle et sociale (éthique des données etc.)
- Rendre public ou non (on peut trouver des erreurs ou voir les faiblesses dans notre étude, d'autres peuvent réutiliser notre code ou données, il y a des données sensibles (mais on peut utiliser de l'anonymisation crypto)).

Outils à éviter et alternatives

1. Eviter suite Microsoft, privilégier les formats texte
2. Eviter les logiciels propriétaires comme matlab et privilégier Scilab, R, Python
3. Utiliser des clouds qui garantissent la pérennité (GitHub, GitLab)
4. Outils "intuitifs" qui ne permettent pas de voir ce qu'il se passe derrière le rideau

### Module 2.3

Principes du document computationnel :
- Inspecter ce qui a été fait (comprendre choix etc.)
- Refaire (reproduire, utiliser les mêmes données, etc.)

La vitrine est lue par le lecture, mais s'il veut en savoir plus il doit avoir accès au code qui génère les graphiques, données, etc.

### Module 2.5

Pour préparer un document à publier, on doit pouvoir générer le PDF et cacher les cellules non nécessaires à la compréhension globale.

Il faut bien configurer et convaincre les co-auteurs (qui n'aiment pas qu'on change leurs habitudes !).

On peut mieux s'assurer de la qualité de ce qu'on produit puisqu'on travaille à plusieurs.

Il faut bien faire attention à la pérennité de ce que l'on produit.

"Sites compagnons" qui permettent de partager via des outils d'archivage si on ne veut/peut pas passer par GitHub et GitLab.

Grace au document computationnel, on voit comment s'articule la recherche avec transparence et on peut mieux réutiliser les travaux.

### Module 2.6

Comparaison des trois outils proposés :

- Pour un cours/tuto : Un notebook Jupyter est idéal car facile à prendre en main et document dynamique
- Journal perso : Org-mode permet de classer et étiquetter très efficacement les notes, exemples, etc.
- Cahier de laboratoire : Org-mode est aussi adapté, ici pour plusieurs auteurs.
- Un article reproductible : Exemple avec Org-mode, plus complexe mais plus puissant et plus permissif. Jupyter est le plus compliqué pour générer un article.

Le plus important, c'est de collecter l'info, l'organiser et la rendre exploitable et la rendre disponible.

