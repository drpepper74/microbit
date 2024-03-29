# Niveau 2

# Tutoriel 8

## @showdialog

Transforme le micro:bit en jeu de hasard. Vrai ou faux ?

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``||logic: si vrai alors sinon||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 3

Remplace la valeur ``||logic: vrai ||`` dans le bloc ``||logic: si vrai alors sinon||`` par le bloc ``||math: choisir au hasard vrai ou faux||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
    	
    } else {
    	
    }
})

```

## Étape 4

Ajoute le bloc ``||basic: montrer l'icone||`` sous le bloc ``||logic: alors||``.

Choisis le bloc ``||basic: oui||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||basic: montrer l'icone||`` sous le bloc ``||logic: sinon||``.

Choisis le bloc ``||basic: non||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 6

Ajoute le bloc ``||loops: répéter ||`` au-dessus du bloc ``||logic: si alors sinon||``.

Modifie la valeur ``||loops: 4||`` du bloc ``||loops: répéter||`` par la valeur ``||loops: 2||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
    	
    }
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 7

Ajoute trois blocs ``||basic: montrer l'icone||`` dans le bloc ``||loops: répéter deux fois||``.

Choisis les blocs ``||basic: diamant||``, ``||basic: petit diamant||``, et ``||basic: échiquier||``.

Regarde les icones dans l'indice.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
        basic.showIcon(IconNames.Diamond)
        basic.showIcon(IconNames.SmallDiamond)
        basic.showIcon(IconNames.Chessboard)
    }
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})

```

## Étape 8

Télécharge le programme dans le micro:bit et teste le programme !

Dis une affirmation et secoue le micro:bit. Que remarques-tu ?
