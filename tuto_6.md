# Niveau 2

# Tutoriel 6

## @showdialog

Transforme le micro:bit en thermomètre.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Temperature||``.

Ajoute le bloc ``||variables: définir Temperature ||`` dans le bloc ``||basic: toujours||``.

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Temperature ||`` par le bloc ``||input: température||``. 

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
})

```

## Étape 4

Ajoute le bloc ``|| basic: montrer nombre ||`` sous le bloc ``|| variables: définir Temperature ||``.

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
    basic.showNumber(0)
})

```

## Étape 5

Remplace la valeur ``|| basic: 0||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Temperature||``. 

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
    basic.showNumber(Temperature)
})
```

## Étape 6

Ajoute le bloc ``|| basic: pause (ms) 1000 ||`` sous le bloc ``|| basic: montrer nombre ||``.

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
    basic.showNumber(Temperature)
    basic.pause(1000)
})

```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le programme!

Manipule le micro:bit. Que remarques-tu?