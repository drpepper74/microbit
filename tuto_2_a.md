# Niveau 1 - Bonus !

## @showdialog
Voici un projet à réaliser en équipe de 2, 3 ou 4 élèves!

![Atelier](https://pxt.azureedge.net/blob/d8cf0f404e04aa67a9f8ed773b2386aa202776de/static/mb/projects/a9-radio.png)

Envoie un message secret aux membres de ton équipe !

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| radio: radio définir groupe ||`` dans le bloc ``||basic: au démarrage||``.

Remplace la valeur ``|| radio: 0 ||`` par un nombre de 1 à 10.

Chaque membre de l'équipe doit utiliser le même nombre. Il s'agit du # de l'équipe.

```blocks

radio.setGroup(1)

```

## Étape 3

Ajoute le bloc ``|| radio: envoyer la chaine par radio ||`` dans le bloc ``|| input: lorsque le bouton A+B est pressé ||``.

Modifie le message affiché dans le bloc ``|| radio: envoyer la chaine par radio ||``.

Il s'agit du message secret que tu enverras.

```blocks

input.onButtonPressed(Button.AB, function () {
    radio.sendString("Salut!")
})
radio.setGroup(1)

```

## Étape 4

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``|| radio: quand une donnée est reçue par radio ||``.

Regarde attentivement l'indice!

```blocks

input.onButtonPressed(Button.AB, function () {
    radio.sendString("Salut!")
})
radio.onReceivedString(function (receivedString) {
    basic.showString("Hello!")
})
radio.setGroup(1)

```

## Étape 5

Glisse le bloc ``|| variables: receivedString ||`` du bloc ``|| radio: quand une donnée est reçue par radio ||`` dans le bloc ``|| basic: afficher texte ||``.

Regarde attentivement l'indice!

```blocks

input.onButtonPressed(Button.AB, function () {
    radio.sendString("Salut!")
})
radio.onReceivedString(function (receivedString) {
    basic.showString(receivedString)
})
radio.setGroup(1)

```

## Étape 6

Télécharge le programme dans le micro:bit.

Teste le programme avec les membres de ton équipe!

Demande à un membre de ton équipe d'envoyer un message secret.