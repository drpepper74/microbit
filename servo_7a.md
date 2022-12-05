# Circuits électriques et servomoteur

# Tutoriel 7 A

## @showdialog

Transforme le micro:bit en émetteur. 


## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajout le bloc ``||radio:radio définir groupe||`` dans le bloc ``||basic:au démarrage||``.

```blocks

radio.setGroup(1)

```

## Étape 3

Modifie le bloc ``||radio:radio définir groupe||``.

Remplace la valeur ``||radio:1||`` par une valeur entre  ``||radio:1||`` et  ``||radio:255||``.

Le valeur pour l'émetteur et le récepteur doit être la même.

```blocks

radio.setGroup(1)

```

## Étape 4

Ajoute le bloc ``||radio:envoyer la chaîne par radio||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    radio.sendString("")
})


```

## Étape 5

Modifie le bloc ``||radio:envoyer la chaîne par radio||``.

Ajoute le texte ``||radio:Ouvrir||`` dans le bloc ``||radio:envoyer la chaîne par radio||``.

```blocks

input.onButtonPressed(Button.A, function () {
    radio.sendString("Ouvrir")
})


```


## Étape 6

Ajoute le bloc ``||radio:envoyer la chaîne par radio||`` dans le bloc ``||input:lorsque le bouton B est pressé||``.

```blocks

input.onButtonPressed(Button.B, function () {
    radio.sendString("")
})


```

## Étape 7

Modifie le bloc ``||radio:envoyer la chaîne par radio||``.

Ajoute le texte ``||radio:Ouvrir||`` dans le bloc ``||radio:envoyer la chaîne par radio||``.

```blocks

input.onButtonPressed(Button.B, function () {
    radio.sendString("Fermer")
})


```

## @showdialog 

Félicitations! Tu as terminé de programmer l'émetteur.

Pour tester, télécharge la programmation dans le micro:bit.

Assure-toi que le récepteur est bien branché et programmé.