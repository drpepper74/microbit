# Circuits électriques - Tutoriel 6

## @showdialog

Programme le défi ultime en utilisant les branchements du tutoriels précédent.

# Étape 1

Le circuit doit clignoter lorsque le bouton A est pressé.
Le circuit doit s'allumer lorsque le bouton B est pressé.
Le circuit doit d'éteindre lorsque le bouton A+B est pressé.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        basic.pause(100)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})
basic.forever(function () {
	
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec plusieurs lumières LED.

Essaie de brancher l'ensemble des composantes du circuit sans indice.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.