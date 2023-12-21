# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 1

## @showdialog

Utilise les capteurs, le bouclier d'extension et les câbles.

## Étape 1

Ajoute le bloc ``||LED:activer LED||`` dans le bloc ``||basic:au démarrage||``.

La valeur ``||logic:faux||`` du bloc ``||LED:activer LED||`` demeure inchangée.

```blocks

led.enable(false)
basic.forever(function () {
	
})

```

## Étape 2

Ajoute le bloc ``||OLED: initialize OLED ||`` (trad. : démarrer l'écran) sous le bloc ``||LED:activer LED||``

Les valeurs du bloc ``||OLED: initialize OLED ||`` demeurent les mêmes.

Les valeurs ``||OLED: 128 ||`` et ``||OLED: 64 ||`` sont les dimensions (en pixels) de l'écran.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
	
})

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Temperature||`` (sans accent).

Ajoute le bloc ``||variables: définir Temperature ||`` dans le bloc ``||basic: toujours||``. 

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = 0
})

```

## Étape 4

Modifie le bloc ``||variables: définir Temperature ||``.

Remplace la valeur ``||variables: 0 ||`` du bloc ``||variables: définir Temperature ||`` par le bloc ``||input:température||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
})

```

## Étape 5

Ajoute le bloc ``||OLED: clear OLED ||`` (trad. : effacer l'écran) sous le bloc ``||variables: définir Temps ||``.

Ajoute le bloc ``||OLED: show string ||`` (trad. : montrer la ligne) sous le bloc ``||OLED: clear OLED ||``.

Ajoute le bloc ``||OLED: show number||`` (trad. : montrer le nombre) sous le bloc ``||OLED: show string ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
    OLED.clear()
    OLED.writeString("")
    OLED.writeNum(0)
})

```

## Étape 6

Remplace la valeur ``||OLED: " " ||`` du bloc ``||OLED: show string ||`` par le mot Temperature (sans accent).

Remplace la valeur ``||OLED: 0 ||`` du bloc ``||OLED: show number ||`` par le bloc ``||variables: Temperature ||``.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
    OLED.clear()
    OLED.writeString("Temperature")
    OLED.writeNum(Temperature)
})

```


## Étape 7

Ajoute le bloc ``||basic:pause (ms)||`` sous le bloc ``||OLED:||``.

Remplace la valeur ``||basic:100||`` du bloc ``||basic:pause (ms)||`` par ``||basic:5000||``.


```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Temperature = 0
basic.forever(function () {
    Temperature = input.temperature()
    OLED.clear()
    OLED.writeString("Temperature")
    OLED.writeNum(Temperature)
    basic.pause(5000)
})


```

## Étape 8

Voici la programmation complète du programme.

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

let Temperature = 0
led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
    Temperature = input.temperature()
    OLED.clear()
    OLED.writeString("Temperature")
    OLED.writeNum(Temperature)
    basic.pause(5000)
})

```