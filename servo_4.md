# Circuits électriques et servomoteur

# Tutoriel 4

## @showdialog

Programme le micro:bit, le servomoteur et le circuit électrique.

## Étape 1

Conserve les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

```blocks

basic.forever(function () {
    
})

```

## Étape 2

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
basic.forever(function () {
	
})


```

## Étape 3

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
basic.forever(function () {
	
})

```
## Étape 4

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les broches ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Les valeurs ``|| pins: 0 ||`` demeurent les mêmes.

Regarde l'indice!

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 0)
basic.forever(function () {
	
})

```

## Étape 5

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 6

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 45 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
})

```

## Étape 7

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 8

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les broches ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 1 ||``, ``|| pins: 0 ||`` et ``|| pins: 0 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```

## Étape 9

Dupplique le bloc ``||input: lorsque le bouton A est pressé||`` et son contenu.

Remplace la valeur ``||input:A||`` par la valeur ``||input:B||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```

## Étape 10

Modifie le contenu du nouveau bloc ``||input: lorsque le bouton B est pressé||``.

Remplace la valeur ``|| pins: 45 ||`` de ``|| pins: P1 ||`` par ``|| pins: 90 ||``.

Remplace la valeur ``|| pins: 1 ||`` de ``|| pins: P12 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P13 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
    pins.digitalWritePin(DigitalPin.P12, 0)
    pins.digitalWritePin(DigitalPin.P13, 1)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```

## Étape 11

Dupplique le bloc ``||input: lorsque le bouton A est pressé||`` et son contenu.

Remplace la valeur ``||input: A||`` par la valeur ``||input: A+B||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```

## Étape 12

Modifie le contenu du nouveau bloc ``||input: lorsque le bouton B est pressé||``.

Remplace la valeur ``|| pins: 45 ||`` de ``|| pins: P1 ||`` par ``|| pins: 180 ||``.

Remplace la valeur ``|| pins: 1 ||`` de ``|| pins: P13 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P14 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    pins.digitalWritePin(DigitalPin.P12, 0)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 1)
})

```

## Étape 13

Dupplique le bloc ``||input: lorsque le bouton A est pressé||`` et son contenu.

Remplace le bloc ``||input:A||`` par le bloc ``||input:lorsquer secouer||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```

## Étape 12

Modifie le contenu du nouveau bloc ``||input: lorsque secouer||``.

Remplace la valeur ``|| pins: 45 ||`` de ``|| pins: P1 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 1 ||`` de ``|| pins: P12 ||`` par ``|| pins: 0 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    pins.servoWritePin(AnalogPin.P1, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```

## @showdialog 

*** Attention ***

N'oublie pas de brancher le servomoteur dans P1 et de brancher les lumières dans P12 - P13 - P14.

Branche les lumières dans les broches jaunes (pôle positif) et dans les broches noires (pôle négatif / GND).

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur et des lumières.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.