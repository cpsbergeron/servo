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

Remplace la broche ``|| pins: P0 ||`` par ``|| pins : P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins : 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 4

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Aigu||``.

Ajoute le bloc ``||variables: définir Aigu ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = 0
})


```

## Étape 5

Remplace la valeur ``|| variables : 0 ||`` du bloc ``|| variables : définir Aigu ||`` par le bloc ``||math: choisir au hasard||``.

```blocks

input.onButtonPressed(Button.A, function () {
    Aigu = randint(0, 10)
})

```

## Étape 6

Moidifie les valeurs du bloc ``||math: choisir au hasard||``.

Remplace la valeur ``|| math : 0 ||`` par ``|| math : 1 ||``.

Remplace la valeur ``|| math : 10 ||`` par ``|| math : 89 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
})


```

## Étape 7

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``|| variables: définir Aigu ||``

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 8

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``|| variables: Aigu ||``.

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Aigu)
})

```

## Étape 9

Ajoute le bloc ``|| basic: montrer nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Aigu ||``.

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Aigu)
    basic.showNumber(Aigu)
})


```

## Étape 10

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Aigu)
    basic.showNumber(Aigu)
    basic.pause(5000)
})

```

## Étape 11

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``|| basic: pause ||``

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Aigu)
    basic.showNumber(Aigu)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 12

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``|| pins: 0 ||``.

```blocks

let Aigu = 0
input.onButtonPressed(Button.A, function () {
    Aigu = randint(1, 89)
    pins.servoWritePin(AnalogPin.P2, Aigu)
    basic.showNumber(Aigu)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P2, 0)
})

```

## Étape 13

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Obtus||``.

Ajoute le bloc ``||variables: définir Obtus ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = 0
})

```

## Étape 14

Remplace la valeur ``|| variables : 0 ||`` du bloc ``|| variables : définir Obtus ||`` par le bloc ``||math: choisir au hasard||``.

```blocks

input.onButtonPressed(Button.B, function () {
    Obtus = randint(0, 10)
})

```

## Étape 15

Moidifie les valeurs du bloc ``||math: choisir au hasard||`` par les valeurs d'un angle aigu.

Remplace la valeur ``|| math : 0 ||`` par ``|| math : 91 ||``.

Remplace la valeur ``|| math : 10 ||`` par ``|| math : 179 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
})

```

## Étape 16

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``|| variables: définir Obtus ||``

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 17

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``|| variables: Obtus ||``.

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
    pins.servoWritePin(AnalogPin.P2, Obtus)
})

```

## Étape 18

Ajoute le bloc ``|| basic: montrer nombre ||`` sous le bloc ``|| pins: régler position servo ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Obtus ||``.

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
    pins.servoWritePin(AnalogPin.P2, Obtus)
    basic.showNumber(Obtus)
})

```

## Étape 19

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 5000 ||``.

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
    pins.servoWritePin(AnalogPin.P2, Obtus)
    basic.showNumber(Obtus)
    basic.pause(5000)
})

```

## Étape 20

Ajoute le bloc ``|| pins: régler position servo ||`` sous le bloc ``|| basic: pause ||``

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
    pins.servoWritePin(AnalogPin.P2, Obtus)
    basic.showNumber(Obtus)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P0, 180)
})


```

## Étape 21

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par le bloc ``|| pins: 0 ||``.

```blocks

let Obtus = 0
input.onButtonPressed(Button.B, function () {
    Obtus = randint(91, 179)
    pins.servoWritePin(AnalogPin.P2, Obtus)
    basic.showNumber(Obtus)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P2, 0)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.