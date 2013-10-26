---
layout: default
title: APM:Copter - Connecting your components
---

# APM:Copter - Connecting your components

The documentation uses a Crius V2 as example flight controller,
but the Pin number is the same for all flight controllers.

## Connecting the RC Input

By default MegaPirateNG uses PPM RC Input.

Connect your PPM RC Receiver to ```Pin A8``` on your flight controller.

![RC Channels no PPM](../images/connecting_components_rcchannels_ppm.png)

If you want to use a non PPM RC Receiver you need to change your [RC Input Type Configuration](general_configuration#rc_input_type_configuration)
and connect the RC Receiver like this.

| Pin  | Channel          |
| -----|:----------------:|
| A8   | Yaw / Rudder     |
| A9   | Pitch / Elevator |
| A10  | Throttle         |
| A11  | Aileron          |
| A12  | Mode Switch      |

![RC Channels](../images/connecting_components_copter_rcchannels.png)

## Connecting Motors

![Rotation informations](../images/connecting_components_copter_motors_rotation.png)

### Quad-Copter in + and X configuration
![Motor for Quad Copter](../images/connecting_components_copter_motors_quad.png)

### Tri-Copter
![Motor and Servo for Tri Copter](../images/connecting_components_copter_motors_tri.png)

### Hexa-Copter
![Motor for Hexa Copter](../images/connecting_components_copter_motors_hexa.png)

### Octo-Copter
![Motor for Octo Copter](../images/connecting_components_copter_motors_octo.png)

### V Octo-Copter, Y6 and X8
![Motor for Octo Copter](../images/connecting_components_copter_motors_special.png)