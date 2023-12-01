# Température - Tutoriel 1

## @showdialog

Température et micro:bit !

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``||smarthome:value of soil moisture||`` dans le bloc ``||basic:afficher nombre||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    basic.showNumber(smarthome.ReadSoilHumidity(AnalogPin.P1))
})

```

## @showdialog 

Réalise le branchement ci-dessous.

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/1.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.