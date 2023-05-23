# Sustainable Agriculture : The Power of Innovation 
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
ledRing=github:climate-action-kits/pxt-fwd-edu
```
## 
``||Step 1||`` 
On your screen you can see an ``||basic: on start||`` block and a ``||basic:forever||``
block. Insert or nest a ``||basic: show leds||`` under the ``||basic:on start||``.
Click on the boxes of the ``||basic:show leds||`` to turn the ``||basic:leds||``
ON or OFF. Let's try to write ``||Hi||`` by turning on the ``||basic:leds||`` of the 
``||basic:show leds||`` blocks. Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
```
## 
``||Step 2||``
Click on the ``||input:input||`` drawer. 
Find the ``||input: on button A pressed||`` block. Drag the block and place it 
on the coding screen.
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
})
```
## 
``||Step 3||``
Click on the ``||input:input||`` drawer. 
Find the ``||input: on button A pressed||`` block. Drag the block and place it 
on the coding screen. This time change ``||input:A||`` to ``||input:B||``
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
})
input.onButtonPressed(Button.B, function () {
})
```
## 
``||Step 4||``
The two buttons ``||input:A||`` and ``||input:B||`` will control the operation of the
the ``||Smart Irrigation System||``. To turn the ``||water pump||`` on ``||input: Button A||``
will be used. Next go to ``||fwdMotors:Motors||`` drawer and find 
``||fwdMotors:set pump ON||`` drag this block and nest it under ``||input:on button A pressed||``

Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
   fwdMotors.pump.fwdSetActive(true)
})
input.onButtonPressed(Button.B, function () {
})
```
## 
``||Step 5||``
The ``||input:Button B||`` is used for stopping the ``||water pump||``. From the
``||fwdMotors:Motors||`` drawer drag the ``||fwdMotors:set pump off||`` block
and nest it under ``||input:on button B pressed||`` block. 
Click on the blub to show your hint.
```blocks
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
input.onButtonPressed(Button.A, function () {
   fwdMotors.pump.fwdSetActive(true)
})
input.onButtonPressed(Button.B, function () {
    fwdMotors.pump.fwdSetActive(false)
})
```
## @showhint 
On pressing ``||input: Button A||`` should make your ``||water pump||``
turn on and when ``||input: Button B||`` is pressed the ``||water pump||`` stops.
Add artifical lighting for your ``||Smart Irrigation System||``. Go to 
``||basic:basic drawer||`` and drag the ``||basic:forever||`` loop
Nest a conditional statement ``||logic: if else||``
```blocks
input.onButtonPressed(Button.A, function () {
    fwdMotors.pump.fwdSetActive(true)
})
input.onButtonPressed(Button.B, function () {
    fwdMotors.pump.fwdSetActive(false)
})
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
basic.forever(function () {
    if () {
            } else if () {
            }
})
```
## @showhint 
Next add the ``||logic:true||`` condition ``||input: on button A pressed||`` turn on the 
``||fwdSensors:LED Light||`` of a particular color or ``||input : on button B pressed||`` the 
``||logic: Else||`` condition the ``||fwdSensors:LED Light||`` should be turned off.
```blocks
input.onButtonPressed(Button.A, function () {
    fwdMotors.pump.fwdSetActive(true)
})
input.onButtonPressed(Button.B, function () {
    fwdMotors.pump.fwdSetActive(false)
})
basic.showLeds(`
    # . # . #
    # . # . .
    # # # . #
    # . # . #
    # . # . #
    `)
basic.forever(function () {
    if (input.buttonIsPressed(Button.A)) {
        fwdSensors.ledRing.fwdSetAllPixelsColour(44)
    } else if (input.buttonIsPressed(Button.B)) {
        fwdSensors.ledRing.fwdSetAllPixelsColour(0)
    }
})
```