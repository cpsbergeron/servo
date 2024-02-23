# Circuits électriques et servomoteur

# Tutoriel - Défi supplémentaire

## @showdialog

Transforme le micro:bit en récepteur. 

## Étape 1

Ajout le bloc ``||radio:radio définir groupe||`` dans le bloc ``||basic:au démarrage||``.

```blocks

radio.setGroup(1)

```

## Étape 2

Modifie le bloc ``||radio:radio définir groupe||``.

Remplace la valeur ``||radio:1||`` par une valeur entre  ``||radio:1||`` et  ``||radio:255||``.

Le valeur pour l'émetteur et le récepteur doit être la même.

```blocks

radio.setGroup(1)

```

## Étape 3

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||basic: au démarrage||``.

```blocks

pins.servoWritePin(AnalogPin.P0, 180)

```

## Étape 4

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 0 ||``.

```blocks

pins.servoWritePin(AnalogPin.P2, 0)

```

## Étape 5

Ajoute trois blocs ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P13 = Jaune - P14 = Rouge

```blocks

pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)
pins.digitalWritePin(DigitalPin.P0, 0)

```

## Étape 6

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace les broches ``|| pins: P0 ||`` par ``|| pins: P12 ||``, ``|| pins: P13 ||`` et ``|| pins: P14 ||``.

Remplace les valeurs ``|| pins: 0 ||`` par ``|| pins: 0 ||``, ``|| pins: 0 ||`` et ``|| pins: 1 ||``.

P12 = Vert - P13 = Jaune - P14 = Rouge

```blocks

pins.servoWritePin(AnalogPin.P2, 0)
pins.digitalWritePin(DigitalPin.P12, 0)
pins.digitalWritePin(DigitalPin.P13, 0)
pins.digitalWritePin(DigitalPin.P14, 1)

```

## Étape 7

Ajoute le bloc ``|| pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 180)
})

```

## Étape 8

Modifie les valeurs du bloc ``|| pins: régler position servo ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P2 ||``.

Remplace la valeur ``|| pins: 180 ||`` par ``|| pins: 90 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
})

```

## Étape 9

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo ||``.

P12 = Vert - P13 = Jaune - P14 = Rouge

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P0, 0)
    })

```

## Étape 10

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
})

```

## Étape 11

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
})

```

## Étape 12

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
})

```

## Étape 13

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer l'icône ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 14

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P14 ||``.

La valeur ``|| pins: 0 ||`` demeure la même.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
})


```

## Étape 15

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
})


```

## Étape 16

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 17

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
})

```

## Étape 18

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
})

```

## Étape 19

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| basic: pause (ms) ||``.

Dessine un petit X.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
})

```

## Étape 20

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: montrer LEDs ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P0, 0)
})

```

## Étape 21

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P13 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 0 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
})

```

## Étape 22

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

La valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` demeure la même.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
})

```

## Étape 23

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) ||``.


```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P0, 0)
})


```

## Étape 24

Modifie les valeurs des blocs ``|| pins: écrire sur la broche ||``.

Remplace la broche ``|| pins: P0 ||`` par ``|| pins: P12 ||``.

Remplace la valeur ``|| pins: 0 ||`` par ``|| pins: 1 ||``.

Regarde l'indice!

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
})


```

## Étape 25

Ajoute le bloc ``|| basic: pause (ms) ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Remplace la valeur ``|| basic: 100 ||`` du bloc ``|| basic: pause (ms) ||`` par la valeur ``|| basic: 1000 ||``.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(1000)
})


```

## Étape 26

Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| basic: pause (ms) ||``.

Regarde l'indice.

```blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P2, 90)
    pins.digitalWritePin(DigitalPin.P14, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.No)
    pins.digitalWritePin(DigitalPin.P14, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P13, 1)
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . # . # .
        . . # . .
        . # . # .
        . . . . .
        `)
    pins.digitalWritePin(DigitalPin.P13, 0)
    basic.pause(100)
    pins.digitalWritePin(DigitalPin.P12, 1)
    basic.pause(1000)
    basic.showIcon(IconNames.Yes)
})


```

## @showdialog 

Réalise une programmation pour fermer la barrière lorsque le bouton B est pressé.

Duplique le bloc ``||input:lorsque le bouton A est pressé||`` et modifie les valeurs.

## Étape 27

Ajoute le bloc ``||logic:si vrai alors||`` dans le bloc ``||radio:quand une donnée est reçue par radio receivedString||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (true) {
    	
    }
})

```

## Étape 28

Remplace la valeur ``||logic:vrai||`` du bloc ``||logic:si vrai alors||`` par le bloc ``||logic:"" = ""||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if ("" == "") {
    	
    }
})

```

## Étape 29

Modifie le bloc ``||logic:"" = ""||``.

Remplace ``||logic:""||`` de gauche par le bloc ``||pins:receivedString||``. 

Pour y arriver, fais glisser le bloc ``||pins:receivedString||`` du bloc ``||radio:quand une donnée est reçue par radio receivedString||`` dans le bloc ``||logic:""||`` de gauche.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "") {
    	
    }
})

```

## Étape 30

Modifie le bloc ``||logic:"" = ""||``. (suite)

Remplace ``||logic:""||`` de droite par le mot Ouvrir. 

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
})

```

## Étape 31

Ajoute le bloc ``||logic:si vrai alors||`` sous le bloc ``||logic:si vrai alors||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if (true) {
    	
    }
})

```

## Étape 32

Remplace la valeur ``||logic:vrai||`` du bloc ``||logic:si vrai alors||`` par le bloc ``||logic:"" = ""||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if ("" == "") {
    	
    }
})

```

## Étape 33

Modifie le bloc ``||logic:"" = ""||``.

Remplace le bloc ``||logic:""||`` de gauche par le bloc ``||pins:receivedString||``. 

Pour y arriver, fais glisser le bloc ``||pins:receivedString||`` du bloc ``||radio:quand une donnée est reçue par radio receivedString||`` dans le bloc ``||logic:""||`` de gauche.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if (receivedString == "") {
    	
    }
})

```

## Étape 34

Remplace le bloc ``||logic:""||`` de droite par le mot Fermer. 

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
    	
    }
    if (receivedString == "Fermer") {
    	
    }
})

```

## Étape 35

Glisse la programmation sous le bloc ``||input: lorsque le bouton A est pressé||`` dans le bloc ``||logic:si Ouvrir alors||``.

Supprime le bloc ``||input: lorsque le bouton A est pressé||``.

```blocks

radio.onReceivedString(function (receivedString) {
    if (receivedString == "Ouvrir") {
        pins.servoWritePin(AnalogPin.P2, 90)
        pins.digitalWritePin(DigitalPin.P14, 1)
        basic.pause(500)
        basic.showIcon(IconNames.No)
        pins.digitalWritePin(DigitalPin.P14, 0)
        basic.pause(100)
        pins.digitalWritePin(DigitalPin.P13, 1)
        basic.pause(500)
        basic.showLeds(`
            . . . . .
            . # . # .
            . . # . .
            . # . # .
            . . . . .
            `)
        pins.digitalWritePin(DigitalPin.P13, 0)
        basic.pause(100)
        pins.digitalWritePin(DigitalPin.P12, 1)
        basic.pause(500)
        basic.showIcon(IconNames.Yes)
    }
    if (receivedString == "Fermer") {
    	
    }
})

```

## Étape 36

Glisse la programmation sous le bloc ``||input: lorsque le bouton B est pressé||`` dans le bloc ``||logic:si Fermer alors||``.

Supprime le bloc ``||input: lorsque le bouton B est pressé||``.

## @showdialog 

Félicitations! Tu as terminé de programmer le récepteur.

Pour tester, télécharge la programmation dans le micro:bit.

Assure-toi que l'émetteur est bien branché et programmé.