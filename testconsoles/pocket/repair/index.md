---
layout: wiki

title: Game Boy Pocket
category: Consoles

logo: logos/GameBoyPocket.png
photo: consoles/GameBoyPocket.jpg
model: MGB
---
## **Game Boy Pocket Problems**

Don't forget that [the common problems section](index) also has more info, such as failure to power on or speaker issues. 
 
* Lost game saves
 
  * What is it? Game saves become corrupted after playing in modified MGB consoles. The original power regulator in the console has difficulty supplying an adequate amount of power for both the console and the mods (e.g. back light) when the batteries start to run low and such the game begins drawing current from the SRAM battery backup instead of the cartridge slot. This will corrupt saves or delete them entirely if the battery is depleted.
  * How do I fix it? For the most part, installing a lithium ion battery will help to resolve the power delivery issues as the voltage supplied is quite a bit higher and more consistent but the best solution is to install a 5v voltage regulator for the cartridge slot. The voltage regulator should be able to handle low voltages if your console is still using AAAs but [it should be wired directly into the cartridge slot](https://i.imgur.com/tYBwzmL.png).
 
* Flash carts do not work
 
  * What is it? Flash carts like the EverDrive will crash the system while loading a ROM. This is caused by the same issue as the corrupted save issue above and has a similar remedy. Basically, the flash cart draws more current than the system can provide
  * How do I fix it? While a lithium ion battery may curb the save related issue, this issue requires a separate voltage regulator to be installed. [The wiring is going to be the same](https://i.imgur.com/tYBwzmL.png) and the system will maintain full compatibility with all OEM carts afterwards.

* Splotchy circles in LCD (after backlight/bivert install)
 
  * What are they? Circles under the LCD that looks like trapped liquid. See [this image for an example.](https://i.redd.it/wsvc4e42n7u41.jpg) This phenomenon is called "Newtonian Rings" and is common in these circumstances. 
  * How do I fix it? The fix will involve either completely separating the glass LCD from the plastic polarizer layer (air gap) or completely joining them together (adhesive polarizer). See this video from /u/esotericsean for [a method of air gapping the polarizer.](https://www.youtube.com/watch?v=-6_s_kNVT0o) If you want to join the polarizer to the LCD OEM style, you'll need a polarizer with pre-applied adhesive. Air gapping is the preferred method. This also applied to the original Game Boy (DMG). 