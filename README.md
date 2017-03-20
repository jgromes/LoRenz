# LoRenz
## Arduino shield/module to allow easy use of the LoRa communication modules

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
  
  Please note that to use this shield, you will need to have a breakout board to mount the LoRa module.
  IMPORTANT: There are several incompatible types of these modules being sold, make sure that your module matches your breakout board!

* `breakout_green`

  This breakout board matches the following LoRa module:
  
  These seem to be fairly common, however, there are several slightly different pinouts. Prior to any soldering, make sure that the module pinout matches the pin description on the breakout board!

* `breakout_blue`

  This breakout board matches the following LoRa module:
  
  The amount of these modules on the market seems to be declining lately, but it's still possible to buy them.
