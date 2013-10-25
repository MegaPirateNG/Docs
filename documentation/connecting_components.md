---
layout: default
title: Connecting your components
---

# Connecting your components

## Serial Ports

* Serial0 (RX0,TX0) - USB, OSD (Minim OSD) or Telemetry (3DR, Xbee, Bluetooth)
* Serial1 (RX1,TX1) - ***Not supported*** OSD which not compatible with Mavlink (Remzibi, E-OSD, FrSky)
* Serial2 (RX2,TX2) - GPS
* Serial3 (RX3,TX3) - OSD (Minim OSD) or Telemetry (3DR, Xbee, Bluetooth)

## RC Input and Outputs (Motors, Servos)

Please refer to the corresponding page for your Platform:

* [APM:Copter](connecting_components_copter)
* [APM:Plane](connecting_components_plane)

## Sonar

Using a sonar with MegaPirateNG is currently not supported.

## Camera Shutter

MegaPirateNG only supports relay type shutters.

You can connect the shutter device on ```pin 46``` on you flight controller and select appropriate Shutter in Camera Gimbal settings in Mission Planner.