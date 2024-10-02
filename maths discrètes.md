# PART 1 : Arithmétique :

## Div Euclidienne

## Bases
1. **définition d'une base**
	- $A = (a_n + a_{n-1} + ... + a_1 + a_0)_b$
	- $A = a_0 * b^0 +  a_0 *b^1 +  ... + a_0 *b^n$  
2. **conversion en base 10**
	- $1789_{16} = 9 * 16^0 + 8 * 16^1 + 7 * 16^2 + 1 * 16^3$
	- $1789_{16} = 6025_{10}$
3. **conversion en base b**
	-  succession de div euclidiennes
		- $1789 = (111*16 + 13)$  
		- $1789 = ((6*16+15)*16 +13)$
		- $1789 =  (((0*16 + 6)*16 +15)*16+13)$
		- $1789 = (6.15.13)_{16}$
		- $1789 = (6FD)_{16}$
	- recherche de puissances de la base
		- $1789 = 6 * 16^0 + 15 * 16^1 + 13 * 16^2$
		- $1789 = (6FD)_{16}$
4. **$(A)_b * (B)_b = (C)_b$**
	-  $(32)_b * (14)_b = (438)_b$
		- $(3b + 2)(b+4) = (4b^2 + 3b+8)$
		- $3b^2+14b+8 = 4b^2+3b+8$
		- $-2b^2+11b = 0$
		- $b(-2b+11) = 0$
		- S{0;11} or la base 0 n'est pas possible du coup b=11
	-  $(27)_b * (35)_b = (758)_b$
		-  $(2b+7)(3b+5)= (7b^2+5b+8)$
		- $-b^2+16b+27=0$
		- delta = 784
		- $x_1 = (-26-784^{1/2})/-2 = 27$
		- $x2= (-26+784^{1/2})/-2 = -1$
		- S{-1;17} or la base -1 n'est pas possible du coup b=27

>  $(1789)_8$  n'est pas possible parce qu'il contient des nombres >= à sa base (8 et 9) 

## Arithmétique
1. **deux nombres premier entre eux**
	> On dit que deux entiers a et b sont premier entre eux si :
	> ils n'ont en PGCD **que 1**. (a^b = 1)
2. **Théorème de Bézout (id de Bézout)**
   	- $d=a$^$b$ ssi il existe u,v deux nombres entiers (dans l'ensemble Z) tel que :
   	- **$d = au+bv$**
   	- --------------------------
   	- en gros, si tu trouve u et v, $d = a$^$b$
   
3. **liste des diviseurs d'un entier**
   	- $nb_div = (aplha_1 + 1)(aplha_2 + 1)$...$(aplha_3 + 1)$
   	- --------------------------
   	- en gros tu décompose ton nombre a en produit de facteur premier, et tu multiplie chaque exposant (alpha) +1, entre eux.
	- puis après tu fait l'arbre des possibilitées (c long en crabe)
 
4. **calcul du PGCD/PPCM par  décomposition**
   	- tu décompose a et b en produit de facteur premier
   	- tu check le plus petit exposant de chaque facteur premier
   	- a^b c'est le produit des facteur de a ou de b les plus petit (si t'a pas compris regarde la partie guidée)
     
5. **calcule du PGCD/PPCM par l'algorithme d'Euclide**
	> PGCD
 
	|NB_lignes|Dividende (a)|Diviseur (b)|Reste (r)|
	|---------|-------------|------------|---------|
	|1        |R1: a        |R2: b       |R3: a/b  |
	|2        |R2           |R3          |R4: R2/R3|
	|3        |R3           |R4          |R5: R3/R4|
	|4        |R4           |R5          |R6: R4/R5|
	|5        |R5           |R6          |R7: ...  |
	|N        |RN           |RN+1        |**RN+2: 0**|

	- tu suis le tableau, puis dès que le reste fait 0, tu prend le reste d'avant
 	- -------------------------- 
	- en gros, si tout en bas à droite, RN+2 = 0, tu prend le reste de la ligne du dessus 
&nbsp;
 	> PPCM
  
  	- (a^b)(a_b) = a*b **donc** (a^b)a*b = (a_b)
	
10. **info en plus je savais pas où la mettre tu m'excusera on est pas à ça près, plutôt même à ça loin, mais bon c'est pas non plus un concours de bite à savoir qui à la plus grosse, parce qu'on sait tous que c'est moi qui l'ai... voila voila...** 
> (a^b)(a_b) = a*b &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a_b : PPCM mais y a pas le circonflex inversé

### Pratique guidée
> $a=132$ et $b=108$
1. **décomposition en produits de facteurs premiers**
	- $132 = 2^2*3+11$
	- $108 = 2^2*3^3$
2. **liste des diviseurs d'un entier**
	- $132 = 2^2 * 3 + 11$
	- $nbdiv = (2+1)(1+1)(1+1)=12$
	> faire l'arbre des possibilitées (c long en crabe)
3. **calcul du PGCD et du PPCM par décomposition**
	- $132$ PGCD $108 = 2^2 * 3^1 =12$
	- $132$ PPCM $108 = 2^2 * 3^3 * 11 = 1188$
4. **calcul du PGCD et du PPCM par l'algorithme d'Euclide**

	
## Calcul Modulaire
1. **BlipBloup**
