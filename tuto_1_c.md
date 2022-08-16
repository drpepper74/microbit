# Niveau 1

# Tutoriel Bonus C

## @showdialog

Crée une animation d'une nuit étoilée.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| led: allumer x y ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    led.plot(0, 0)
})

```

## Étape 3

Remplace les valeurs ``|| led: 0 ||`` et ``|| led: 0 ||`` du bloc ``|| led: allumer x y ||`` par le bloc ``|| math: choisir un nombre aléatoire ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    led.plot(randint(0, 10), randint(0, 10))
})

```

## Étape 4

Remplace les valeurs ``|| math: 10 ||`` et ``|| math: 10 ||`` du bloc ``|| math: choisir un nombre aléatoire ||`` par ``|| math: 4 ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    led.plot(randint(0, 4), randint(0, 4))
})

```

## Étape 5

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| led: allumer x y ||``.

Regarde l'indice.

```blocks
input.onButtonPressed(Button.A, function () {
    led.plot(randint(0, 4), randint(0, 4))
    basic.pause(100)
})
```

## Étape 6

Ajoute le bloc ``|| loops: répéter 4 fois ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Regarde l'indice.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        led.plot(randint(0, 4), randint(0, 4))
        basic.pause(100)
    }
})
```

## Étape 7

Ajoute le bloc ``|| led: éteindre x y ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.B, function () {
    led.unplot(0, 0)
})

```

## Étape 8

Remplace les valeurs ``|| led: 0 ||`` et ``|| led: 0 ||`` du bloc ``|| led: éteindre x y ||`` par le bloc ``|| math: choisir un nombre aléatoire ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.B, function () {
    led.unplot(randint(0, 10), randint(0, 10))
})

```

## Étape 9

Remplace les valeurs ``|| math: 10 ||`` et ``|| math: 10 ||`` du bloc ``|| math: choisir un nombre aléatoire ||`` par ``|| math: 4 ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.B, function () {
    led.unplot(randint(0, 4), randint(0, 4))
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| led: éteindre x y ||``.

Regarde l'indice.

```blocks
input.onButtonPressed(Button.B, function () {
    led.unplot(randint(0, 4), randint(0, 4))
    basic.pause(100)
})
```

## Étape 11

Ajoute le bloc ``|| loops: répéter 4 fois ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Regarde l'indice.

```blocks
input.onButtonPressed(Button.B, function () {
    for (let index = 0; index < 4; index++) {
        led.unplot(randint(0, 4), randint(0, 4))
        basic.pause(100)
    }
})
```

## Étape 12

Ajoute le bloc ``|| basic: effacer l'écran ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    basic.clearScreen()
})

```

## Étape 13

Télécharge et teste la programmation.