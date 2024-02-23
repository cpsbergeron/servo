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

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 45 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
})

```

## Étape 4

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 5

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

## Étape 6

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.


```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 7

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
})

```

## Étape 8

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 9

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les broches ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 0 ||``, ``|| pins: 1 ||`` et ``|| pins: 0 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
    pins.digitalWritePin(DigitalPin.P12, 0)
    pins.digitalWritePin(DigitalPin.P13, 1)
    pins.digitalWritePin(DigitalPin.P14, 0)
})

```


## Étape 10

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.


```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 11

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

La valeur ``|| pins: 180 ||`` demeure la même.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
})

```

## Étape 12

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 13

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les broches ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 0 ||``, ``|| pins: 0 ||`` et ``|| pins: 1 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    pins.digitalWritePin(DigitalPin.P12, 0)
    pins.digitalWritePin(DigitalPin.P13, 0)
    pins.digitalWritePin(DigitalPin.P14, 1)
})

```

## Étape 14

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 15

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)


```

## Étape 16

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les broches ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Les valeurs ``|| pins: 0 ||`` demeurent les mêmes

Regarde l'indice!

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 0)


```

## @showdialog 

*** Attention ***

N'oublie pas de brancher le servomoteur dans P1 et de brancher les lumières dans P12 - P13 - P14.

Branche les lumières dans les broches jaunes (pôle positif) et dans les broches noires (pôle négatif / GND).

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur et des lumières.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.