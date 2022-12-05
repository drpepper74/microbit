# Circuits électriques et servomoteur

# Tutoriel 7 A

## @showdialog

Transforme le micro:bit en récepteur. 

## Étape 1

Utilise la programmation du Tutoriel #6 et ajoute les prochaines étapes.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(500)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(500)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(500)
    basic.showIcon(IconNames.Yes)
    pins.digitalWritePin(DigitalPin.P12, 0)
})

```

## Étape 2

Ajoute le bloc ``||logic:si vrai alors||`` dans le bloc ``||radio:quand une donnée est reçue par radio receivedString||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (true) {
    	
    }
})

```

## Étape 3

Remplace la valeur ``||logic:vrai||`` du bloc ``||logic:si vrai alors||`` par le bloc ``||logic:"" = ""||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if ("" == "") {
    	
    }
})

```

## Étape 4

Modifie le bloc ``||logic:"" = ""||``.

Remplace ``||logic:""||`` de gauche par le bloc ``||pins:receivedString||``. 

Pour y arriver, fais glisser le bloc ``||pins:receivedString||`` du bloc ``||radio:quand une donnée est reçue par radio receivedString||`` dans le bloc ``||logic:""||`` de gauche.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "") {
    	
    }
})

```

## Étape 5

Modifie le bloc ``||logic:"" = ""||``. (suite)

Remplace ``||logic:""||`` de droite par le mot Ouvrir. 

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
})

```

## Étape 6

Ajoute le bloc ``||logic:si vrai alors||`` sous le bloc ``||logic:si vrai alors||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if (true) {
    	
    }
})

```

## Étape 7

Remplace la valeur ``||logic:vrai||`` du bloc ``||logic:si vrai alors||`` par le bloc ``||logic:"" = ""||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if ("" == "") {
    	
    }
})

```

## Étape 8

Modifie le bloc ``||logic:"" = ""||``.

Remplace le bloc ``||logic:""||`` de gauche par le bloc ``||pins:receivedString||``. 

Pour y arriver, fais glisser le bloc ``||pins:receivedString||`` du bloc ``||radio:quand une donnée est reçue par radio receivedString||`` dans le bloc ``||logic:""||`` de gauche.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if (receivedString == "") {
    	
    }
})

```

## Étape 9

Modifie le bloc ``||logic:"" = ""||``. (suite)

Remplace le bloc ``||logic:""||`` de droite par le mot Fermer. 

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if (receivedString == "Fermer") {
    	
    }
})

```

## Étape 10

Glisse la programmation sous le bloc ``||input: lorsque le bouton A est pressé||`` dans le bloc ``||logic:si Ouvrir alors||``.

Supprime le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
        pins.servoWritePin(AnalogPin.P2, 90)
        pins.digitalWritePin(DigitalPin.P14, 1)
        basic.pause(500)
        basic.showIcon(IconNames.No)
        pins.digitalWritePin(DigitalPin.P14, 0)
        basic.pause(100)
        pins.digitalWritePin(DigitalPin.P13, 1)
        basic.pause(500)
        basic.showLeds(`
            . . . . .
            . # . # .
            . . # . .
            . # . # .
            . . . . .
            `)
        pins.digitalWritePin(DigitalPin.P13, 0)
        basic.pause(100)
        pins.digitalWritePin(DigitalPin.P12, 1)
        basic.pause(500)
        basic.showIcon(IconNames.Yes)
        pins.digitalWritePin(DigitalPin.P12, 0)
    }
    if (receivedString == "Fermer") {
    	
    }
})

```

## Étape 11

Glisse la programmation sous le bloc ``||input: lorsque le bouton B est pressé||`` dans le bloc ``||logic:si Fermer alors||``.

Supprime le bloc ``||input: lorsque le bouton B est pressé||``.

## @showdialog 

Félicitations! Tu as terminé de programmer le récepteur.

Pour tester, télécharge la programmation dans le micro:bit.

Assure-toi que l'émetteur est bien branché et programmé.