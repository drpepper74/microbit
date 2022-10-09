# Niveau 2

# Tutoriel Bonus D

## @showdialog

Transforme ton micro:bit en émetteur de signal.

## Étape 1

Ajoute le bloc ``|| radio: radio définir groupe ||`` dans le bloc ``||basic: au démarrage||``.

Remplace la valeur ``|| radio: 0 ||`` par un nombre de 1 à 10.


```blocks

radio.setGroup(1)

```

## Étape 2

Ajoute le bloc ``|| radio: radio définir puissance de transmission ||`` sous le bloc ``|| radio: radio définir groupe ||``.

Remplace la valeur ``|| radio: 0 ||`` par la valeur ``|| radio: 1 ||``.


```blocks

radio.setGroup(1)
radio.setTransmitPower(1)

```

## Étape 3

Ajoute le bloc ``|| radio: envoyer la chaine ||`` dans le bloc ``||basic: toujours||``.

Remplace la ``|| radio: valeur ||`` par la valeur ``|| radio: 1 ||``.


```blocks

radio.setGroup(1)
radio.setTransmitPower(1)
basic.forever(function () {
    radio.sendString("1")
})

```

## Étape 4

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| radio: envoyer la chaine ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||``par la valeur ``|| basic: 200 ||``.


```blocks

radio.setGroup(1)
radio.setTransmitPower(1)
basic.forever(function () {
    radio.sendString("1")
    basic.pause(200)
})

```

## Étape 5

Télécharge le programme dans le micro:bit.

Cache le micro:bit dans la classe.

Les élèves devront le trouver à l'aide du récepteur! 

Bonne chance.