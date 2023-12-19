# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 1

## @showdialog

Programme le micro:bit pour que la lumière s'allume au contrôle du son et de la luminosité.

## @showdialog

Ajoute l'extension ``||loops:smarthome||``.

Appuie sur le bouton Extensions et recherche ``||loops:smarthome||``.

## Étape 1

Ajoute le bloc ``||LED:activer LED||`` dans le bloc ``||basic:au démarrage||``.

La valeur ``||logic:faux||`` du bloc ``||LED:activer LED||`` demeure inchangée.

```blocks

led.enable(false)
basic.forever(function () {
	
})

```

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:lumière||``.

Ajoute le bloc ``||variables: définir lumière ||`` dans le bloc ``||basic: toujours||``. 

```blocks

let lumière = 0
basic.forever(function () {
    lumière = 0
})

```

## Étape 3

Ajoute le bloc ``||smarthome:value of light intensity||`` (trad: valeur de l'intensité lumineuse) dans le bloc ``||variables: définir lumière ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let lumière = 0
basic.forever(function () {
    lumière = smarthome.ReadLightIntensity(AnalogPin.P1)
})

```

## Étape 4