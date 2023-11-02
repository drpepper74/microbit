# Circuits électriques - Tutoriel 8

## @showdialog

Programme le micro:bit et le circuit électrique.

## Étape 1

Utilise les blocs de ton choix.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})
input.onGesture(Gesture.Shake, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
})
let LED = randint(0, 10)
basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.showNumber(input.temperature())
    basic.showIcon(IconNames.Heart)
    basic.showString("Hello!")
    basic.clearScreen()
    basic.pause(100)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer le circuit électrique.

Essaie de brancher l'ensemble des composantes du circuit sans indice.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.