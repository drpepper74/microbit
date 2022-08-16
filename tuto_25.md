# Niveau 5

# Tutoriel 25

## @showdialog 

Crée une alarme à l'aide de l'accéléromètre et d'une lumière LED.

## Étape 1 

Supprime le bloc  ``|| basic:au démarrage ||``. 

## Étape 2 

Ajoute le bloc ``|| logic: si vrai alors sinon ||`` sous le bloc ``||basic:toujours||``.

Remplace la valeur "vrai" du bloc ``|| logic: si alors sinon ||`` par le bloc ``|| logic: ou ||``. 

Ajoute les blocs ``|| logic: 0 > 0 ||`` et ``|| logic: 0 <  0 ||`` dans le bloc ``|| logic: ou ||``
 

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (0 > 0 || 0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 3 

Remplace la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic: 0 > 0 ||`` par le bloc ``|| input: accélération (mg) x||``.

Remplace la valeur ``|| logic: 0 ||`` de droite du bloc ``|| logic: 0 < 0 ||`` par le bloc ``|| input: accélération (mg) x||``.

Remplace les valeurs ``|| logic: 0 ||`` par ``|| logic: 500 ||`` et ``|| logic: -500 ||``.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
    	
    } else {
    	
    }
})

```

## Étape 4 

Ajoute le bloc ``|| basic: montrer l'icone ||`` sous le bloc ``|| logic: "si alors" ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:montrer l'icône||``.

Ajoute le bloc ``|| basic: pause (ms) 200 ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Ajoute le bloc ``|| basic: montrer l'icone ||`` sous le bloc ``|| basic: pause (ms) 200 ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:montrer l'icône||``.

Ajoute le bloc ``|| basic: pause (ms) 200 ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
        basic.showIcon(IconNames.SmallSquare)
        pins.digitalWritePin(DigitalPin.P0, 0)
        basic.pause(200)
    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``|| loops: répéter 2 fois ||`` dans le bloc ``|| logic: si alors ||``.

Ajouter les autres blocs dans la boucle.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        for (let index = 0; index < 2; index++) {
            basic.showIcon(IconNames.Square)
            pins.digitalWritePin(DigitalPin.P0, 1)
            basic.pause(200)
            basic.showIcon(IconNames.SmallSquare)
            pins.digitalWritePin(DigitalPin.P0, 0)
            basic.pause(200)
        }
    } else {
    	
    }
})

```

## Étape 6 

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| logic: "sinon" ||``.

Ajoute le bloc ``|| basic: effacer l'écran ||`` sous le bloc ``|| pins: écrire sur la broche ||``.


Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < 500) {
        for (let index = 0; index < 2; index++) {
            basic.showIcon(IconNames.Square)
            pins.digitalWritePin(DigitalPin.P0, 1)
            basic.pause(200)
            basic.showIcon(IconNames.SmallSquare)
            pins.digitalWritePin(DigitalPin.P0, 0)
            basic.pause(200)
        }
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
        basic.clearScreen()
    }
})


```

## @showdialog 

Félicitations! Tu as terminé la programmation de ton  circuit électrique.

Branche maintenant ton circuit.

Vérifie que la lumière LED clignote lorsque le micro:bit est déplacé.