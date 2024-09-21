
## Règles @:
**donne des info sur les comportements/instructions pour le CSS**
```
@charset "utf-8"; 		            // donne des infos sur les meta-données
@import url("bluish.css") speech    // indique au css d'importer un autre css  
```
## Requêtes Média :
	• @import url requête_média;
	• @media requête_média;
	
```
@media screen and (min-width: 780px) and (max-width: 979px)
{ /* Liste des règles pour ce mdéia */
	p {font-size: 150%;}
	...
}
@media print
{ /* Liste des règles pour ce mdéia */
	p {font-size: inherit; …}
	⁞
}
```

## Sélecteur d'attribut :
**Permet de cibler des éléments en fonction de la présence ou non d’un attribut.**

**CSS :**
Sélecteur d’attribut
```
p[cat] { color: green; } /existence */
p[cat^="dog"] { color: blue; }  / commence par /
p[cat~="dog"] { color: red; } / valeur dans une liste /
p[cat="dog"] { color: yellow; } /* valeur exacte */
```


**HTML** :
```
<p>Un 1er paragraphe simple</p>
```
```
<p cat>Un 2e paragraphe simple</h3>
```
```
<p cat="matou dog chat">Un 3e paragraphe simple</p>
```
```
<p cat="doggy">Un 4e paragraphe simple</p>
```

**Résultat:**
	Un 1e paragraphe simple (vert)
	Un 2e paragraphe simple (rouge)
	Un 3e paragraphe simple (bleu)
	Un 4e paragraphe simple (jaune)

## Les pseudo-classes :
**Permet d’indiquer l’état spécifique dans lequel un élément ciblé doit être pour utiliser la**
**mise en forme définie.**

```
h1:hover {
	background-color: #F89B4D;
	font-variant-caps: small-caps;
}
p:nth-child( 2 ) { 
	background-color: lightgreen;
}

p:lang(fr) { ... }
a:visited { ... }
a:focus:hover { ... }
```

S’applique à un sélecteur pour **appliquer des styles selon** :
	• **l’état** : fonction de l’état de l’élément ciblé
	• **la position** : compter et cibler les éléments pairs, impair, le n-ième, …
	• **l’information** (meta-données ou autres)


[lien du cours](https://moodle.univ-lille.fr/pluginfile.php/4167327/mod_resource/content/0/R102_pres3_css1.pdf)


