# Circuits électriques - Tutoriel 5

## @showdialog

Programme le micro:bit et le circuit électrique.

## Étape 1

Supprime le bloc ``||basic: au démarrage||``.

```blocks

basic.forever(function () {
	
})

```

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Température||``.

Ajoute le bloc ``||variables: définir Température||`` dans le bloc ``||basic: toujours||``.

```blocks

let Température = 0
basic.forever(function () {
    Température = 0
})


```

## Étape 3

Remplace la valeur  ``||variables: 0||`` du bloc ``||variables: définir Température||`` par le bloc ``||input: température||``.

```blocks

let Température = 0
basic.forever(function () {
    Température = input.temperature()
})

```

## Étape 4

Ajoute le bloc  ``||logic: si vrai alors sinon||`` dans le bloc ``||basic: toujours||``.

```blocks

let Température = 0
basic.forever(function () {
    Température = input.temperature()
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 5

Modifie le bloc ``||logic: si vrai alors sinon||``.

Remplace la valeur ``||logic: vrai||`` par le bloc ``||logic: 0 > 0||``.

```blocks

let Température = 0
basic.forever(function () {
    Température = input.temperature()
    if (0 > 0) {
    	
    } else {
    	
    }
})

```

## Étape 6

Modifie le bloc ``||logic: 0 > 0||``.

Remplace la valeur ``||logic: 0||`` de gauche par le bloc ``||variables: Température||``.

Remplace la valeur ``||logic: 0||`` de droite par la valeur ``||logic: 25||``.

```blocks

let Température = 0
basic.forever(function () {
    Température = input.temperature()
    if (Température > 25) {
    	
    } else {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``|| pins: écrire sur la broche   ||`` sous la condition ``|| logic: si alors ||``. 

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice au besoin.

```blocks

let Température = 0
basic.forever(function () {
    Température = input.temperature()
    if (Température > 25) {
        pins.digitalWritePin(DigitalPin.P1, 1)
    } else {
    	
    }
})

```

## Étape 8

Ajoute le bloc ``|| pins: écrire sur la broche   ||`` sous la condition ``|| logic: sinon ||``. 

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.

Regarde l'indice au besoin.

```blocks

let Température = 0
basic.forever(function () {
    Température = input.temperature()
    if (Température > 25) {
        pins.digitalWritePin(DigitalPin.P1, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P1, 0)
    }
})

```

## Étape 9

Ajoute le bloc ``|| input: lorsque le bouton A est pressé   ||``. 

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| input: lorsque le bouton A est pressé   ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    basic.showNumber(0)
})

```

## Étape 10

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


