# Circuits électriques et servomoteur

# Tutoriel 1 - B

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

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P16 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P16, 0)

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

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P16 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 45 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P16, 45)
})

```

## Étape 6

Dupplique la séquence de programmation du bloc ``||input:lorsque le bouton A est pressé||``.

## Étape 7

Modifie le nouveau bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||input:A||`` par ``||input:B||``.

Remplace la valeur ``||pins:45||`` par ``||pins:90||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P16, 90)
})

```

## Étape 8

Dupplique la séquence de programmation du bloc ``||input:lorsque le bouton A est pressé||``.

## Étape 9

Modifie le nouveau bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||input:A||`` par ``||input:A+B||``.

Remplace la valeur ``||pins:45||`` par ``||pins:180||``.

```blocks

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P16, 180)
})

```

## Étape 10

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input:lorsque secouer||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P16 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
       pins.servoWritePin(AnalogPin.P16, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.

