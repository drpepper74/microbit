# ElecFreaks micro:bit Smart Home Kit

# Tutoriel 15

## @showdialog

Invente une programmation en utilisant les conditions complexes "ET" / "OU".

## Étape 1

Utilise le plus de blocs possibles.

Bonne chance !

```package

dstemps=github:tinkertanker/pxt-smarthome

```

```blocks

input.onButtonPressed(Button.A, function () {
    OLED.clear()
    OLED.writeStringNewLine("Celcius")
    OLED.writeNumNewLine(Celcius)
    if (Lumen > 50 || Lumen < 50) {
        music.play(music.tonePlayable(131, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    }
})
input.onButtonPressed(Button.AB, function () {
    basic.pause(100)
})
input.onButtonPressed(Button.B, function () {
    OLED.clear()
    OLED.drawLoading(Lumen)
    if (Lumen > 50 && Lumen < 50) {
        music.play(music.tonePlayable(988, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    }
})
let Lumen = 0
let Celcius = 0
pins.servoWritePin(AnalogPin.P0, 180)
pins.digitalWritePin(DigitalPin.P0, 0)
led.enable(false)
OLED.init(128, 64)
music.setVolume(127)
let strip = neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB)
strip.showColor(neopixel.colors(NeoPixelColors.Black))
basic.forever(function () {
    basic.pause(100)
})
loops.everyInterval(1000 * 5, function () {
    Celcius = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, AnalogPin.P2)
    Lumen = smarthome.ReadLightIntensity(AnalogPin.P3)
})

```

## @showdialog 

Félicitations! Tu as terminé la programmation. Réalise maintenant les branchements.

Pour tester le circuit électrique, télécharge la programmation dans le micro:bit.