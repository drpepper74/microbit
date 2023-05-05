# Niveau 1

# Tutoriel 5

## @showdialog

Programme le micro:bit pour qu'il affiche une direction en fonction de l'inclinaison du.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer la flèche ||`` dans le bloc ``||input: lorsque incliner à droite||``.

```blocks

input.onGesture(Gesture.TiltRight, function () {
    basic.showArrow(ArrowNames.North)
})

```

## Étape 3

Modifie le bloc ``|| basic: montrer la flèche ||``.

Remplace la valeur ``|| led: Nord ||`` par la valeur ``|| led: Est ||``.

```blocks

input.onGesture(Gesture.TiltRight, function () {
    basic.showArrow(ArrowNames.East)
})

```

## Étape 4

Ajoute le bloc ``|| basic: montrer la flèche ||`` dans le bloc ``||input: lorsque incliner à gauche||``.

```blocks

input.onGesture(Gesture.TiltLeft, function () {
    basic.showArrow(ArrowNames.North)
})

```

## Étape 5

Modifie le bloc ``|| basic: montrer la flèche ||``.

Remplace la valeur ``|| led: Nord ||`` par la valeur ``|| led: Ouest ||``.

```blocks

input.onGesture(Gesture.TiltLeft, function () {
    basic.showArrow(ArrowNames.West)
})

```

## Étape 6

Ajoute le bloc ``|| basic: montrer la flèche ||`` dans le bloc ``||input: lorsque logo vers le haut||``.

La valeur ``|| led: Nord ||`` demeure la même.

```blocks

input.onGesture(Gesture.LogoUp, function () {
    basic.showArrow(ArrowNames.North)
})

```

## Étape 7

Ajoute le bloc ``|| basic: montrer la flèche ||`` dans le bloc ``||input: lorsque logo vers le bas||``.


```blocks

input.onGesture(Gesture.LogoDown, function () {
    basic.showArrow(ArrowNames.North)
})

```

## Étape 8

Modifie le bloc ``|| basic: montrer la flèche ||``.

Remplace la valeur ``|| led: Nord ||`` par la valeur ``|| led: Sud ||``.

```blocks

input.onGesture(Gesture.LogoDown, function () {
    basic.showArrow(ArrowNames.South)
})

```

## Étape 9

Télécharge le programme dans le micro:bit.

Teste le programme!