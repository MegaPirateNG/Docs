---
layout: default
title: Troubleshooting
---

# Troubleshooting

## After a successfull compile the Arduino IDE hangs while uploading the firmware to the flight controller

There is a bug with old Arduino bootloaders, you have the following options:

1. If you have an AVR-ISP Programmer you can update the bootloader.
2. Change the ```#define BOOTLOADER_BUGFIX "234fs34567hf"``` line in your ```APM_Config.h```, replace the string ```"234fs34567hf"``` with some random characters and try to upload the firmware again.

## My Transmitter does not work

If you can move your sticks and the flight controller seams to not register any of your inputs its most likely you forgot configuring your correct RC Input type.
Please refer the [General Configuration](general_configuration#rc_input_type_configuration) documentation.
