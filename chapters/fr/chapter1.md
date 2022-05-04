---
title: 'ACP avec FactoMineR'
description:
  "Ce chapitre présente l'analyse en composantes principales illustrer à l'aide du package FactoMiner"
prev: null
next: /chapter2
type: chapter
id: 1
---


<exercise id="1" title="Préparation des données" type="slides">

<slides source="chapter1_01_introduction-to-spacy" start="0:165" end="3:01">
</slides>

</exercise>

<exercise id="2" title="Choix des variables et individus">

### Visualiser les données

Avant de réaliser une ACP il est important de connaître les données sur lequelles l'étude va être réalisée et la problématique de l'étude. Ici, nous avons des données concernant des performances à un decathlon, l'objectif sera d'étudier le profil des participants en fonctions de leur performance.

Dans un premier temps, la fonction `head`permet de visualiser les premières lignes du jeu de données.

<codeblock id="01_02_01"></codeblock>


<codeblock id="01_02_03"></codeblock>

</exercise>

<exercise id="3" title="Individus et variables actifs ">

Quand tu passes une chaîne de caractères à un objet `nlp`, spaCy commence par
découper le texte en tokens et crée un objet document. Dans cet exercice, tu vas
en apprendre davantage sur le `Doc`, ainsi que sur ses vues `Token` et `Span`.

### Étape 1

- Utilise `spacy.blank` pour créer l'objet `nlp` français.
- Traite le texte et crée un objet `Doc` affecté à une variable `doc`.
- Sélectionne le premier token du `Doc` et affiche son attribut `text`.

<codeblock id="01_03_01">

Tu peux utiliser les indices dans un `Doc` comme dans une liste Python. Par
exemple, `doc[4]` désigne le token à l'indice 4, qui est le cinquième token dans
le texte. N'oublie pas qu'en Python le premier indice est 0, et pas 1.

</codeblock>

### Étape 2

- Utilise `spacy.blank` pour créer l'objet `nlp` français.
- Traite le texte et crée un objet `Doc` affecté à une variable `doc`.
- Crée les portions du `Doc` pour les tokens "loups gris" et "loups gris et
  renards roux".

<codeblock id="01_03_02">

La création d'une portion d'un `Doc` s'effectue exactement comme pour la portion
d'une liste en Python en utilisant la notation `:`. N'oublie pas que l'indice du
dernier token est _exclu_ – par exemple, `0:4` désigne les tokens à partir de 0
_jusqu'au_ token 4, mais sans inclure le token 4.

</codeblock>

</exercise>
