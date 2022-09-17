# Circuits électriques

# Tutoriel 1

## @showdialog

Programme le micro:bit pour qu'il allume une lumière LED.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| pins: écrire sur la broche ||`` dans le bloc ``||basic: toujours||``.


```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: 0 ||` par 1.


```blocks

basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})

```

## @showdialog 

Réalise le branchement ci-dessous.

La couleur des fils n'a pas d'importance!

![CSSBF](https://github.com/sbergeroncp/micro-seb/blob/master/1.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé ton premier circuit électrique avec une lumière LED.

Pour tester ton circuit électrique, télécharge la programmation dans le micro:bit.