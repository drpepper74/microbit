# Température - Tutoriel 1

## @showdialog

Température et micro:bit !

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``||basic:montrer nombre||`` dans le bloc ``||basic:toujours||``.

```blocks

basic.forever(function () {
    basic.showNumber(0)
})

```

## Étape 3

Ajoute le bloc ``||dstemp2wire:temperature||`` dans le bloc ``||basic:montrer nombre||``.

```package

dstemps=github:bsiever/microbit-dstemp-2wire

```

```blocks

basic.forever(function () {
    basic.showNumber(dstemp.celsius(DigitalPin.P0))
})

```

## @showdialog 

Réalise le branchement ci-dessous.

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/1.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.