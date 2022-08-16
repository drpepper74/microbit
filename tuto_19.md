# Niveau 4

# Tutoriel 19

## @showdialog

Transforme le micro:bit en console de jeux vidéo.

## Étape 1

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Sprite||``. 

Ajoute le bloc ``||variables: définir Sprite||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Sprite = 0

```

## Étape 2

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Sprite||`` par le bloc ``|| game: créer un sprite ||``.

```blocks

let Sprite = game.createSprite(2, 2)

```

## Étape 3

Ajoute le bloc ``||variables: Sprite||`` ``|| game: se déplace de 1 ||`` dans le bloc ``||basic: toujours||``.

```blocks

let Sprite = game.createSprite(2, 2)
basic.forever(function () {
    let sprite: game.LedSprite = null
    sprite.move(1)
})

```

## Étape 4

Ajoute le bloc ``||variables: Sprite||`` ``|| game: si au bord, rebondir ||`` sous le bloc ``||variables: Sprite||`` ``|| game: se déplace de 1 ||``.

```blocks

let sprite = game.createSprite(2, 2)
basic.forever(function () {
    sprite.move(1)
    sprite.ifOnEdgeBounce()
})

```

## Étape 5

Ajoute le bloc ``||basic: pause (ms) 100||`` sous le bloc ``||variables: Sprite||`` ``|| game: si au bord, rebondir ||``.

```blocks

let sprite = game.createSprite(2, 2)
basic.forever(function () {
    sprite.move(1)
    sprite.ifOnEdgeBounce()
    basic.pause(100)
})

```

## Étape 6

Ajoute le bloc ``||logic: si vrai alors sinon||`` dans le bloc ``|| input: lorsque le bouton A est pressé ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    if (true) {
    	
    } else {
    	
    }

```

## Étape 7

Remplace la valeur ``||logic: vrai||`` par le bloc ``||logic: 0 = 0||``.

```blocks

input.onButtonPressed(Button.A, function () {
    if (0 == 0) {
    	
    } else {
    	
    }
})

```

## Étape 8

Remplace la valeur ``||logic: 0||`` de gauche dans le bloc ``||logic: 0 = 0||`` par le bloc par le bloc ``||variables: Sprite||`` ``|| game: x ||``.

Remplace la valeur ``||logic: 0||`` de droite  dans le bloc ``||logic: 0 = 0||`` par la valeur ``||logic: 2||``.

```blocks

input.onButtonPressed(Button.A, function () {
    if (sprite.get(LedSpriteProperty.X) == 2) {
    	
    } else {
    	
    }
})
let sprite: game.LedSprite = null
sprite = game.createSprite(2, 2)
basic.forever(function () {
    sprite.move(1)
    sprite.ifOnEdgeBounce()
    basic.pause(100)
})

```

## Étape 9 

Ajoute le bloc ``|| game: incrémenter le score de 1 ||`` dans le bloc ``||logic: si vrai alors sinon||`` sous ``||logic: si vrai alors ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    if (sprite.get(LedSpriteProperty.X) == 2) {
        game.addScore(1)
    } else {
    	
    }
})
let sprite: game.LedSprite = null
sprite = game.createSprite(2, 2)
basic.forever(function () {
    sprite.move(1)
    sprite.ifOnEdgeBounce()
    basic.pause(100)
})

```

## Étape 10

Ajoute le bloc ``|| game: fin du jeu ||`` sous ``||logic: sinon||``.

```blocks

input.onButtonPressed(Button.A, function () {
    if (sprite.get(LedSpriteProperty.X) == 2) {
        game.addScore(1)
    } else {
        game.gameOver()
    }
})
let sprite: game.LedSprite = null
sprite = game.createSprite(2, 2)
basic.forever(function () {
    sprite.move(1)
    sprite.ifOnEdgeBounce()
    basic.pause(100)
})

```

## Étape 11

Télécharge le programme dans le micro:bit.

Teste le programme!

Appuie sur le bouton A lorsque le pixel est au centre de l'écran! Bonne chance.