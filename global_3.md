# Global Goals 3

## @showdialog

Transforme le micro:bit en collier anti-braconnage.

Chaque fois que l'animal se déplace, le compteur à son pied se réinitialise.

Après 9 secondes sans activité, il émet un signal d'alarme!

## @showdialog

Programme le récepteur.

## Étape 1

Ajoute le bloc ``||radio: définir groupe||`` dans le bloc ``||basic:au démarrage||``.

Choisis un numéro de groupe représentatif de l'animal.

Tu peux également  laisser le ``||radio:groupe||`` à ``||radio:1||``.

```blocks

radio.setGroup(1)

```

## Étape 2

Ajoute le bloc ``||logic: si vrai||`` dans le bloc ``||radio: quand une donnée est reçue par onde radio||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (true) {
    	
    }
})

```

## Étape 3

Remplace le bloc ``||logic: vrai ||`` par le bloc ``||logic: "   " = "   "||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if ("" == "") {
    	
    }
})


```

## Étape 4

Glisse le bloc ``||variables:receivedString||`` dans le bloc ``||logic: 0||`` de gauche. 

Remplace la valeur ``||logic: 0||`` de droite par le texte ``||logic:ALERTE||``.

Regarde l'indice au besoin.

Le mot de l'émetteur et du récepteur doivent correspondre.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "ALERTE") {
    	
    }
})


```

## Étape 5

Ajoute le bloc ``||basic: afficher texte||`` sous le bloc ``||logic:si alors||``.

Modifie le mot ``||basic: Hello!||`` par le mot ``||radio:ALERTE||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "ALERTE") {
        basic.showString("ALERTE")
    }
})


```

## @showdialog

Bravo! Tu as terminé de programmer l'émetteur.

Télécharge le programme dans le micro:bit. Teste le programme!

As-tu programmé le récepteur également ?