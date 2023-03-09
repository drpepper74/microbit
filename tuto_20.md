# Générateur de mot de passe

# Tutoriel 20

## @showdialog

Transforme le micro:bit en générateur de mot de passe.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| variables: définir liste||`` dans le bloc ``|| basic: au démarrage||``.

Regarde dans l'onglet ``|| arrays: Tableaux||``.

Regarde l'indice au besoin.

```blocks

let liste = [0, 1]

```

## Étape 3

Renomme le bloc ``|| variables: définir liste||`` par ``|| variables: motdepasse||``.

Clique sur la petite flèche du bloc ``|| variables: définir liste||`` pour le renommer.

Regarde l'indice au besoin.

```blocks

let motdepasse = [0, 1]

```

## Étape 4

Remplace le bloc ``|| arrays: tableau de 0 1||`` par le bloc ``|| arrays: tableau vide||``.

Regarde dans l'onglet ``|| arrays: Tableaux||``.

Regarde l'indice au besoin.

```blocks

let motdepasse: number[] = []


```

## Étape 5

Ajoute le bloc ``|| variables: définir liste_de_textes ||`` sous le bloc ``||variables: définit motdepasse||``.

Regarde dans l'onglet ``|| arrays: Tableaux||``.

Regarde l'indice au besoin.


```blocks

let motdepasse: number[] = []
let liste_de_textes = ["a", "b", "c"]

```

## Étape 6

Modifie les valeurs du ``|| arrays: Tableau||``.

Ajoute les valeurs ``|| arrays: 1,2 et 3||`` au  tableau.

Regarde l'indice au besoin.

```blocks

let motdepasse: number[] = []
let liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]

```

## Étape 7

Ajoute le bloc ``|| arrays: ajoute la valeur à la fin||`` dans  le bloc ``|| input: lorsque le bouton A est pressé||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    let list: number[] = []
    list.push(0)
})
let liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
let motdepasse: number[] = []

```

## Étape 8

Remplace le bloc ``|| variables: liste||`` du bloc ``|| arrays: ajoute la valeur à la fin||`` par ``|| variables: motdepasse||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(0)
})
let motdepasse: number[] = []
let liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 9

Remplace la valeur  ``|| arrays: 0||`` du bloc ``|| arrays: ajoute la valeur||`` par le bloc ``|| arrays: reçoit la valeur||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    let liste: number[] = []
    motdepasse.push(liste[0])
})
let motdepasse: number[] = []
let liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 10

Remplace la valeur  ``|| variables: liste||`` par ``|| variables: liste de textes||`` dans le bloc ``|| arrays: ajouter la valeur||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[0])
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 11

Remplace la valeur  ``|| arrays: 0||`` du bloc ``|| arrays: reçoit la valeur||`` par le bloc ``|| math: choisir au hasard||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[randint(0, 10)])
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 12

Remplace le valeur  ``|| math: 10||`` du bloc ``|| math: choisir au hasard||`` par la valeur ``|| math: 5||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[randint(0, 5)])
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 13

Ajoute le bloc ``|| loops: pour l'élément||`` dans  le bloc ``|| input: lorsque le bouton B est pressé||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[randint(0, 5)])
})
input.onButtonPressed(Button.B, function () {
    let list: number[] = []
    for (let valeur of list) {
    	
    }
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 14

Remplace la valeur ``|| variables: list||`` du bloc ``|| loops: pour l'élément||`` par la valeur ``|| variables: motdepasse||``.

Clique sur la flèche du bloc ``|| variables: list||`` pour modifier la valeur.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[randint(0, 5)])
})
input.onButtonPressed(Button.B, function () {
    for (let valeur of motdepasse) {
    	
    }
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## Étape 15

Ajoute le bloc ``|| basic: afficher texte||`` dans le bloc ``|| loops: pour l'élément||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[randint(0, 5)])
})
input.onButtonPressed(Button.B, function () {
    for (let valeur of motdepasse) {
        basic.showString("Hello!")
    }
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []


```

## Étape 15

Remplace la valeur  ``|| variables: Hello!||`` du bloc ``|| basic: afficher texte ||`` par le bloc ``|| variables: valeur||``.

Regarde dans l'onglet ``|| variables: Variables||``.

Regarde l'indice au besoin.

```blocks

input.onButtonPressed(Button.A, function () {
    motdepasse.push(liste_de_textes[randint(0, 5)])
})
input.onButtonPressed(Button.B, function () {
    for (let valeur of motdepasse) {
        basic.showString("" + (valeur))
    }
})
let motdepasse: string[] = []
let liste_de_textes: string[] = []
liste_de_textes = [
"a",
"b",
"c",
"1",
"2",
"3"
]
motdepasse = []

```

## @showdialog

Félicitations! Tu as terminé de programmer le générateur de mot de passe.

Pour le tester, télécharge la programmation dans le micro:bit. 

Ensuite, appuie sur le bouton A cinq fois pour générer le mot de passe.

Finalement, appuie sur le bouton B pour afficher le mot de passe.