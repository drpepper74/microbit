# Niveau 1

# Tutoriel 5

## @showdialog

Programme le micro:bit pour qu'il affiche l'animation d'un battement de coeur lorsqu'il est secoué.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer l'icône ||`` dans le bloc ``||input: lorsque secouer||``.

Choisis l'icône du grand coeur.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
})

```

## Étape 3

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| basic: montrer l'icône ||``.


```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(100)
})

```

## Étape 4

Ajoute le bloc ``|| basic: montrer l'icône ||`` sous le bloc ``|| basic: pause (ms) 100 ||``.

Choisis l'icône du petit coeur.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(100)
    basic.showIcon(IconNames.SmallHeart)
})

```

## Étape 5

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| basic: montrer l'icône ||``.


```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(100)
    basic.showIcon(IconNames.SmallHeart)
    basic.pause(100)
})

```

## Étape 6

Ajoute le bloc ``|| loops: Répéter  4 fois ||`` dans la séquence de programmation.

Remplace la valeur ``|| loops: 4 ||`` par ``|| loops: 10 ||``

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 10; index++) {
        basic.showIcon(IconNames.Heart)
        basic.pause(100)
        basic.showIcon(IconNames.SmallHeart)
        basic.pause(100)
    }
})

```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le programme!