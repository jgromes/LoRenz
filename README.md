# LoRenz

<img src="https://github.com/jgromes/LoRenz/blob/master/doc/LoRenz_shield.png" alt="LoRenz shield" width="40%" height="40%"/>

## Arduino shield/module to allow easy use of the LoRa communication modules

---

## Work in progress warning
This shield is still early in developement. The shield, module or breakout layouts might be changed at any moment! Watch this repo for progress updates.

---

### This is not the library you are looking for!
If you're looking for Arduino library to use with these modules, it has its own repository: [https://github.com/jgromes/LoRaLib](https://github.com/jgromes/LoRaLib)

---

DISCLAIMER: All schematic and board files are provided 'AS IS'. see `license.txt` for details.

The following is a listing of all the files in the `eagle` folder:

* `shield`

  This will most likely be the starting point of your experiments with LoRa. The shield is compatible with Arduino R3 pinout and has many ways to make your life easier. The main features include:
  
  * Dedicated 3.3V linear regulator to provide more than enough power for the LoRa module.
  * Arduino UNO and Mega compatibility.
  * On-board prototyping area with separate power rails.
  * Coaxial connector on the breakout board for connecting antenna.
  * NSS jumper to allow for LoRenz shield stacking.
  
  Please note that to use this shield, you will need to have a breakout board to mount the LoRa module.
  IMPORTANT: There are several incompatible types of these modules being sold, make sure that your module matches your breakout board!
  
  Arduino UNO setup:
  To use LoRenz shield with Arduino UNO, short all the jumpers on U/M pin header. You will also have to short one of the pin pairs on NSS pin header. See the picture for details.
  
  The NSS pin header allows you to stack up to four LoRenz shields on one Arduino (why would you though?!) by shorting different pin pair on each shield. Use pin 7 for default LoRaLib settings. See LoRaLib reference for details.
  
  Arduino Mega setup:
  To use LoRenz shield with Arduino Mega, remove all the shorting jumpers from U/M pin header. Arduino Mega has the SPI located on pins 20-22, connect the shield to these pins as per the following image.
  
  The shield has a place for LED that will light up when there are data being transferred to/from the LoRa module. To enable this feature, short the EN pads with solder.

* `breakout_green`

  This breakout board matches the following LoRa module:
  
  <img src="https://github.com/jgromes/LoRenz/blob/master/doc/SX1278_green_top.png" alt="SX1278 Green module top" width="355" height="300"/>
  
  <img src="https://github.com/jgromes/LoRenz/blob/master/doc/SX1278_green_bottom.png" alt="SX1278 Green module bottom" width="355" height="300"/>
  
  These seem to be fairly common, however, there are several slightly different pinouts. Prior to any soldering, make sure that the module pinout matches the pin description on the breakout board!

* `breakout_blue`

  This breakout board matches the following LoRa module:
  
  <img src="https://github.com/jgromes/LoRenz/blob/master/doc/SX1278_blue_top.png" alt="SX1278 Blue module top" width="355" height="300"/>
  
  <img src="https://github.com/jgromes/LoRenz/blob/master/doc/SX1278_blue_bottom.png" alt="SX1278 Blue module bottom" width="355" height="300"/>
  
  The amount of these modules on the market seems to be declining lately, but it's still possible to buy them. Again, there are multiple different pinouts.
