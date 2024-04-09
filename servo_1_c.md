# Circuits électriques et servomoteur

# Tutoriel 1 - C

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

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Angle||``.

Ajoute le bloc ``||variables: définir Angle ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = 0
})

```

## Étape 5

Remplace la valeur ``|| variables : 0 ||`` du bloc ``|| variables : définir Angle ||`` par le bloc ``||math: choisir au hasard||``.

```blocks

input.onButtonPressed(Button.A, function () {
    Angle = randint(0, 10)
})

```

## Étape 6

Moidifie les valeurs du bloc ``||math: choisir au hasard||``.

Remplace la valeur ``|| math : 0 ||`` par ``|| math : 1 ||``.

Remplace la valeur ``|| math : 10 ||`` par ``|| math : 89 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 89)
})

```

## Étape 7

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``|| variables: définir Angle ||``

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 8

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``|| variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle)
})

```

## Étape 9

Ajoute le bloc ``|| basic: montrer nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle)
    basic.showNumber(Angle)
})

```

## Étape 8

Dupplique la séquence de programmation du bloc ``||input:lorsque le bouton A est pressé||``.

## Étape 9

Modifie le nouveau bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||input:A||`` par ``||input:B||``.

Remplace la valeur ``||maths:1||`` par ``||maths:91||``.

Remplace la valeur ``||maths:89||`` par ``||maths:179||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.B, function () {
    Angle = randint(91, 179)
    pins.servoWritePin(AnalogPin.P1, Angle)
    basic.showNumber(Angle)
})

```
## Étape 10

Ajoute le bloc ``||basic:montrer nombre||`` dans le bloc ``||input:lorsque le bouton A+B est pressé||``.

Remplace la valeur ``||basic:montrer nombre||`` du bloc ``||basic:montrer nombre||`` par ``||variable:Angle||``

```blocks

input.onButtonPressed(Button.AB, function () {
    let Angle = 0
    basic.showNumber(Angle)
})

```

## Étape 11

Ajoute le bloc ``||variables:définir Angle||`` dans le bloc ``||input:lorsque secouer||``.

La valeur ``||variables:0||`` demeure la même.

```blocks

let Angle = 0
input.onGesture(Gesture.Shake, function () {
    Angle = 0
})

```

## Étape 12

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||variables:définir Angle||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.Shake, function () {
    Angle = 0
    pins.servoWritePin(AnalogPin.P0, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.