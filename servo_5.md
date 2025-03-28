# Circuits électriques et servomoteur

# Tutoriel 5

## @showdialog

Programme le micro:bit, le servomoteur et le circuit électrique.

## Étape 1

Supprime le bloc ``||basic:toujours||``.


## Étape 2

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P16 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P16, 0)

```

## Étape 4

Ajoute deux blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

pins.servoWritePin(AnalogPin.P16, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 5

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les valeurs ``|| pins: P0 ||`` par ``|| pins: P12 ||`` et ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P12 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P13 ||`` par ``|| pins: 1 ||``.

P12 = Vert - P13 = Rouge

```blocks

pins.servoWritePin(AnalogPin.P16, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 1)

```

## Étape 6

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 7

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: P0 ||`` par ``|| pins: P16 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
})

```

## Étape 8

Ajoute deux blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    })

```

## Étape 9

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les valeurs ``|| pins: P0 ||`` par ``|| pins: P12 ||`` et ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P12 ||`` par ``|| pins: 1 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P13 ||`` par ``|| pins: 0 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` par ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(1000)
})

```

## Étape 11

Ajoue le bloc ``|| basic: montrer l'icône ||`` sous le bloc ``|| basic: pause ||``.

Remplace le ``|| basic: le grand coeur ||`` par un ``|| basic: crochet ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(1000)
    basic.showIcon(IconNames.Yes)
})

```

## Étape 12

Duplique le bloc ``|| input: lorsque le bouton A est pressé ||``.

Remplace la valeur ``|| input: A ||`` par ``|| input: B ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(1000)
    basic.showIcon(IconNames.Yes)
})

```

## Étape 13

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| pins: 90 ||`` par ``|| pins: 0 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P16, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(1000)
    basic.showIcon(IconNames.Yes)
})

```

## Étape 14

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: 1 ||`` de ``|| pins: P12 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P13 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
    pins.digitalWritePin(DigitalPin.P12, 0)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.Yes)
})

```

## Étape 15

Remplace le ``|| basic: crochet ||`` par un ``|| basic: X ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P16, 0)
    pins.digitalWritePin(DigitalPin.P12, 1)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer une barrière et des lumières.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.