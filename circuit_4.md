# Circuits électriques - Tutoriel 4

## @showdialog

Programme le micro:bit pour qu'une lumière LED s'allume lorsque l'intensité lumineuse de la pièce est base.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.


## Étape 2
 
Crée une ``|| variables: variable  ||`` et donne lui le nom ``|| variables: LED  ||``. 

Ajoute le bloc ``|| variables: définir LED à 0 ||`` sous le bloc ``|| basic: toujours  ||``.

```blocks

let LED = 0
basic.forever(function () {
    LED = 0
})

```

## Étape 3
 
Remplace la valeur ``|| variables: 0 ||`` du bloc ``|| variables: définir LED  ||`` par le bloc ``|| input: niveau d'intensité luminosité  ||``.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
})

``` 

## Étape 4 

Ajoute le bloc ``|| logic: si vrai alors sinon  ||`` dans le bloc ``|| variables:défimir LED ||``. 
 

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (true) {
    	
    } else {
    	
    }
})

``` 

## Étape 5 

Remplace la valeur ``|| logic:vrai||`` par le bloc ``|| logic:0 < 0||`` dans le bloc ``|| logic: si vrai alors sinon||``. 
 
Regarde l'indice au besoin.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 6 
 
Modifie la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic:0 < 0||`` par le bloc ``|| variables: LED ||``. 
 
Modifie la valeur ``|| logic: 0 ||`` de droite du bloc ``|| logic:0 < 0||`` par la valeur ``|| logic: 40 ||``.

Il est possible que la valeur 40 soit trop petite ou trop grande.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (LED < 40) {
    	
    } else {
    	
    }
})

``` 

## Étape 7 
 
Ajoute le bloc ``|| pins: écrire sur la broche   ||`` sous la condition ``|| logic: si alors ||``. 

La valeur ``|| pins: P0 ||`` demeure la même.

Remplace la broche ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice au besoin.
 
```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (LED < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
    	
    }
})

``` 

## Étape 8 
 
Ajoute le bloc ``|| pins: écrire sur la broche P0  ||`` sous la condition ``|| logic: sinon ||``. 

La broche ``|| pins: P0 ||`` demeure la même.

La valeur ``|| pins: 0 ||`` demeure la même.

Regarde l'indice au besoin.
 
```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (LED < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## @showdialog 

Réalise le branchement ci-dessous.

La couleur des fils n'a pas d'importance!

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/1.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un éclairage de sécurité.

Pour tester la séquence de programmation, télécharge le programme dans le micro:bit.


