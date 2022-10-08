# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 1

## @showdialog

Programme le micro:bit pour afficher sur celui-ci le taux d'humidité de la terre.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``||basic:afficher nombre||`` dans le bloc ``||basic:au démarrage||``.

```blocks
basic.forever(function () {
    basic.showNumber(0)
})

```

## Étape 3

Ajoute le bloc ``||smarthome:value of soil moisture||`` dans le bloc ``||basic:afficher nombre||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

basic.forever(function () {
    basic.showNumber(smarthome.ReadSoilHumidity(AnalogPin.P1))
})

```
