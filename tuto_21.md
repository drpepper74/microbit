# Niveau 5

# Tutoriel 21

## @showdialog

Crée un circuit électrique et numérique.

## Étape 2 

Ajoute le bloc ``|| pins: écrire sur la broche  ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``. 
 
Remplace la valeur sur la broche ``|| pins: P0  ||`` par ``|| pins: 1  ||``.
 

```blocks 

input.onButtonPressed(Button.A, function () {
    pins.digitalWritePin(DigitalPin.P0, 1)
})

``` 

## Étape 3 
 
Ajoute le bloc ``|| pins: écrire sur la broche  ||`` dans le bloc ``||input:lorsque le bouton B est pressé||``. 
 
Remplace la valeur sur la broche ``|| pins: P0  ||`` par ``|| pins: 0  ||``.
 
```blocks 

input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
})

``` 
## @showdialog 

Branche une pince alligator au port "P0" du micro:bit.

La couleur du fil n'a pas d'importance!

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_a_1.jpg?raw=true) 

## @showdialog 

Relis la même pince alligator à une lumière LED à la broche positive. Il s'agit de la plus longue.

La couleur n'a pas d'importance!

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_a_2.jpg?raw=true) 

## @showdialog 

Branche une autre pince alligator dans le port "GND" du micro:bit. 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_a_3.jpg?raw=true) 

## @showdialog 

Relis la même pince alligator de la lumière LED à la broche négative. Il s'agit de la plus petite.

Attention, les deux broches ne doivent pas se toucher!

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_a_4.jpg?raw=true) 

## @showdialog 

Félicitations! Tu as terminé ton premier circuit électrique avec une lumière LED.

Pour tester ton circuit électrique, télécharge la programmation dans le micro:bit.