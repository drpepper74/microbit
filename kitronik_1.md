# Ensemble - Bouclier d'extension Kitronik 5693

# Tutoriel 1

## @showdialog

Programme le micro:bit pour activer le servomoteur.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

```blocks

basic.forever(function () {
	
})


```

## Étape 2

Ajoute le bloc ``||Kitronik_Robotics_Board:set Servo||`` dans le bloc ``||basic:toujours||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

basic.forever(function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 0)
})

```

## Étape 3

Modifie le bloc ``||Kitronik_Robotics_Board:set Servo||``.

La valeur ``||Kitronik_Robotics_Board:1||`` demeure la même.

Modifie la valeur ``||Kitronik_Robotics_Board:0||`` par 90.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

basic.forever(function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 90)
})

```