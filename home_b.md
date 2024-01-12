# ElecFreaks micro:bit Smart Home Kit

# Tutoriel supplémentaire - B

## @showdialog

Invente une programmation.

## Étape 1

Utilise le plus de blocs possibles.

Bonne chance !

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    OLED.writeStringNewLine("Celcius")
    OLED.writeNumNewLine(Celcius)
})
input.onButtonPressed(Button.AB, function () {
    OLED.clear()
})
input.onButtonPressed(Button.B, function () {
    OLED.clear()
    OLED.drawLoading(Lumen)
})
let strip: neopixel.Strip = null
let Lumen = 0
let Celcius = 0
led.enable(false)
OLED.init(128, 64)
basic.forever(function () {
    basic.pause(100)
})
loops.everyInterval(1000 * 5, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
    if (Celcius > 25 && Lumen > 50) {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Orange))
    } else {
        strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
        strip.showColor(neopixel.colors(NeoPixelColors.Black))
    }
})


```

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.