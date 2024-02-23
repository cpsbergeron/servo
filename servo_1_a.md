# Circuits électriques et servomoteur

# Tutoriel 1 - A

## @showdialog

Programme le micro:bit, le servomoteur et le circuit électrique.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic:au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 3

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)

```

## Étape 4

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 5

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 45 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
})


```

## Étape 6

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    basic.pause(5000)
})

```

## Étape 7

Ajoute le bloc ``|| pins: régler position du servo ||`` sous le bloc ``|| basic: pause ||``.

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P1, 0)
})

```

## Étape 8

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input:lorsque le bouton B est pressé||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 9

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 90 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
})


```

## Étape 10

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
    basic.pause(5000)
})

```

## Étape 11

Ajoute le bloc ``|| pins: régler position du servo ||`` sous le bloc ``|| basic: pause ||``.

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P1, 0)
})

```

## Étape 12

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input:lorsque le bouton A+B est pressé||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 9

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

La valeur ``|| pins: 180 ||`` demeure la même.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
})


```

## Étape 10

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    basic.pause(5000)
})

```

## Étape 11

Ajoute le bloc ``|| pins: régler position du servo ||`` sous le bloc ``|| basic: pause ||``.

Modifie le bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P1, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.