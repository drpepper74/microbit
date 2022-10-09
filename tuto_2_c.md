# Niveau 2

# Tutoriel Bonus C

## @showdialog

Transforme ton micro:bit en récepteur de signal.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| radio: radio définir groupe ||`` dans le bloc ``||basic: au démarrage||``.

Remplace la valeur ``|| radio: 0 ||`` par un nombre de 1 à 10.


```blocks

radio.setGroup(1)

```

## Étape 3

Ajoute le bloc ``||radio: quand une donnée est reçue par radio||``.

Regarde l'indice. Assure-toi de sélectionner le bon ``||radio: bloc||``.

```blocks

radio.onReceivedString(function (receivedString) {
	
})
radio.setGroup(1)

```

## Étape 4

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:signal||``.

Ajoute le bloc ``||variables: définir signal||`` dans le bloc ``||radio: quand une donnée est reçue par radio||``.

```blocks

radio.onReceivedString(function (receivedString) {
    signal = 0
})
let signal = 0
radio.setGroup(1)

```

## Étape 5

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir signal||`` par le bloc ``||radio: paquet reçu force du signal||``.

```blocks
radio.onReceivedString(function (receivedString) {
    signal = radio.receivedPacket(RadioPacketProperty.SignalStrength)
})
let signal = 0
radio.setGroup(1)

```

## Étape 6

Ajoute le bloc ``||LED: tracer le graphe||`` sous le bloc ``||variables: définir signal||``.

```blocks

radio.onReceivedString(function (receivedString) {
    signal = radio.receivedPacket(RadioPacketProperty.SignalStrength)
    led.plotBarGraph(
    0,
    0
    )
})
let signal = 0
radio.setGroup(1)

```

## Étape 7

Remplace la valeur ``||LED: 0||`` du haut du bloc ``||LED: tracer le graphe||`` par le bloc ``||math: projeter||``.

```blocks

radio.onReceivedString(function (receivedString) {
    signal = radio.receivedPacket(RadioPacketProperty.SignalStrength)
    led.plotBarGraph(
    Math.map(0, 0, 1023, 0, 4),
    0
    )
})
let signal = 0
radio.setGroup(1)

```
## Étape 8

Remplace la valeur ``||LED: 0||`` du bas du bloc ``||LED: tracer le graphe||`` par la valeur ``||LED: 9||``.

```blocks

radio.onReceivedString(function (receivedString) {
    signal = radio.receivedPacket(RadioPacketProperty.SignalStrength)
    led.plotBarGraph(
    Math.map(0, 0, 1023, 0, 4),
    9
    )
})
let signal = 0
radio.setGroup(1)

```

## Étape 9

Remplace la valeur ``||math: 0||`` de gauche du bloc ``||math: projeter||`` par le bloc ``||variables: signal||``.

```blocks

radio.onReceivedString(function (receivedString) {
    signal = radio.receivedPacket(RadioPacketProperty.SignalStrength)
    led.plotBarGraph(
    Math.map(signal, 0, 1023, 0, 4),
    9
    )
})
let signal = 0
radio.setGroup(1)

```


## Étape 10

Remplace les autres ``||math: valeurs||`` du bloc ``||math: projeter||`` par les valeurs ``||math: -95 -42 0 9||``.

```blocks

radio.onReceivedString(function (receivedString) {
    signal = radio.receivedPacket(RadioPacketProperty.SignalStrength)
    led.plotBarGraph(
    Math.map(signal, -95, -42, 0, 9),
    9
    )
})
let signal = 0
radio.setGroup(1)

```

## Étape 11

Télécharge le programme dans le micro:bit.

Un trésor est caché dans la classe. Essaie de le trouver.

Bonne chance!