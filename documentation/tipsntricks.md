---
layout: default
title: Tips and tricks
---

# Tips and tricks

This site tries to provide some code changes which could give you a nice extra feature.
But which is not really used by many so not an official setting.

## Get external LEDs and piezo buzzer working with Crius 1.1

The Crius board only allows you to connect ```A0 to A5``` so the default config does not work.
Here are the code-changes necessary to still have external LEDs and a piezo buzzer.

```config.h``` changes:

    #define PIEZO_PIN 46
    #define COPTER_LED_1 AN2 // Motor or Aux LED
    #define COPTER_LED_2 AN3 // Motor LED
    #define COPTER_LED_3 AN4 // Motor or GPS LED
    #define COPTER_LED_4 AN7 // Motor LED
    #define COPTER_LED_5 -1 // Motor LED
    #define COPTER_LED_6 -1 // Motor LED
    #define COPTER_LED_7 -1 // Motor LED
    #define COPTER_LED_8 -1 // Motor LED

```define.h``` changes:

    #define AN5 46
    // #define PIEZO_PIN 32 //Last pin on the back ADC connector
    #define PIEZO_PIN 46

After this changes, a compile and flash you can connect the arming led on ```A3```, the GPS led on ```A4``` and the Buzzer on ```PIN 46```.
You also need to set the ```Led Mode``` to ```127``` via Advanced parameters in the Mission Planner software.

## Use an external compass instead of using the internal

Sometimes you want to use an external compass instead of the flight controllers on board one.
In most cases its not really needed, but you have the option.

```libraries\AP_InertialSensor\AP_InertialSensor_MPU6000_I2C.cpp``` changes:

```//#define DISABLE_INTERNAL_MAG``` to ```#define DISABLE_INTERNAL_MAG```

After this changes, a compile and flash you also need to erase and reset to factory defaults via Mission Planner.

