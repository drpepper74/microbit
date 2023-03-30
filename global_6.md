# Global Goals 7

## @showdialog

Transforme le micro:bit en lumière de vélo.

Lorsque la luminosité extérieure diminue (ex. : coucher de soleil), la lumière du vélo s'allume pour avertir les automobilistes et les piétons.

## @showdialog

Programme la lumière du vélo.

## Étape 1

Ajoute le bloc ``||basic: montrer LEDs||`` dans le bloc ``||basic:toujours||``.

```blocks

basic.forever(function () {
    basic.showLeds(`
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        `)
})

```

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Lumiere||``.

Ajoute le bloc ``||variables: définir Lumiere ||`` dans le bloc ``||basic: toujours||``.

```blocks

let Lumiere = 0
basic.forever(function () {
    basic.showLeds(`
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        `)
    Lumiere = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0 ||`` par le bloc ``||input: niveau d'intensité lumineuse||``.

```blocks

let Lumiere = 0
basic.forever(function () {
    basic.showLeds(`
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        `)
    Lumiere = input.lightLevel()
})

```

## Étape 4

Ajoute le bloc ``||LED:activer LED||`` dans le bloc ``||basic: au démarrage ||``.

Choisis ``||logic:faux||`` comme condition.

```blocks

let Lumiere = 0
led.enable(false)
basic.forever(function () {
    basic.showLeds(`
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        # # # # #
        `)
    Lumiere = input.lightLevel()
})

```

## Étape 5

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:A||``.

Ajoute le bloc ``||variables: définir A ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Remplace la valeur ``||variables: 0 ||`` par la valeur ``||variables: 1 ||``.

```blocks

let A = 0
input.onButtonPressed(Button.A, function () {
    A = 1
})

```

## Étape 6

Ajoute le bloc ``||music: démarrer la mélodie ||`` sous le bloc ``||variables: définir A||``.

Remplace la valeur ``||music: dadadum ||`` par la valeur ``||music: mise sous tension ||``.

```blocks

let A = 0
input.onButtonPressed(Button.A, function () {
    A = 1
    music.startMelody(music.builtInMelody(Melodies.PowerUp), MelodyOptions.Once)
})

```

## Étape 7

Ajoute le bloc ``||variables: définir A ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

La valeur ``||variables: 0 ||`` demeure la même.

```blocks

let A = 0
input.onButtonPressed(Button.B, function () {
    A = 0
})


```

## Étape 8

Ajoute le bloc ``||music: démarrer la mélodie ||`` sous le bloc ``||variables: définir A||``.

Remplace la valeur ``||music: dadadum ||`` par la valeur ``||music: mise hors tension ||``.

```blocks

let A = 0
input.onButtonPressed(Button.B, function () {
    A = 0
    music.startMelody(music.builtInMelody(Melodies.PowerDown), MelodyOptions.Once)
})

```

## Étape 9

Ajoute le bloc ``||logic: si vrai alors ||`` dans un nouveau bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    if (true) {
    	
    }
})

```

## Étape 10

Remplace la valeur ``||logic: vrai ||`` par le bloc ``||logic: 0 = 0||``.

```blocks

basic.forever(function () {
    if (0 == 0) {
    	
    }
})

```

## Étape 11

Modifie le bloc ``||logic: 0 = 0||``.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: A||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 1||``.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
    	
    }
})


```

## Étape 12

Ajoute le bloc ``||logic: si vrai alors ||`` sous le bloc ``||logic: si alors||``.

Regarde l'indice au besoin.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        if (true) {
        	
        }
    }
})

```

## Étape 13

Remplace la valeur ``||logic: vrai ||`` par le bloc ``||logic: 0 < 0||``.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        if (0 < 0) {
        	
        }
    }
})

```

## Étape 14

Modifie le bloc ``||logic: 0 < 0||``.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: Lumiere||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 100||``.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        let Lumiere = 0
        if (Lumiere < 100) {
        	
        }
    }
})

```

## Étape 15

Ajoute le bloc ``||loops: tant que ||`` sous le bloc ``||logic: si alors||``.

Regarde l'indice au besoin.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        let Lumiere = 0
        if (Lumiere < 100) {
            while (false) {
            	
            }
        }
    }
})

```

## Étape 16

Remplace la valeur ``||loops: faux ||`` par le bloc ``||logic: 0 = 0||``.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        let Lumiere = 0
        if (Lumiere < 100) {
            while (0 == 0) {
            	
            }
        }
    }
})

```

## Étape 17

Modifie le bloc ``||logic: 0 = 0||``.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: A||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 1||``.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        let Lumiere = 0
        if (Lumiere < 100) {
            while (A == 1) {
            	
            }
        }
    }
})


```

## Étape 18

Ajoute les blocs ``||basic: pause (ms) 1000 ||`` (une seconde) et ``||led: activer LED||`` dans le bloc ``||loops: tant que||``.

Regarde l'indice au besoin.

Assure-toi que la valeur ``||logic: vrai ||`` du bloc ``||led: activer LED ||`` soit sélectionnée.

```blocks

basic.forever(function () {
    let A = 0
    if (A == 1) {
        let Lumiere = 0
        if (Lumiere < 100) {
            while (A == 1) {
                basic.pause(1000)
                led.enable(true)
            }
        }
    }
})


```

## Étape 19

Ajoute les blocs ``||basic: pause (ms) 1000 ||`` (une seconde) et ``||led: activer LED||`` dans le bloc ``||loops: tant que||``.

Regarde l'indice au besoin.

Assure-toi que la valeur ``||logic: faux ||`` du bloc ``||led: activer LED ||`` soit sélectionnée.

```blocks

basic.forever(function () {
    let A = ""
    if (A == "1") {
        let Lumiere = 0
        if (Lumiere < 100) {
            while (A == "1") {
                basic.pause(1000)
                led.enable(true)
                basic.pause(1000)
                led.enable(false)
            }
        }
    }
})


```

## @showdialog

Bravo! Tu as terminé de programmer la lumière du vélo.

Télécharge le programme dans le micro:bit. Teste le programme!

Sois prudent sur la route!
