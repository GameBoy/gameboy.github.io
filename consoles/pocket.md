---
layout: wiki

title: Game Boy Pocket
category: Consoles

logo: logos/GameBoyPocket.png
photo: consoles/GameBoyPocket.jpg
model: MGB
---
This model is a much smaller redesign of the original [Game Boy](gameboy). It uses two AAA batteries and has a slightly improved screen with a grey reflection film compared to the original Game Boy's green. Early models of the Game Boy Pocket lacked the battery indicator LED found next to the screen.

Table of Contents:
<!--ts-->
* [**Game Boy Pocket Problems**](--game-boy-pocket-problems--)
  * [Lost game saves](--lost-game-saves--)
  * [Flash carts do not work](--flash-carts-do-not-work--)
  * [Splotchy circles in LCD (after backlight/bivert install)](--splotchy-circles-in-lcd--)
* [**Game Boy Pocket Mods**](--game-boy-pocket-mods--)
<!--te-->

Last Content Revision: 2020-12-16

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
  
  
## **Game Boy Pocket Mods**

Looking for a backlight mod? Why not check out [this guide](../wiki/backlightmods#mgb) from /u/Admiral_Butter_Crust on all the different backlight kits for MGB. 
 
* Backlight (parts: [HHL](https://handheldlegend.com/collections/dmg/products/game-boy-backlight-dmg-and-pocket) or [Retromodding](https://www.retromodding.com/collections/gameboy-pocket/products/game-boy-backlight?variant=12258355576855)) – [Video Guide](https://www.youtube.com/watch?v=OezxcoxMWSc)/[Instructables guide.](http://www.instructables.com/id/Game-Boy-Backlight-DIY/) This is a similar process as the DMG  
    * A note on potential issues -- Check the problems section above for more info on "Newtonian Rings."
	* Tidy wiring method: https://www.reddit.com/r/Koji_Kendo/comments/62j5ga/mgb_backlit_lcd_screen_single_piece_module/

* One Chip / HiVision Replacement transflective LCD kit (AIO kit, smaller than stock, found on [aliexpress](https://www.aliexpress.com/item/4000277929265.html)) - [Video Guide](https://www.youtube.com/watch?v=gT1XbwIfRYk)

* BennVenn Replacement transflective LCD kit (**Freckleshack v2.5 - Aioli** parts from [BennVenn](https://bennvenn.myshopify.com/collections/aftermarket-lcds/products/freckleshack-pre-orders-batch-7?variant=29881069535335))

* Funnyplaying Replacement IPS LCD kit (from [Funnyplaying](https://funnyplaying.com/collections/product/products/gbp-retro-pixel-ips-lcd-kit)) - [Youtube](https://www.youtube.com/watch?v=lWLE5fMPz7Y)
    * First batch has buggy firmware that will affect the sound on some consoles and [funnyplaying has several options to remedy this.](https://www.instagram.com/p/CBKP7ftHI_9/) Subsequent batches include the fix already (if you're reading this and you haven't ordered a kit yet, the kit will already be fixed). 
	
* One Chip OSD Q5 IPS Kit (from [RGRS](https://retrogamerepairshop.com/collections/game-boy-pocket/products/gbp-game-boy-pocket-osd-backlight-mod-kit?variant=32560949297226)) - [Youtube](https://youtu.be/Z5tfjz52N5A)

* Bivert DMG module install (parts: [HandHeldLegend](https://handheldlegend.com/collections/dmg/products/game-boy-bivert-biversion-module)) – [Video Guide](https://www.youtube.com/watch?v=lqOtKcprt7Y)  

* Bivert chip install (and comparison) – [Step by step guide](https://handheldlegend.com/blogs/news/115066947-game-boy-pocket-bivert-installation-and-comparison)  

* Bivert mini module (parts: [HHL](https://handheldlegend.com/products/game-boy-pocket-bivert-module-mini)) - [Image Guide](https://imgur.com/a/HSkyd2U) or [Video Guide](https://www.youtube.com/watch?v=vAoFNnsCR24)

* Replacement shell/housing – [Written guide]( https://jonathansblog.co.uk/gameboy-pocket-case-mod)  

* USB Rechargeable battery mod – [Step by step guide](https://www.reddit.com/r/Gameboy/comments/63npzo/tutorial_gameboy_pocket_usb_rechargeable_mod/)

* Helder's replacement custom power switch (parts from [Helder's site](https://www.heldergametech.com/shop/gbc/gbc-gbp-power-switch/)) 
