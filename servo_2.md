# Circuits électriques et servomoteur

# Tutoriel 2

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

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 3

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)

```

## Étape 4

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    basic.showNumber(0)
})

```

## Étape 5

Modifie le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``|| input: niveau d'intensité lumineuse ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
})

```

## Étape 6

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| basic: montrer nombre ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(100)
})

```

## Étape 7

Modifie le bloc ``|| basic: pause ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 2000 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
})

```

## Étape 8

Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| basic: pause ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (true) {
        
    }
})

```

## Étape 9

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 <= 0 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (0 <= 0) {
        
    }
})

```

## Étape 10

Modifie le bloc ``|| logic: 0 <= 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| input: niveau d'intensité lumineuse ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 39 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (input.lightLevel() <= 39) {
        
    }
})

```

## Étape 111

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (input.lightLevel() <= 39) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})

```

## Étape 12

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

La valeur ``|| pins: 180 ||`` demeure la même.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (input.lightLevel() <= 39) {
        pins.servoWritePin(AnalogPin.P1, 180)
    }
})

```

## Étape 13

Dupplique le bloc ``|| logic: si vrai alors ||`` et glisse-le sous le bloc ``|| logic: si vrai alors ||``.

Regarde l'indice au besoin.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (input.lightLevel() <= 39) {
        pins.servoWritePin(AnalogPin.P1, 180)
    }
    if (input.lightLevel() <= 39) {
        pins.servoWritePin(AnalogPin.P1, 180)
    }
})

```

## Étape 14

Modifie le nouveau bloc ``|| logic: si vrai alors ||``.

Remplace ``|| logic: 0 <= 0 ||`` par ``|| logic: 0 >= 0 ||``.

Remplace la valeur ``|| logic: 39 ||`` par ``|| logic: 40 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

basic.forever(function () {
    basic.showNumber(input.lightLevel())
    basic.pause(2000)
    if (input.lightLevel() <= 39) {
        pins.servoWritePin(AnalogPin.P1, 180)
    }
    if (input.lightLevel() >= 40) {
        pins.servoWritePin(AnalogPin.P1, 0)
    }
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.