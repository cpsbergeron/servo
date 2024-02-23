# Circuits électriques et servomoteur

# Tutoriel 2

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

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 4

Crée une ``||variables: variable||`` et donne lui le nom ``||variables: Angle||``.

Ajoute le bloc ``||variables: définir Angle||`` dans le bloc ``||input: lorsque incliné à droite||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = 0
})

```

## Étape 5

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Angle ||`` par le bloc ``||math: choisir au hasard de 0 à 10||``. 

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(0, 10)
})


```

## Étape 6

Remplace la valeur ``||math: 0||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par la valeur ``||math: 1||``.

Remplace la valeur ``||math: 10||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par la valeur ``||math: 89||``. 

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
})

```

## Étape 7

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||variables: définir Angle ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 8

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``||variables:  Angle ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Angle)
})

```

## Étape 9

Ajoute le bloc ``|| basic: montre nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Angle ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause  ||`` sous le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(5000)
})



```

## Étape 11

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||basic: pause ||``.


```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 12

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par  ``|| pins: 0 ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltRight, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P2, 0)
})


```

## Étape 13

Ajoute le bloc ``||variables: définir Angle||`` dans le bloc ``||input: lorsque incliné à gauche||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = 0
})

```

## Étape 14

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Angle ||`` par le bloc ``||math: choisir au hasard de 0 à 10||``. 

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(0, 10)
})


```

## Étape 15

Remplace la valeur ``||math: 0||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par ``||math: 91||``.

Remplace la valeur ``||math: 10||`` du bloc ``||math: choisir au hasard de 0 à 10 ||`` par ``||math: 180||``. 

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
})

```

## Étape 16

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||variables: définir Angle ||``.


```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 17

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``||variables:  Angle ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
})


```

## Étape 18

Ajoute le bloc ``|| basic: montre nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Angle ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
})

```

## Étape 19

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par ``|| basic: 5000 ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(5000)
})

```

## Étape 20

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``||basic: pause ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 21

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

let Angle = 0
input.onGesture(Gesture.TiltLeft, function () {
    Angle = randint(91, 180)
    pins.servoWritePin(AnalogPin.P2, Angle)
    basic.showNumber(Angle)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P2, 0)
})



```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.