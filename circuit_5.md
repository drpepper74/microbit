# Circuits électriques - Tutoriel 5

## @showdialog

Transforme le micro:bit en système de sécurité.

## Étape 1 

Supprime le bloc  ``|| basic:au démarrage ||``. 

## Étape 2 

Ajoute le bloc ``|| logic: si vrai alors sinon ||`` dans le bloc ``||basic:toujours||``.


```blocks 

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 3 

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si alors sinon ||`` par le bloc ``|| logic: ou ||``. 


```blocks 

basic.forever(function () {
    if (false || false) {
    	
    } else {
    	
    }
})

```

## Étape 4 

Ajoute les blocs ``|| logic: 0 > 0 ||`` et ``|| logic: 0 <  0 ||`` dans le bloc ``|| logic: ou ||``.


```blocks 

basic.forever(function () {
    if (0 > 0 || 0 < 0) {
    	
    } else {
    	
    }
})

```


## Étape 5 

Remplace la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic: 0 > 0 ||`` par le bloc ``|| input: accélération (mg) x||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche du bloc ``|| logic: 0 < 0 ||`` par le bloc ``|| input: accélération (mg) x||``.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 0 || input.acceleration(Dimension.X) < 0) {
    	
    } else {
    	
    }
})

```

## Étape 6 

Remplace la valeur ``|| logic: 0 ||`` de gauche par la valeur ``|| logic: 500 ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: -500 ||``.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
    	
    } else {
    	
    }
})

```

## Étape 7 

Ajoute le bloc ``|| basic: montrer l'icone ||`` dans le bloc ``|| logic: si alors ||``.

Choisis le grand carré comme image.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        basic.showIcon(IconNames.Square)
    } else {
    	
    }
})

```

## Étape 8 

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:montrer l'icône||``.

Modifie les valeurs du bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
    	
    }
})


```

## Étape 9 

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc  ``|| basic: pause (ms) 100 ||`` par ``|| basic: 200 ||``.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
    } else {
    	
    }
})

```

## Étape 10 

Ajoute le bloc ``|| basic: montrer l'icone ||`` sous le bloc ``|| basic: pause (ms) 200 ||``.

Choisis le petit carré comme image.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
        basic.showIcon(IconNames.SmallSquare)
    } else {
    	
    }
})

```

## Étape 11 

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:montrer l'icône||``.

Les valeurs ``|| pins: P0 ||`` et ``|| pins: 0 ||`` demeurent les inchangées.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
        basic.showIcon(IconNames.SmallSquare)
        pins.digitalWritePin(DigitalPin.P0, 0)
    } else {
    	
    }
})
```

## Étape 12 

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc  ``|| basic: pause (ms) 100 ||`` par ``|| basic: 200 ||``.

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

## Étape 13

Ajoute le bloc ``|| loops: répéter 4 fois ||`` dans le bloc ``|| logic: si alors ||``.

Ajouter les autres blocs dans la boucle.

Regarde l'indice au besoin.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        for (let index = 0; index < 4; index++) {
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

## Étape 14 

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| logic: sinon ||``.

La valeur ``|| pins: 0 ||`` demeure la même.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < 500) {
        for (let index = 0; index < 4; index++) {
            basic.showIcon(IconNames.Square)
            pins.digitalWritePin(DigitalPin.P0, 1)
            basic.pause(200)
            basic.showIcon(IconNames.SmallSquare)
            pins.digitalWritePin(DigitalPin.P0, 0)
            basic.pause(200)
        }
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
            }
})


```

## Étape 15 

Ajoute le bloc ``|| basic: effacer l'écran ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

```blocks

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 500 || input.acceleration(Dimension.X) < -500) {
        for (let index = 0; index < 4; index++) {
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

Réalise le branchement ci-dessous.

La couleur des fils n'a pas d'importance!

![MicroSeb](https://github.com/sbergeroncp/micro-seb/blob/master/2.png?raw=true)

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec une lumière LED.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.


