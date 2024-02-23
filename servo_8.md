# Circuits électriques et servomoteur

# Tutoriel 7

## @showdialog

Programme le micro:bit, le servomoteur et le circuit électrique.

## Étape 1

Supprime le bloc ``||basic:toujours||``.


## Étape 2

Ajoute le bloc ``||pins:régler position servo||`` dans le bloc ``||basic:au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 3

Modifie le bloc ``||pins:régler position servo||``.

Remplace la broche ``||pins:P0||`` par ``||pins:P1||``.

Remplace la valeur ``||pins:180||`` par ``||pins:0||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)

```

## Étape 4

Ajoute deux blocs ``||pins:écrire sur la broche||`` sous le bloc ``||pins:régler position servo||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 5

Modifie les blocs ``||pins:écrire sur la broche||``.

Remplace les broches ``||pins:P0||`` par ``||pins:P12||`` et ``||pins:P13||``.

Les valeurs ``||pins:0||`` demeurent les mêmes.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)

```

## Étape 6

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Angle||``.

Ajoute le bloc ``||variables: définir Angle ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = 0
})

```

## Étape 7

Modifie le bloc ``||variables: définir Angle ||``.

Remplace la valeur ``||variables: 0 ||`` par le bloc ``||math: choisir au hasard ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(0, 10)
})

```

## Étape 8

Modifie le bloc ``||math: choisir au hasard ||``.

Remplace la valeur ``||math: 0 ||`` par ``||math: 1 ||``.

Remplace la valeur ``||math: 10 ||`` par ``||math: 180 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
})

```

## Étape 9

Ajoute le bloc ``||basic: montrer nombre ||`` sous le bloc ``||variables: définir Angle ||``.

Remplace la valeur ``||basic: 0 ||`` par le bloc ``||variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
})

```

## Étape 10

Ajoute le bloc ``||basic: pause ||`` sous le bloc ``||basic: montrer nombre ||``.

Remplace la valeur ``||basic: 100 ||`` par la valeur ``||basic: 2000 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
})

```

## Étape 11

Ajoute le bloc ``||logic: si vrai alors ||`` sous le bloc ``||basic: pause ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (true) {
    	
    }
})

```

## Étape 12

Modifie le bloc ``||logic: si vrai alors ||``.

Remplace la valeur ``||logic: vrai ||`` par le bloc ``||logic: 0 < 0 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (0 < 0) {
    	
    }
})


```

## Étape 13

Modifie le bloc ``||logic: 0 < 0 ||``.

Remplace la ``||logic: 0 ||`` de gauche par le bloc ``||variables: Angle ||``.

Remplace la ``||logic: 0 ||`` de droite par la valeur ``||logic: 90 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (Angle < 90) {
    	
    }
})

```

## Étape 14

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||logic: si alors ||``.

Remplace la broche ``||pins: P0 ||`` par la valeur ``||pins: P1 ||``.

Remplace la valeur ``||pins: 180 ||`` par le bloc ``||variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (Angle < 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
    }
})

```

## Étape 15

Ajoute deux blocs ``||pins: écrire sur la broche ||`` sous le bloc ``||pins: régler position servo ||``.

Remplace les broches ``||pins: P0 ||`` par  ``||pins: P12 ||`` et ``||pins: P13 ||``.

Remplace les valeurs ``||pins: 0 ||`` par ``||pins: 1 ||`` et ``||pins: 0 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (Angle < 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
    }
})

```

## Étape 16

Ajoute le bloc ``||basic: montrer LEDs ||`` sous le bloc ``||pins: écrire sur la broche ||``.

Dessine la lettre A dans le bloc ``||basic: montrer LEDs ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (Angle < 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        basic.showLeds(`
            . . # . .
            . # . # .
            # . . . #
            # # # # #
            # . . . #
            `)
    }
})

```

## Étape 17

Duplique le bloc ``||logic: si vrai alors||`` et positionne celui-ci sous le bloc ``||logic: si vrai alors||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (Angle < 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        basic.showLeds(`
            . # # # .
            # # . # #
            # . . . #
            # # # # #
            # . . . #
            `)
    }
    if (Angle < 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        basic.showLeds(`
            . # # # .
            # # . # #
            # . . . #
            # # # # #
            # . . . #
            `)
    }
})


```

## Étape 18

Modifie les valeurs pour que :
- le ``||pins: servomoteur ||`` puisse réaliser un angle obtus lorsque le ``||input: bouton A est pressé ||``,
- la lumière en ``||pins: P12 ||`` s'éteigne,
- la lumière en ``||pins: P13 ||`` s'allumer,
- la ``||basic: lettre O ||`` (pour obtus) s'affiche.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 180)
    basic.showNumber(Angle)
    basic.pause(2000)
    if (Angle < 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        basic.showLeds(`
            . # # # .
            # # . # #
            # . . . #
            # # # # #
            # . . . #
            `)
    }
    if (Angle > 90) {
        pins.servoWritePin(AnalogPin.P1, Angle)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 1)
        basic.showLeds(`
            . # # # .
            # # . # #
            # . . . #
            # # . # #
            . # # # .
            `)
    }
})


```

## Étape 19

Ajoute le bloc ``||basic: effacer l'écran||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.clearScreen()
})

```

## Étape 20

Ajoute les blocs de programmation manquants pour réinitialiser le servomoteur à 0 et éteindre les lumières lorsque le bouton B est pressé.

Regarde l'indice et modifie les valeurs incorrectes.

```blocks

input.onButtonPressed(Button.B, function () {
    basic.clearScreen()
    pins.servoWritePin(AnalogPin.P0, 180)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## @showdialog 

Bravo! Tu as terminé de programmer.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.