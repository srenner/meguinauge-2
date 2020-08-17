# meguinauge-2

**MEG**asquirt + ard**UIN**o + g**AUGE** = meguinauge. Pronounced "meh-gween-edge." Or however you want. 20x4 character LCD gauge for [MegaSquirt](http://megasquirt.info/).

## Overview
* Provides a vehicle gauge that can display 1 or 2 different engine parameters at a time.
* Designed for a 1980s-1990s aesthetic.

## Hardware details (to be installed in car)
* [Arduino-compatible AST-CAN485 Dev Board](https://www.sparkfun.com/products/14483)
* 16x2 LCD display with serial communication
* Red LED
* 1 pushbutton

## User Interface
Engine parameters will be displayed on a 16x2 LCD display. Each engine parameter will be shown with a short code and a number. For example, "CLT 203.5" means the coolant temperature is 203.5 degrees. The short codes will be familiar to MegaSquirt users. When 2 or 4 gauges are shown on the display, a bar graph will also be shown for each engine parameter.

The pushbutton will be used to cycle through the different gauge displays and modes.

A red LED is illuminated when one or more of the engine parameters goes outside of its predefined range. When all engine parameters return to their normal range, the LED will stay illuminated for a few more moments. The amount of time the LED remains illuminated depends on the amount of time a parameter was out of range.

## MegaSquirt details
* Tested using MegaSquirt-3 with firmware version 1.5.0.
* Uses MegaSquirt's "Simplified Dash Broadcasting" as described in [this PDF](http://www.msextra.com/doc/pdf/Megasquirt_CAN_Broadcast.pdf).
