# Circuits électriques

# Tutoriel 2

## @showdialog

Transforme le micro:bit en interrupteur pour activer et/ou éteindre une lumière LED.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque le bouton A est pressé ||``.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P1, 1)
})

```

## Étape 4

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``|| input: lorsque le bouton B est pressé ||``.


```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 5

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P1, 0)
})

```

## @showdialog 

Réalise le branchement ci-dessous.

La couleur des fils n'a pas d'importance!

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/2.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.