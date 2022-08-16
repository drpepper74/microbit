# Niveau 5

# Tutoriel 24

## @showdialog

Crée une alarme à l'aide de l'accéléromètre.

## Étape 1 

Supprime le bloc  ``|| basic:toujours ||``. 

## Étape 2 

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:au démarrage||``.

Ajoute le bloc ``|| basic: montrer l'icône ||`` sous le bloc ``|| pins: écrire sur la broche ||``. 
 

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

pins.digitalWritePin(DigitalPin.P0, 0)
basic.showIcon(IconNames.Angry)

```

## Étape 3 

Ajoute le bloc ``|| pins: écrire sur la broche||`` dans le bloc ``||input:lorsque secouer||``.

Ajoute le bloc ``|| basic: pause (ms) 200 ||`` sous le bloc ``|| pins: écrire sur la broche ||``. 
 
Ajoute le bloc ``|| pins: écrire sur la broche||`` sous le bloc ``|| basic: pause (ms) 200 ||``. 

Ajoute le bloc ``|| basic: pause (ms) 200 ||`` sous le bloc ``|| pins: écrire sur la broche ||``. 

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

input.onGesture(Gesture.Shake, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
    basic.pause(200)
    pins.digitalWritePin(DigitalPin.P0, 0)
    basic.pause(200)
})

```

## Étape 4 

Ajoute le bloc ``|| loops: répéter 2 fois ||`` dans le bloc ``||input:lorsque secouer||``.

Ajouter les autres blocs dans la boucle.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
        pins.digitalWritePin(DigitalPin.P0, 0)
        basic.pause(200)
    }
})

```

## @showdialog 

Félicitations! Tu as terminé la programmation de ton  circuit électrique.

Branche maintenant ton circuit.

Vérifie que la lumière LED clignote lorsque le micro:bit est secoué.