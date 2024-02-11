# Réalise un niveau à bulle sonore avec Taill'Créons


## Bonjour, Taill'Crons va t'apprendre à faire un thermomètre avec mémoire de température min et max !@unplugged
Suis bien les instructions à chaques étapes et clique sur ``|Next|`` pour passer
 aux prochaines étapes.  
N'hésite pas à cliquer sur le bouton d'aide en forme d'ampoule en cas 
de blocage.  
Si vous êtes deux à cet atelier, faites une étapes sur deux à tour de rôle et entraidez-vous!
Clique sur OK pour commencer.


 ![Image description](https://def773hwqc19t.cloudfront.net/img/actor_cover/2786/18daa29583f7776a3032954d83007d40_Taillcr%C3%A9o.jpg)


## Créer une variable permettant de mémoriser la température actuelle
Dans la boite à outils, clique sur la section ``||Variables||`` et sur 
"créer une variable". Ecrit le nom de la variable "Température actuelle" puis clique sur OK.  
Dans la section ``||Variables||`` Déplace un bloc ``||Variables:définir Température actuelle à 0||`` 
à l'intérieur du bloc ``||Basic:toujours||`` .  
Clique sur ``|Next|``.

``` blocks

basic.forever(function () {
	Température_actuelle = 0
})

```

## Lit la température toute les secondes 
Dans la boite à outils, clique sur la section ``||Input:Entrée||`` et déplace le bloc
 ``||Input:température(°C)|`` à la place du "0".
 Puisque on veut lire la température toutes les secondes, clique sur la section ``||Basic:Base||``
 et déplace un bloc ``||Basic:pause (ms) 100||`` en dessous de ``||Variables:définir Température actuelle à Température (°C)||``.  
 Clique sur la valeur "100" et sélectionne "1 seconde". La valeur 100 ms se change en 1000 ms qui est la même chose que 1 seconde.  
 Clique sur ``|Next|``.

``` blocks
basic.forever(function () {
   let Température_actuelle = input.temperature()
   basic.pause(1000)
})
```

## Affiche la température sur l'écran du microbit 
Dans la boite à outils, clique sur la section ``||Basic:Base||`` et déplace le bloc
 ``||Basic:montrer nombre 0|`` en dessous de ``||Basic:pause (ms) 1000||``.  
 Dans la section  ``||Variables||`` déplacer le bloc  ``||Variables:Température actuelle||`` 
 à la place du 0.  
 Regarde le microbit à gauche de l'écran il doit aficher une valeur de 21 que tu peux modifier avec le thermomètre en restant cliqué dessus et en montant ou descendant. Clique sur ``|Next|``.  

``` blocks
basic.forever(function () {
   let Température_actuelle = input.temperature()
  basic.pause(1000)
  basic.showNumber(Température_actuelle)
})
```

## Essaye dans la vrai vie!
Clique sur ``|Télécharger|`` et patiente le temps que ton programme se transfert vers ton microbit.  
Regarde la température s'afficher sur ton microbit. Tu peux soufler dessus pour voir la température refroidir ou poser ta main dessus pour le réchauffer.  
 Clique sur ``|Next|``.


## Créer une variable pour la température maximale et minimale
Dans la boite à outils, clique sur la section ``||Variables||`` et sur 
"créer une variable". Ecrit le nom de la variable "max" puis clique sur OK.  
Fait la même chose pour créer une variable avec le nom "min" puis clique sur OK.  
Clique sur ``|Next|``.

``` blocks
basic.forever(function () {
   let Température_actuelle = input.temperature()
  basic.pause(1000)
  basic.showNumber(Température_actuelle)
})
```

## Mémoriser la température minimale
Dans la boite à outils, clique sur la section ``||Logic:Logique||`` et déplace un bloc
``||Logic:si vrai alors||`` en dessous de ``||Basic:montrer nombre||``.  
Dans la boite à outils, clique sur la section ``||Logic:Logique||`` et déplace un bloc
``||Logic:0 <0 ||`` à la place du ``||Logic:vrai||``.  
Clique sur ``|Next|``.

``` blocks
basic.forever(function () {
   let Température_actuelle = input.temperature()
  basic.pause(1000)
  basic.showNumber(Température_actuelle)

    if (0 < 0) {
        min = Température_actuelle
    }
})
```


## Mémoriser la température minimale
La température minimale est plus basse donc inférieure (<) à la température actuelle.  
Dans la section  ``||Variables||`` déplacer le bloc  ``||Variables:min||`` 
 à la place du 0 de droite.  
 Dans la section  ``||Variables||`` déplacer le bloc  ``||Variables:Température actuelle||`` 
 à la place du 0 de gauche.
Clique sur ``|Next|``.

``` blocks
basic.forever(function () {
   let Température_actuelle = input.temperature()
  basic.pause(1000)
  basic.showNumber(Température_actuelle)

    if (Température_actuelle < min) {
        
    }
})
```

## Mémoriser la température minimale
Lorsque la température actuelle est plus basse que le minimum alors c'est que la nouvelle température 
minimum est justement la température actuelle que l'on doit mémoriser.  
Dans la section ``||Variables||``, déplace un bloc ``||Variables:définir min à 0||`` 
à l'intérieur du bloc ``||Logic :si Température actuelle < min||``  et déplace le bloc  ``||Variables:température actuelle||``
à la place du 0.  
Clique sur ``|Next|``.

``` blocks
basic.forever(function () {
   let Température_actuelle = input.temperature()
  basic.pause(1000)
  basic.showNumber(Température_actuelle)

    if (Température_actuelle < min) {
        min = Température_actuelle
    }
})
```


## Afficher la température minimale sur l'écran
On souhaite afficher la température minimale mémorisé sur l'écran lorsque l'on appuie sur
le boutin A (à gauche) du microbit.  
Déplace un bloc `||Input:Lorque le bouton A est pressé||``dans un espace vide.  
Déplace un bloc  ``||Basic:montrer nombre||`` à l'intérieur et remplace la valeur 0 par  ``||Variables:min||``
Clique sur ``|Next|``.

``` blocks
 input.onButtonPressed(Button.A, function () {
    basic.showNumber(min)
})

basic.forever(function () {
   let Température_actuelle = input.temperature()
  basic.pause(1000)
  basic.showNumber(Température_actuelle)

    if (Température_actuelle < min) {
        min = Température_actuelle
    }
})
```


## Essaye dans la vrai vie!
Clique sur ``|Télécharger|`` et patiente le temps que ton programme se transfert vers ton microbit.  
Regarde la température s'afficher sur ton microbit.
Souffle dessus pour le refroidir le plus possible. laisse le ensuite se réchauffer.
Appuie sur le bouton A pour afficher ton score de température le plus bas. Passe le microbit à ton binôme pour qu'il essaye de battre ton score.
 Clique sur ``|Next|``.



