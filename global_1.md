# Global Goals 1

## @showdialog

Transforme le micro:bit en compteur d'espèces.

Par à la découverte de la faune locale.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:oiseau||``.

Ajoute le bloc ``||variables: définir oiseau ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let oiseau = 0

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:mammifere||``.

Ajoute le bloc ``||variables: définir mammifere ||`` sous le bloc ``||variables:oiseau||``.

```blocks

let oiseau = 0
let mammifere = 0

```

## Étape 4

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:reptile||``.

Ajoute le bloc ``||variables: définir reptile ||`` sous le bloc ``||variables:mammifere||``.

```blocks

let oiseau = 0
let mammifere = 0
let reptile = 0

```
## @showdialog

Maintenant que les variables sont définies, crée des séquences de programmationqui te permettront de compter les espèces lorsque tu appuies sur un bouton.

## Étape 5

Ajoute le bloc ``||variables: modifier oiseau||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

```blocks

let oiseau = 0
input.onButtonPressed(Button.A, function () {
    oiseau += 1
})

```

## Étape 6

Ajoute le bloc ``||basic: montrer nombre||`` sous le bloc ``||variables:modifier oiseau||``.

Remplace la valeur ``||basic: 0||`` par le bloc ``||variables:oiseau||``.

Regarde l'indice au besoin.

```blocks

let oiseau = 0
input.onButtonPressed(Button.A, function () {
    oiseau += 1
    basic.showNumber(oiseau)
})

```

## Étape 7

Ajoute le bloc ``||variables: modifier mammifere||`` dans le bloc ``||input:lorsque le bouton B est pressé||``.

```blocks

let mammifere = 0
input.onButtonPressed(Button.B, function () {
    mammifere += 1
})

```
## Étape 8

Ajoute le bloc ``||basic: montrer nombre||`` sous le bloc ``||variables:modifier mammifere||``.

Remplace la valeur ``||basic: 0||`` par le bloc ``||variables:mammifere||``.

Regarde l'indice au besoin.

```blocks

let mammifere = 0
input.onButtonPressed(Button.B, function () {
    mammifere += 1
    basic.showNumber(mammifere)
})

```

## Étape 9

Ajoute le bloc ``||variables: modifier reptile||`` dans le bloc ``||input:lorsque le bouton A+B est pressé||``.

```blocks

let reptile = 0
input.onButtonPressed(Button.AB, function () {
    reptile += 1
})

```

## Étape 10

Ajoute le bloc ``||basic: montrer nombre||`` sous le bloc ``||variables:modifier reptile||``.

Remplace la valeur ``||basic: 0||`` par le bloc ``||variables:reptile||``.

Regarde l'indice au besoin.

```blocks

let reptile = 0
input.onButtonPressed(Button.AB, function () {
    reptile += 1
    basic.showNumber(reptile)
})

```

## @showdialog

Télécharge le programme dans le micro:bit.

Teste le programme!

Combien as-tu observé d'oiseaux ? de mammifères ? de reptiles ?