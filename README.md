# RP2040-keypad

## Table of Contents
* [General Info](#general-information)
* [Design](#design)
* [Ordering](#ordering)
* [Uploading Firmware](#uploading-firmware)
* [Case](#case)
* [Assembly](#assembly)


## General Information

This project was made as a learning experience on how to design a MCU-based PCB with minimum components.
It is a 2-key Keypad based on Raspberry RP2040 MCU. It doesn't have any button to enter bootmode, and no LED indicator. Simplicity was the main target.

## Design

This board was designed with KiCad. It is a 4 layer board with signal on the outer layer and power on the inner layer. It has serial wire pin-hole to debugging
and a USB-C header for connection to the host and power. The switches used for the key are mechanical switches and they are connected to GPIO6 and GPIO7. The other end
of the switch connected directly to ground. For programming the BOOT jumper pad must be shorted before connecting the USB.

## Ordering

Ordering and assembly can be done easily at JLCPCB. [Manufacturing_JLCPCB](./Manufacturing_JLCPCB) provide all the necessary files like Gerber, BOM, and components
placement for ordering the board.

## Uploading firmware

Uploading firmware with RP2040 IC is a very simple task. Just short the BOOT jumper while connecting the USB to PC. The board should appear as a mass storage device
on the host PC. Then just copy the [.uf2 file](./rp2040-keypad-1000hz.uf2) there and the board should reset itself. The firmware is installed with z and x as the key.

## Case

There is also a simple [case](./case.obj) for 3D printing. The following components are also required for the case:
  - 4 M2 14mm
  - 4 M2 hex nuts

## Assembly

1. Place both of the switch from the top case. It should hold the switches well
2. Align the PCB with the switch. Now should be the right time to solder the switches to the PCB
3. Insert all the hex nuts to the bottom case
4. Place the bottom case aligned with the top case and press until the PCB sits on the bottom case
5. Screw all the M2 screws to secure the case

