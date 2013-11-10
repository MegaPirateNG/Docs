---
layout: default
title: General Configuration
---

# General Configuration

All configuration here requires you to modify the source-code of MegaPirateNG. You need to save the changes and recompile / upload this changes with Arduino IDE.

## Changing Board Type

MegaPirateNG supports different types of flight controller boards. In order to get the Firmware running you have to specify which board you are using.

After opening the desired Sketch change to the ```APM_Config.h``` file in the tab-bar.
In this file you need to change the line ```#define MPNG_BOARD_TYPE   RCTIMER_CRIUS_V2``` with the
board you have.

The file also contains the list of supported boards in a comment block bellow the configuration define itself.

For example (using a crius v1):

    // Select Megapirate board type:
    #define MPNG_BOARD_TYPE   CRIUS_V1
    /*
       RCTIMER_CRIUS_V2    -- (DEFAULT!!!) Use ONLY for RCTimer CRIUS V2 board
       CRIUS_V1            -- Use this define for RCTimer CRIUS V1(1.1) board and all HobbyKing AIOP boards
       HK_RED_MULTIWII_PRO -- HobbyKing MultiWii Pro board with ITG3205 and BMA180, BMP085 sensors
       BLACK_VORTEX
    */

## Select frame type

If you use ***APM:Copter*** and you are not using a quad-copter you need to set the correct frame configuration for that frame.
If you do use a quad-copter, you can ignore this setting.

The configuration option is also located in the ```APM_Config.h``` file.

If you want to use, for example, a tri-copter you need to change the ```//#define FRAME_CONFIG HEXA_FRAME``` line.
First of you need to remove the ```//``` before the line to uncomment and use the configuration and set the value to ```TRI_FRAME```

For example (using a tri-copter):

    #define FRAME_CONFIG TRI_FRAME
    /*
     *  options:
     *  QUAD_FRAME
     *  TRI_FRAME
     *  HEXA_FRAME
     *  Y6_FRAME
     *  OCTA_FRAME
     *  OCTA_QUAD_FRAME
     *  HELI_FRAME
     */

## RC Input type configuration

Based on the type of your Receiver you have 3 possible configuration options.

1. Serial PPM on A8 pin selected (default)
2. Serial PPM (CPPM) on PL1 pin
3. Regular PWM inputs A8-A15

If you want to change the type to something other than the default you have to edit the file: ```libraries\AP_HAL_MPNG\RCInput_MPNG.cpp```

### Serial PPM (CPPM) on PL1 pin

Change ```#define SERIAL_PPM SERIAL_PPM_ENABLED``` to ```#define SERIAL_PPM SERIAL_PPM_ENABLED_PL1```

### Regular PWM inputs A8-A15

Change ```#define SERIAL_PPM SERIAL_PPM_ENABLED``` to ```#define SERIAL_PPM SERIAL_PPM_DISABLED```

## Change the RC input channel order

MegaPirateNG uses the default RC input channel order used by APM hardware, but you are able to change it if you like.

The configuration is located in the ```libraries\AP_HAL_MPNG\RCInput_MPNG.cpp``` file.

If you want to use, for example, the multiwii channel order you need to change the ```//#define RC_MAPPING RC_MAP_STANDARD``` line.
First of you need to remove the ```//``` before the line to uncomment and use the configuration and set the value to ```RC_MAP_MULTIWII```

For example (multiwii):

    #define RC_MAPPING RC_MAP_MULTIWII
    /*
            RC_MAP_STANDARD 1
            RC_MAP_GRAUPNER 2
            RC_MAP_HITEC 3
            RC_MAP_MULTIWII 4
            RC_MAP_JR 5
    */
