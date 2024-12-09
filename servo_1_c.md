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

Ajoute le bloc ``|| loops: répéter 4 fois ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle)
    for (let index = 0; index < 4; index++) {
    	
    }
})

```

## Étape 9

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| loops: répéter 4 fois ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    Angle = randint(1, 89)
    pins.servoWritePin(AnalogPin.P1, Angle)
    for (let index = 0; index < 4; index++) {
        basic.showNumber(Angle)
    }
})

```


## Étape 11

Dupplique la séquence de programmation du bloc ``||input:lorsque le bouton A est pressé||``.

## Étape 12

Modifie le nouveau bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||input:A||`` par ``||input:B||``.

Remplace la valeur ``||math:1||`` par ``||math:91||``.

Remplace la valeur ``||math:89||`` par ``||math:179||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.B, function () {
    Angle = randint(91, 179)
    pins.servoWritePin(AnalogPin.P1, Angle)
    basic.showNumber(Angle)
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.