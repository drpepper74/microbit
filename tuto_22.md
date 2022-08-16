# Niveau 5

# Tutoriel 22

## @showdialog

Crée un circuit électrique et numérique à l'aide du capteur d'intensité lumineuse et d'une lumière LED.

## Étape 1 

Supprime le bloc ``|| basic:au démarrage ||``. 

## Étape 2 

Ajoute le bloc ``|| logic: si vrai alors sinon  ||`` dans le bloc ``|| basic:toujours ||``. 
 

```blocks 

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

``` 

## Étape 3 

Remplace la valeur ``|| logic:vrai||`` par le bloc ``|| logic:"0 < 0"||`` dans le bloc ``|| logic: si vrai alors sinon||``. 
 
Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (0 < 0) {
    	
    } else {
    	
    }
})
```

## Étape 4 
 
Modifie la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic:"0 < 0"||`` par le bloc ``|| input: niveau d'intensité lumineuse  ||``. 
 
Modifie la valeur ``|| logic: 0 ||`` de droite du bloc ``|| logic:"0 < 0"||`` par la valeur ``|| logic: 40 ||``.

Il est possible que la valeur 40 soit trop petite ou trop grande.

```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
    	
    } else {
    	
    }
})

``` 

## Étape 5 
 
Ajoute le bloc ``|| pins: écrire sur la broche P0  ||`` sous la condition ``|| logic: si alors ||``. 
 
La valeur ``|| pins: 1  ||`` permet au courant de passer dans le circuit.

Regarde l'indice pour connaître les valeurs à changer.
 
```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
    	
    }
})

``` 

## Étape 6 
 
Ajoute le bloc ``|| pins: écrire sur la broche P0  ||`` sous la condition ``|| logic: sinon ||``. 

La valeur ``|| pins: 0  ||`` empêche le courant de passer dans le circuit.

Regarde l'indice pour connaître les valeurs à changer.

 
```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## Étape 7 
 
Crée une ``|| variables: variable  ||`` et donne lui le nom ``|| variables: LED  ||``. 

Ajoute le bloc ``|| variables: définir LED à "0" ||`` sous le bloc ``|| basic: toujours  ||``.

```blocks

let LED = 0
basic.forever(function () {
    LED = 0
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 8
 
Remplace la valeur ``|| variables: 0 ||`` du bloc ``|| variables: définir "LED" à "0"  ||`` par le bloc ``|| input: niveau d'intensité luminosité  ||``.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## Étape 9
 
Ajoute le bloc ``|| basic: montrer nombre  ||`` sous le bloc ``|| pins: écrire sur la broche P0 la valeur 1 ||``.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.showNumber(0)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## Étape 10
 
Ajoute le bloc ``|| variables: LED ||`` dans le bloc ``|| basic: montrer nombre ||``.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.showNumber(LED)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## Étape 11
 
Ajoute le bloc ``|| basic: pause (ms) 500)  ||`` sous le bloc ``|| basic: montrer nombre  ||``.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.showNumber(LED)
        basic.pause(500)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un éclairage de sécurité.

Pour tester la séquence de programmation, télécharge le programme dans le micro:bit.

