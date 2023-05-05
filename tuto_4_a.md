# Niveau 4

# Tutoriel Bonus A

## @showdialog

Affiche la température ambiante sur le micro:bit à l'aide d'un graphique.

## Étape 1

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Graphique||``.

Ajoute le bloc ``||variables: définir Graphique||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Graphique = 0

```

## Étape 2

Ajoute le bloc ``||logic: si alors||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    if (true) {
    	
    }
})

```

## Étape 3

Modifie le bloc ``||logic: si alors||``.

Remplace la valeur ``||logic: vrai||`` par le bloc ``||logic: 0 = 0||``.

```blocks

basic.forever(function () {
    if (0 == 0) {
    	
    }
})

```

## Étape 4

Modifie le bloc ``||logic: 0 = 0||``.

Remplace la valeur ``||logic: 0||`` de gauche par le bloc ``||variables: Graphique||``.

La valeur ``||logic: 0||`` de droite demeure la même.

```blocks

basic.forever(function () {
    let Graphique = 0
    if (Graphique == 0) {
    	
    }
})


```

## Étape 5

Ajoute le bloc ``||led: plot bar graph||`` dans le bloc ``||logic: si alors||``.

```blocks

basic.forever(function () {
    let Graphique = 0
    if (Graphique == 0) {
        led.plotBarGraph(
        0,
        0
        )
    }
})

```

## Étape 6

Modifie le bloc ``||led: plot bar graph||``.

Remplace la valeur ``||led: 0||`` du haut par le bloc ``||input: température||``.

Remplace la valeur ``||led: 0||`` du bas par la valeur ``||led: 50||``.


```blocks

basic.forever(function () {
    let Graphique = 0
    if (Graphique == 0) {
        led.plotBarGraph(
        input.temperature(),
        50
        )
    }
})

```

## Étape 7

Ajoute le bloc ``||variables: définir Graphique ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

Remplace la valeur ``||variables: 0 ||`` par la valeur ``||variables: 1 ||``.

```blocks

let Graphique = 0
input.onButtonPressed(Button.AB, function () {
    Graphique = 1
})

```

## Étape 8

Ajoute le bloc ``||basic: effacer l'écran ||`` sous le bloc ``||variables: définir Graphique||``.

```blocks

let Graphique = 0
input.onButtonPressed(Button.AB, function () {
    Graphique = 1
    basic.clearScreen()
})

```

## Étape 9

Ajoute le bloc ``||basic: montrer nombre ||`` sous le bloc ``||basic: effacer l'écran ||``.

Remplace la valeur ``||basic: 0 ||`` par le bloc ``||input: température ||``.

```blocks

let Graphique = 0
input.onButtonPressed(Button.AB, function () {
    Graphique = 1
    basic.clearScreen()
    basic.showNumber(input.temperature())
})

```

## Étape 10

Ajoute le bloc ``||variables: définir Graphique ||`` sous le bloc ``||basic: montrer nombre ||``.

La valeur ``||variables: 0 ||`` demeure la même.

```blocks

let Graphique = 0
input.onButtonPressed(Button.AB, function () {
    Graphique = 1
    basic.clearScreen()
    basic.showNumber(input.temperature())
    Graphique = 0
})

```

## Étape 11

Télécharge le programme dans le micro:bit.

Teste le programme!