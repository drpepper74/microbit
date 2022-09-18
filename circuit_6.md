# Circuits électriques

# Tutoriel 6

## @showdialog

Transforme le micro:bit en interrupteur pour activer et/ou éteindre plusieurs lumières LED.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque le bouton A est pressé ||``.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Chaque lumière LED doit s'allumer lorsque le bouton A est pressé.
Remplace les valeurs pour paramétrer trois broches.
Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
    pins.digitalWritePin(DigitalPin.P1, 1)
    pins.digitalWritePin(DigitalPin.P2, 1)
})

```

## Étape 4

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque le bouton B est pressé ||``.


```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 5

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Chaque lumière LED doit s'allumer lorsque le bouton A est pressé.
Remplace les valeurs pour paramétrer trois broches.
Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P1, 0)
    pins.digitalWritePin(DigitalPin.P2, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec plusieurs lumières LED.

Essaie de brancher l'ensemble des composantes du circuit.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.