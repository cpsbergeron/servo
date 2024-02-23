# Circuits électriques et servomoteur

# Tutoriel 9

## @showdialog

Programme le micro:bit, le servomoteur et le circuit électrique.

## Étape 1

Supprime le bloc ``||basic:toujours||``.


## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Angle||``.

Ajoute le bloc ``||variables: définir Angle ||`` dans le bloc ``||basic:au démarrage||``.

```blocks

let Angle = 0

```

## Étape 3

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||variables:définir Angle||``.

Remplace la broche ``||pins: P0 ||`` par ``||pins: P2 ||``.

Remplace la valeur ``||pins: 180 ||`` par ``||pins: 0 ||``.

```blocks

let Angle = 0
pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 4

Ajoute les blocs ``||pins: écrire sur la broche ||`` sous le bloc ``||pins:régler position servo||``.

Remplace les broches ``||pins: P0 ||`` par ``||pins: P12 ||``, ``||pins: P13 ||`` et ``||pins: P14 ||``.

Les valeurs ``||pins: 0 ||`` demeurent les mêmes.

```blocks

let Angle = 0
pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 0)

```

## Étape 5

Ajoute le bloc ``||loops: répéter ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

Remplace la valeur ``||loops: 4 ||`` par ``||loops: 36 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
    	
    }
})

```

## Étape 6

Ajoute le bloc ``||variables: modifier Angle ||`` dans le bloc ``||loops:répéter||``.

Remplace la valeur ``||variables: 1 ||`` par ``||variables: 5 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
    }
})

```

## Étape 7

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||variables:modifier Angle||``.

Remplace la valeur ``||pins: P0 ||`` par la valeur ``||pins: P2 ||``.

Remplace la valeur ``||pins: 180 ||`` par le bloc ``||variables: Angle ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
    }
})

```

## Étape 8

Ajoute le bloc ``||basic: pause ||`` sous le bloc ``||pins:régler position servo||``.

Remplace la valeur ``||basic: 100 ||`` par la valeur ``||basic: 500 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
    }
})

```

## Étape 9

Ajoute le bloc ``||logic: si vrai alors ||`` sous le bloc ``||basic:pause||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (true) {
        	
        }
    }
})

```

## Étape 10

Ajoute le bloc ``||logic: 0 < 0 ||`` dans le bloc ``||logic:si vrai alors||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (0 < 0) {
        	
        }
    }
})


```

## Étape 11

Modifie le bloc ``||logic: 0 < 0 ||``.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: Angle ||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 60 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
        	
        }
    }
})

```

## Étape 12

Ajoute les blocs ``||pins: écrire sur la broche ||`` sous le bloc ``||logic: 0 < 0 ||``.

Remplace les broches ``||pins: P0 ||`` par ``||pins: P12 ||``, ``||pins: P13 ||`` et ``||pins: P14 ||``.

Remplace les valeur ``||pins: 0 ||`` par ``||pins: 1 ||``, ``||pins: 0 ||`` et ``||pins: 0 ||``.


```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
    }
})

```

## Étape 13

Ajoute le bloc ``||logic: si vrai alors ||`` sous le bloc ``||logic: si vrai alors ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (true) {
        	
        }
    }
})

```

## Étape 14

Remplace la valeur ``||logic: vrai ||`` par le bloc ``||logic: et ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (false && false) {
        	
        }
    }
})

```

## Étape 15

Modifie le bloc ``||logic: et ||``.

Remplace la valeur de gauche par le bloc ``||logic: 0 > 0 ||``.

Remplace la valeur de droite par le bloc ``||logic: 0 < 0 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (0 > 0 && 0 < 0) {
        	
        }
    }
})

```

## Étape 16

Modifie le bloc ``||logic: 0 > 0 ||`` de gauche.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: Angle ||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 61 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && 0 < 0) {
        	
        }
    }
})

```

## Étape 17

Modifie le bloc ``||logic: 0 < 0 ||`` de droite.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: Angle ||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 119 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && Angle < 119) {
        	
        }
    }
})

```

## Étape 18

Ajoute les blocs ``||pins: écrire sur la broche ||`` sous le bloc ``||logic: et ||``.

Remplace les broches ``||pins: P0 ||`` par ``||pins: P12 ||``, ``||pins: P13 ||`` et ``||pins: P14 ||``.

Remplace les valeurs ``||pins: 0 ||`` par ``||pins: 0 ||``, ``||pins: 1 ||`` et ``||pins: 0 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && Angle < 119) {
            pins.digitalWritePin(DigitalPin.P12, 0)
            pins.digitalWritePin(DigitalPin.P13, 1)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
    }
})


```

## Étape 19

Ajoute le bloc ``||logic: si vrai alors ||`` sous le bloc ``||logic: si vrai alors ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && Angle < 119) {
            pins.digitalWritePin(DigitalPin.P12, 0)
            pins.digitalWritePin(DigitalPin.P13, 1)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (true) {
        	
        }
    }
})


```

## Étape 20

Ajoute le bloc ``||logic: 0 > 0 ||`` dans le bloc ``||logic:si vrai alors||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && Angle < 119) {
            pins.digitalWritePin(DigitalPin.P12, 0)
            pins.digitalWritePin(DigitalPin.P13, 1)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (0 > 0) {
        	
        }
    }
})


```

## Étape 21

Modifie le bloc ``||logic: 0 > 0 ||``.

Remplace la valeur ``||logic: 0 ||`` de gauche par le bloc ``||variables: Angle ||``.

Remplace la valeur ``||logic: 0 ||`` de droite par la valeur ``||logic: 120 ||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && Angle < 119) {
            pins.digitalWritePin(DigitalPin.P12, 0)
            pins.digitalWritePin(DigitalPin.P13, 1)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 120) {
        	
        }
    }
})


```

## Étape 22

Ajoute les blocs ``||pins: écrire sur la broche ||`` sous le bloc ``||logic: 0 > 0 ||``.

Remplace les broches ``||pins: P0 ||`` par ``||pins: P12 ||``, ``||pins: P13 ||`` et ``||pins: P14 ||``.

Remplace les valeurs ``||pins: 0 ||`` par ``||pins: 0 ||``, ``||pins: 0 ||`` et ``||pins: 1||``.

```blocks

let Angle = 0
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 36; index++) {
        Angle += 5
        pins.servoWritePin(AnalogPin.P2, Angle)
        basic.pause(500)
        if (Angle < 60) {
            pins.digitalWritePin(DigitalPin.P12, 1)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 61 && Angle < 119) {
            pins.digitalWritePin(DigitalPin.P12, 0)
            pins.digitalWritePin(DigitalPin.P13, 1)
            pins.digitalWritePin(DigitalPin.P14, 0)
        }
        if (Angle > 120) {
            pins.digitalWritePin(DigitalPin.P12, 0)
            pins.digitalWritePin(DigitalPin.P13, 0)
            pins.digitalWritePin(DigitalPin.P14, 1)
        }
    }
})

```

## Étape 23

Ajoute le bloc ``||input:lorsque le bouton B est pressé||`` pour réinitialiser les valeurs du servomoteur et des lumières.

## @showdialog 

Bravo! Tu as terminé de programmer.

Pour tester le circuit, réalise les branchements et télécharge la programmation dans le micro:bit.