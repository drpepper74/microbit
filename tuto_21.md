# Serrure numérique

# Tutoriel 21

## @showdialog

Transforme le micro:bit en serrure numérique.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:motdepasse||``.

Ajoute le bloc ``||variables: définir motdepasse ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let motdepasse = 0

```

## Étape 3

Remplace la valeur ``||variables:0||`` du bloc ``||variables:définir motdepasse||`` par le bloc ``||text:"   "||``.

Regarde dans l'onglet ``||text:Texte||``.


```blocks

let motdepasse = ""

```

## Étape 4

Crée un mot de passe dans le bloc ``||text:"   "||``. 

Voici le mot de passe ``||variables:ABBAB||``

```blocks

let motdepasse = "ABBAB"

```

## Étape 5

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:mdp||``.

Ajoute le bloc ``||variables: définir mdp ||`` sous le bloc ``||variables:définir motdepasse||``.

```blocks

let motdepasse = "ABBAB"
let mdp = 0

```

## Étape 6

Remplace la valeur ``||variables:0||`` du bloc ``||variables:définir mdp||`` par le bloc ``||text:"   "||``.

Regarde dans l'onglet ``||text:Texte||``.

```blocks

let motdepasse = "ABBAB"
let mdp = ""

```

## Étape 7

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||variables: définir mdp ||``.

Remplace la valeur et ``||pins: P0 ||`` par ``||pins: P1 ||``.

Remplace la valeur et ``||pins: 180 ||`` par ``||pins: 0 ||``.

```blocks

let motdepasse = "ABBAB"
let mdp = ""
pins.servoWritePin(AnalogPin.P1, 0)

```

## Étape 8

Ajoute le bloc ``||variables:définir mdp||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

```blocks

let mdp = 0
input.onButtonPressed(Button.A, function () {
    mdp = 0
})

```

## Étape 9

Remplace la valeur ``||variables:0||`` du bloc ``||variables:définir mdp||`` par le bloc ``||text:concaténation||``.

```blocks

let mdp = ""
input.onButtonPressed(Button.A, function () {
    mdp = "Bonjour" + "Monde"
})

```

## Étape 10

Modifie les valeurs du bloc ``||text:concaténation||``.

Remplace la valeur ``||text:Bonjour||`` par le bloc ``||variables:mdp||``.

Remplace la valeur ``||text:Monde||`` par la lettre ``||text:A||``.

```blocks

let mdp = ""
input.onButtonPressed(Button.A, function () {
    mdp = "" + mdp + "A"
})

```


## Étape 11

Ajoute le bloc ``||variables:définir mdp||`` dans le bloc ``||input:lorsque le bouton B est pressé||``.


```blocks

let mdp = 0
input.onButtonPressed(Button.B, function () {
    mdp = 0
})

```

## Étape 12

Remplace la valeur ``||variables:0||`` du bloc ``||variables:définir mdp||`` par le bloc ``||text:concaténation||``.

```blocks

let mdp = ""
input.onButtonPressed(Button.B, function () {
    mdp = "Bonjour" + "Monde"
})

```

## Étape 13

Modifie les valeurs du bloc ``||text:concaténation||``.

Remplace la valeur ``||text:Bonjour||`` par le bloc ``||variables:mdp||``.

Remplace la valeur ``||text:Monde||`` par la lettre ``||text:B||``.

```blocks

let mdp = ""
input.onButtonPressed(Button.B, function () {
    mdp = "" + mdp + "B"
})

```

## Étape 14

Ajoute le bloc ``||logic:si vrai alors sinon||`` dans le bloc ``||input:lorsque le bouton A+B est pressé||``.


```blocks

input.onButtonPressed(Button.AB, function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 15

Remplace la valeur ``||logic:vrai||`` par le bloc ``||logic:"   " = "   "||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    if ("" == "") {
    	
    } else {
    	
    }
})

```

## Étape 16

Modifie les valeurs du bloc ``||logic:"   " = "   "||``.

Remplace la valeur de gauche par le bloc ``||variables:motdepasse||``.

Remplace la valeur de droite par le bloc ``||variables:mdp||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
    	
    } else {
    	
    }
})

```

## Étape 17

Ajoute le bloc ``||basic:montrer l'icône||`` dans le bloc ``||logic:si||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
        basic.showIcon(IconNames.Yes)
    } else {
    	
    }
})

```

## Étape 18

Ajoute le bloc ``||pins:régler position du servo||`` sous le bloc ``||basic:montrer l'icône||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
        basic.showIcon(IconNames.Yes)
        pins.servoWritePin(AnalogPin.P1, 0)
    } else {
    	
    }
})

```

## Étape 19

Modifie les valeurs du bloc ``||pins:régler position du servo||``.

Remplace la valeur ``||pins:P0||`` par ``||pins:P1||``.

Remplace la valeur ``||pins:0||`` par ``||pins:90||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
        basic.showIcon(IconNames.Yes)
        pins.servoWritePin(AnalogPin.P1, 90)
    } else {
    	
    }
})

```

## Étape 20

Ajoute le bloc ``||basic:montrer l'icône||`` dans le bloc ``||logic:sinon||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
        basic.showIcon(IconNames.Yes)
        pins.servoWritePin(AnalogPin.P1, 90)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 21

Ajoute le bloc ``||basic:pause (ms) 100||`` sous le bloc ``||logic:sinon||``.

Modifie la valeur ``||basic:100||`` du bloc ``||basic:pause||`` par la valeur ``||basic:500||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
        basic.showIcon(IconNames.Yes)
        pins.servoWritePin(AnalogPin.P1, 90)
    } else {
        basic.showIcon(IconNames.No)
    }
    basic.pause(500)
})


```

## Étape 22

Ajoute le bloc ``||basic:effacer l'écran||`` sous le bloc ``||basic:pause (ms) 500||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    let mdp = 0
    let motdepasse = 0
    if (motdepasse == mdp) {
        basic.showIcon(IconNames.Yes)
        pins.servoWritePin(AnalogPin.P1, 90)
    } else {
        basic.showIcon(IconNames.No)
    }
    basic.pause(500)
    basic.clearScreen()
})

```

## @showdialog

Félicitations! Tu as terminé de programmer la serrure.

Pour le tester, télécharge la programmation dans le micro:bit. 
