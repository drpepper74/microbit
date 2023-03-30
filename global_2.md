# Global Goals 2

## @showdialog

Transforme le micro:bit en collier anti-braconnage.

À chaque fois que l'animal se déplace, le compteur à son pied se réinitialise.

Après 9 secondes sans activité, il émet un signal d'alarme!

## @showdialog

Programme l'émetteur.

## Étape 1

Ajoute le bloc ``||radio: définir groupe||`` dans le bloc ``||basic:au démarrage||``.

Choisis un numéro de groupe représentatif de l'animal.

Tu peux également  laisser le ``||radio:groupe||`` à ``||radio:1||``.

```blocks

radio.setGroup(1)

```

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Temps||``.

Ajoute le bloc ``||variables: définir Temps ||`` sous le bloc ``||radio: définir groupe||``.

```blocks

radio.setGroup(1)
let Temps = 0

```

## Étape 3

Ajoute le bloc ``||variables: définir Temps ||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

let temps = 0
input.onGesture(Gesture.Shake, function () {
    temps = 0
})

```

## Étape 4

Ajoute le bloc ``||basic: pause (ms) 1000 ||`` (1 seconde) dans le bloc ``||basic: toujours ||``.

```blocks

basic.forever(function () {
    basic.pause(1000)
    })

```

## Étape 5

Ajoute le bloc ``||variables: modifier Temps ||`` sous le bloc ``||basic: pause (ms) 1000 ||``.

```blocks

let Temps = 0
basic.forever(function () {
    basic.pause(1000)
    Temps += 1
})

```

## Étape 6

Ajoute le bloc ``||logic: si alors||`` sous le bloc ``||variables:modifier Temps||``.

Regarde l'indice au besoin.

```blocks

let Temps = 0
basic.forever(function () {
    basic.pause(1000)
    Temps += 1
    if (true) {
    	
    }
})


```

## Étape 7

Remplace la valeur ``||logic: vrai||`` par le bloc ``||logic:0 > 0||``.

```blocks

let Temps = 0
basic.forever(function () {
    basic.pause(1000)
    Temps += 1
    if (0 > 0) {
    	
    }
})

```

## Étape 8

Remplace la valeur ``||logic: 0||`` de gauche par le bloc ``||variables:Temps||``.

Remplace la valeur ``||logic: 0||`` de droite par la valeur ``||logic:9||``.

Regarde l'indice au besoin.

```blocks

let Temps = 0
basic.forever(function () {
    basic.pause(1000)
    Temps += 1
    if (Temps > 9) {
    	
    }
})

```

## Étape 9

Ajoute le bloc ``||radio: envoyer chaîne||`` dans le bloc ``||logic:si alors||``.

Ajoute la valeur ``||radio: "   "||`` par le mot ``||radio:ALERTE||``.

```blocks

let temps = 0
basic.forever(function () {
    basic.pause(1000)
    temps += 1
    if (temps > 9) {
        radio.sendString("ALERTE")
    }
})

```

## @showdialog

Bravo! Tu as terminé de programmer l'émetteur.

Télécharge le programme dans le micro:bit. Teste le programme!

As-tu programmé le récepteur également ?