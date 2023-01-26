# Circuits électriques et servomoteur avec un bouclier Kitronik

# Tutoriel 1

## @showdialog

Programme le micro:bit pour qu'il active le servomoteur lorsqu'un bouton est pressé.

## Étape 1

Conserve les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

```blocks

basic.forever(function () {
	
})

```

## Étape 2

Ajoute le bloc ``||Kitronik_Robotics_Board:set Servo||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onButtonPressed(Button.A, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 0)
})

```

## Étape 3

Modifie les valeurs du bloc ``||Kitronik_Robotics_Board:set Servo||``.

La valeur ``||Kitronik_Robotics_Board:1||`` du bloc ``||Kitronik_Robotics_Board:set Servo||`` demeure la même.

Remplace la valeur ``||Kitronik_Robotics_Board:0||`` par la valeur ``||Kitronik_Robotics_Board:45||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onButtonPressed(Button.A, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 45)
})
```

## Étape 4

Ajoute le bloc ``||Kitronik_Robotics_Board:set Servo||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onButtonPressed(Button.B, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 0)
})

```

## Étape 5

Modifie les valeurs du bloc ``||Kitronik_Robotics_Board:set Servo||``.

La valeur ``||Kitronik_Robotics_Board:1||`` du bloc ``||Kitronik_Robotics_Board:set Servo||`` demeure la même.

Remplace la valeur ``||Kitronik_Robotics_Board:0||`` par la valeur ``||Kitronik_Robotics_Board:90||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onButtonPressed(Button.B, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 90)
})
```

## Étape 6

Ajoute le bloc ``||Kitronik_Robotics_Board:set Servo||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onButtonPressed(Button.AB, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 0)
})

```

## Étape 7

Modifie les valeurs du bloc ``||Kitronik_Robotics_Board:set Servo||``.

La valeur ``||Kitronik_Robotics_Board:1||`` du bloc ``||Kitronik_Robotics_Board:set Servo||`` demeure la même.

Remplace la valeur ``||Kitronik_Robotics_Board:0||`` par la valeur ``||Kitronik_Robotics_Board:180||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onButtonPressed(Button.AB, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 45)
})
```
## Étape 8

Ajoute le bloc ``||Kitronik_Robotics_Board:set Servo||`` dans le bloc ``||input: lorsque secouer||``.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onGesture(Gesture.Shake, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 0)
})

```

## Étape 9

La valeur ``||Kitronik_Robotics_Board:1||`` du bloc ``||Kitronik_Robotics_Board:set Servo||`` demeure la même.

La valeur ``||Kitronik_Robotics_Board:0||`` du bloc ``||Kitronik_Robotics_Board:set Servo||`` demeure la même.

```package

dstemps=github:kitronikltd/pxt-kitronik-robotics-board

```

```blocks

input.onGesture(Gesture.Shake, function () {
    Kitronik_Robotics_Board.servoWrite(Kitronik_Robotics_Board.Servos.Servo1, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.