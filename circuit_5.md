# Circuits électriques - Tutoriel 5

## @showdialog

Transforme le micro:bit en thermomètre.

## Étape 1

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Température||``.

Ajoute le bloc ``||variables: définir Température||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Température = 0

```

## Étape 2

Remplace la valeur  ``||variables: 0||`` du bloc ``||variables: définir Température||`` par le bloc ``||input: température||``.

```blocks

let Température = input.temperature()

```

## Étape 3

Ajoute le bloc  ``||logic: si vrai alors sinon||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 4

Modifie le bloc ``||logic: si vrai alors sinon||``.

Remplace la valeur ``||logic: vrai||`` par le bloc ``||logic: 0 > 0||``.

```blocks

basic.forever(function () {
    if (0 > 0) {
    	
    } else {
    	
    }
})

```

## Étape 5

Modifie le bloc ``||logic: 0 > 0||``.

Remplace la valeur ``||logic: 0||`` de gauche par le bloc ``||variables: Température||``.

Remplace la valeur ``||logic: 0||`` de droite par la valeur ``||logic: 22||``.


```blocks

basic.forever(function () {
    let Température = 0
    if (Température > 22) {
    	
    } else {
    	
    }
})

```

## Étape 6

Ajoute le bloc ``|| pins: écrire sur la broche   ||`` sous la condition ``|| logic: si alors ||``. 

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice au besoin.

```blocks

basic.forever(function () {
    let Température = 0
    if (Température > 22) {
        pins.digitalWritePin(DigitalPin.P1, 1)
    } else {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``|| pins: écrire sur la broche   ||`` sous la condition ``|| logic: sinon ||``. 

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.

Regarde l'indice au besoin.

```blocks

basic.forever(function () {
    let Température = 0
    if (Température > 22) {
        pins.digitalWritePin(DigitalPin.P1, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P1, 0)
    }
})

```

## Étape 8

Ajoute le bloc ``|| input: lorsque le bouton A est pressé   ||``. 

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| input: lorsque le bouton A est pressé   ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(0)
})

```

## Étape 9

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``||variables: Température||``.

```blocks

input.onButtonPressed(Button.A, function () {
    let Température = 0
    basic.showNumber(Température)
})

```

## @showdialog 

Réalise le branchement ci-dessous.

La couleur des fils n'a pas d'importance!

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/2.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.


