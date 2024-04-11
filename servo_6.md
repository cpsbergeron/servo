# Circuits électriques et servomoteur

# Tutoriel 6

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

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 5

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les valeurs des blocs ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 0 ||``, ``|| pins: 0 ||`` et ``|| pins: 0 ||``.

Regarde l'indice!

```blocks

pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 0)

```

## Étape 6

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Température||``.

Ajoute le bloc ``||variables: définir Température ||`` dans le bloc ``|| basic: au démarrage ||``.

```blocks

let Température = 0
pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 0)

```

## Étape 7

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Température ||`` par le bloc ``||input: température||``. 

```blocks

let Température = input.temperature()
pins.servoWritePin(AnalogPin.P1, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 0)

```

## Étape 8

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    basic.showNumber(0)
})

```

## Étape 9

Modifie le bloc ``|| basic: montrer nombre ||``.

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer nombre ||`` par le bloc ``||variables: Température ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
})

```

## Étape 10

Ajoute le bloc ``|| basic: pause ||`` sous le bloc ``|| basic: montrer nombre ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(100)
})

```

## Étape 11

Modifie le bloc ``|| basic: pause (ms) 100 ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
})

```

## Étape 12

Ajoute le bloc ``|| logic: si vrai alors ||`` sous le bloc ``|| basic: pause ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (true) {
        
    }
})

```

## Étape 13

Modifie le bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors ||`` par le bloc ``|| logic: 0 ≤ 0 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (0 <= 0) {
        
    }
})

```

## Étape 14

Modifie le bloc ``|| logic: 0 ≤ 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 21 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        
    }
})

```

## Étape 15

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P0, 180)
    }
})

```

## Étape 16

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P1 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 45 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
    }
})

```

## Étape 17

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P0, 0)
        pins.digitalWritePin(DigitalPin.P0, 0)
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 18

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les valeurs ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace la valeur ``|| pins: 0 ||`` du bloc ``|| pins: P12 ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 19

Dupplique le bloc ``|| logic: si vrai alors ||`` et glisse-le sous le bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 20

Modifie le deuxième bloc ``|| logic: si vrai alors ||``.

Remplace le bloc ``|| logic: 0 ≤ 0 ||`` par le bloc ``|| logic: et ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (false && false) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 21

Modifie le bloc ``|| logic: et ||``.

Remplace la ``|| logic: valeur ||`` de gauche par le bloc ``|| logic: 0 ≥ 0 ||``.

Remplace la ``|| logic: valeur ||`` de droite par le bloc ``|| logic: 0 ≤ 0 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (0 >= 0 && 0 <= 0) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 22

Modifie le bloc ``|| logic: 0 ≥ 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 22 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 0 <= 0) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 23

Modifie le bloc ``|| logic: 0 ≤ 0 ||``.

Remplace la valeur ``|| logic: 0 ||`` de gauche par le bloc ``|| variables: Température ||``.

Remplace la valeur ``|| logic: 0 ||`` de droite par la valeur ``|| logic: 27 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 27 <= Température) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 24

Modifie les valeurs des blocs ``|| pins: régler position servo ||`` et des blocs ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| pins: 45 ||`` de ``|| pins: régler position servo ||`` par ``|| pins: 90||``.

Remplace la valeur ``|| pins: 1 ||`` de ``|| pins: P12 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P13 ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 27 <= Température) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 1)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 25

Dupplique le premier bloc ``|| logic: si vrai alors ||`` et glisse-le sous le deuxième bloc ``|| logic: si vrai alors ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 27 <= Température) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 1)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 26

Modifie le troisième bloc ``|| logic: si vrai alors ||``.

Remplace le bloc ``|| logic: 0 ≤ 0 ||`` par le bloc ``|| logic: 0 ≥ 0 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 27 <= Température) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 1)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 27

Modifie le troisième bloc ``|| logic: si vrai alors ||``.

Remplace la valeur ``|| logic: 27 ||`` par la valeur ``|| logic: 28 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 27 <= Température) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 1)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
})

```

## Étape 28

Modifie les valeurs du bloc ``|| pins: régler position servo ||`` et des blocs ``|| pins: écrire sur la broche ||``.

Remplace le valeur ``|| pins: 45 ||`` du bloc ``|| pins: régler position servo ||`` par ``|| pins: 180||``.

Remplace la valeur ``|| pins: 1 ||`` de ``|| pins: P13 ||`` par ``|| pins: 0 ||``.

Remplace la valeur ``|| pins: 0 ||`` de ``|| pins: P14 ||`` par ``|| pins: 1 ||``.

```blocks

basic.forever(function () {
    let Température = 0
    basic.showNumber(Température)
    basic.pause(1000)
    if (Température <= 21) {
        pins.servoWritePin(AnalogPin.P1, 45)
        pins.digitalWritePin(DigitalPin.P12, 1)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 22 && 27 <= Température) {
        pins.servoWritePin(AnalogPin.P1, 90)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 1)
        pins.digitalWritePin(DigitalPin.P14, 0)
    }
    if (Température >= 28) {
        pins.servoWritePin(AnalogPin.P1, 180)
        pins.digitalWritePin(DigitalPin.P12, 0)
        pins.digitalWritePin(DigitalPin.P13, 0)
        pins.digitalWritePin(DigitalPin.P14, 1)
    }
})

```

## @showdialog 

Félicitations! Tu as terminé de programmer un circuit électrique avec un servomoteur.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.