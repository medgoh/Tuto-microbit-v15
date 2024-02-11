# Réalise un détecteur sonore avec Taill'Créons


## Bonjour, Taill'Crons va t'apprendre à faire battre le coeur de ton microbit en rythme
Suis bien les instructions à chaques étapes et clique sur ``|Next|``. pour passer
 aux prochaines étapes.  
N'hésite pas à cliquer sur le bouton d'aide  en forme d'ampoule en cas 
de blocage.  
Si vous êtes deux à cet atelier, faites une étapes sur deux à tour de rôle et entraidez-vous!
Clique sur OK pour commencer.

 ![Image description](https://def773hwqc19t.cloudfront.net/img/actor_cover/2786/18daa29583f7776a3032954d83007d40_Taillcr%C3%A9o.jpg)


## Détecte lorsque l'environnement sonore est bruyant
Dans la boite à outils, clique sur la section ``||Input:Entrée||`` et 
déplace le bloc ``||Input:Lorsque que le son bruyant est détecté||`` 
dans un espace libre à droite de l'écran.  
Clique sur ``|Next|``.

``` blocks
input.onSound(DetectedSound.Loud, function () {
  basic.showIcon(IconNames.Heart)
})
```

## Affiche une icone d'un grand coeur lorsque c'est bruyant
Dans la boite à outils, clique sur la section ``||Basic:Base||`` et déplace le bloc
 ``||Basic:montrer l'icône|`` à l'intérieur du bloc ``||Input:Lorsque que le son bruyant est détecté||``.  
 Clique sur ``|Next|``.

``` blocks
input.onSound(DetectedSound.Loud, function () {
    basic.showIcon(IconNames.Heart)
})
```

## Détecte lorsque l'environnement sonore est calme
Dans la boite à outils, clique sur la section ``||Input:Entrée||`` et 
déplace le bloc ``||Input:Lorsque que le son bruyant est détecté||`` 
dans un espace libre à droite de l'écran.  
Clique sur  ``||Input:bruyant||`` et sélectionne  ``||Input:silencieux||``.  
Clique sur ``|Next|``.

``` blocks
input.onSound(DetectedSound.Quiet, function () {
    basic.showIcon(IconNames.SmallHeart)
})
```

## Affiche une icone d'un petit coeur lorsque c'est silencieux
Dans la boite à outils, clique sur la section ``||Basic:Base||`` et déplace le bloc
 ``||Basic:montrer l'icône|`` à l'intérieur du bloc ``||Input:Lorsque que le son silencieux est détecté||``.  
Clique sur l'icône et sélectionne une icône en forme de petit coeur.  
 Clique sur ``|Next|``.

``` blocks
input.onSound(DetectedSound.Quiet, function () {
    basic.showIcon(IconNames.SmallHeart)
})
```




## Essaye dans la vrai vie!
Clique sur ``|Télécharger|`` et patiente le temps que ton programme se transfert vers ton microbit.  
Tape des mains en rythme et regarde le coeur de ton microbit t'accompagner.  
 Clique sur ``|Next|``.

