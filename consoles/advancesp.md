---
layout: wiki

title: Game Boy Advance SP
category: Consoles

logo: logos/GameBoyAdvanceSP.png
photo: consoles/GameBoyAdvanceSP.jpg
model: AGS
---
The first major redesign of the [Game Boy Advance](advance) changed the system to a clamshell design and also added a rechargeable lithium-ion battery. The biggest difference however was the addition of a front light to the screen. Excluding the somewhat rare Japanese exclusive [Game Boy Light](light), this was Nintendo’s first handheld with an internally lit screen. This system also switched from rubber membrane buttons, common on almost all Nintendo systems to this point, to dome tact switches. One common complaint about this system has been the removal of the headphone jack and the need of an adapter which plugs into the charger port, similar to modern smartphones.

## 101 Revision
Nearly Identical to the original Game Boy Advance SP, the revised 101 model finally added the much sought after backlit screen to the Game Boy line. Interestingly, this model debuted almost a full year after the release of the Nintendo DS but mainly in North America, European/Australian systems are extremely rare and Japan never got the revision. Although sold in large numbers, the backlit screen of this SP makes this model one of the most sought-after models of Game Boy, consequently its current price is usually higher than that of other Game Boy models. Exacerbating this price increase is the fact that many systems have been taken apart for their valuable screens.

Table of Contents:
<!--ts-->
* [**Game Boy Advance SP Problems**](--game-boy-advance-sp-problems--)
  * [One or both shoulder buttons do not work](--one-or-both-shoulder-buttons-do-not-work--)
  * [Game Boy Advance SP power LED is always RED even on new batteries or LED will flicker/ will restart randomly or if jolted](--game-boy-advance-sp-power-led-is-always-red-even-on-new-batteries-or-led-will-flicker--)
  * [When charging the console, the charge light does not come on at all/ only comes on for a second before turning off](--when-charging-the-console,-the-charge-light--)
  * [Shell is cracked or broken in multiple places](--the-shell-is-cracked-or-broken-in-multiple-places--)
* [**Game Boy Advance SP Mods**](--game-boy-advance-sp-problems--)
<!--te-->

Last Content Revision: 2020-12-16
 
## **Game Boy Advance SP Problems**

Don't forget that [the common problems section](index) also has more info, such as failure to power on, speaker issues, or battery issues.
 
* One or both shoulder buttons do not work
 
  * What is it? When pressing either the L or R button, sometimes or always the input is not registered by the console. Like the power switch, the buttons internally tend to gather dirt and gunk and no longer make electrical contact when actuated.
  * How do I fix it? The console will need to be disassembled and the switch cleaned or replaced. Replacement switches can be sourced on places like Mouser, Digikey, or RetroModding, but usually cleaning the button is sufficient. Occasionally the buttons can be cleaned without disassembling by soaking in rubbing alcohol or electrical contact cleaner (please allow sufficient time to dry before reassembly), but disassembling the switch or replacing it entirely may yield the best results.
  
* Game Boy Advance SP power LED is always RED even on new batteries or LED will flicker/ will restart randomly or if jolted
 
  * What is it? Both of these issues are usually caused by the same problem. The power switch on the console tends to accumulate dirt and gunk and will make poor contact. This will result in your Game Boy getting worse battery life and it will significantly decrease the reliability.
  * How do I fix it? You'll need to clean or replace the power switch. Please see the "Common Problems" section for more info.
  
* When charging the console, the charge light does not come on at all/ only comes on for a second before turning off

  * What is it? These two problems are a symptom of greater issues. In most cases, this issue requires disassembly and soldering to repair. 
  * How do I fix it? If the light does not come on at all, double check that your charger works. If you do not have another console to test it with, try picking up a cheap USB charging cable for only a few dollars. You can find them on aliexpress or ebay or from your usual parts places. If the light comes on for a second and then shuts off, the first thing to check is the battery. If you have a multimeter, check to make sure the voltage on the battery is over 3.4 volts. If it is under 3 volts, recycle the battery and purchase a new one. If it is over 3 volts, you likely have another issue but the console will not boot unless the battery is at least 3.4 volts. If you do not have a multimeter, you can try to purchase a new battery but do be aware that the aftermarket cells are usually only 400-700 mAh despite what they may claim. If neither of these fixes resolve your issues, then you'll have to disassemble to console.
    * If neither a new battery or another charger helped, you'll need to take apart the console. Before you do any further troubleshooting or repairs, first check for any signs of water damage on the PCB. If the water indicator sticker (should be on the bottom of the PCB near the power switch) is tripped (appears solid red or pink or is missing entirely) or if you see any corrosion or other signs of water damage, you may wish to take pictures and consult help. If nothing else, take pictures first before cleaning the corrosion as the corrosion will likely only be in areas connected to circuits you may have trouble with. 
	* It has been observed that a common ingress of water into the console is from the front speaker grill. Due to where the cart reader sits on the board, water that makes its way in from there can become trapped and cause localized corrosion. The path of the charge circuit runs directly next to the speaker hole so it is easy for liquids to get trapped and those traces to get compromised. You can use a multimeter to probe continuity from D1 to F2, if you identify a break in the line a jumper wire between any suitable points in between may resolve the issue with the charge circuit. There may be additional components between D1 and F2 based on the board revision you are looking at, please refer to [Gekkio's AGS schematic of the AGS-CPU-11](https://github.com/Gekkio/gb-schematics/blob/master/AGS-CPU-11/schematic/AGS-CPU-11.pdf) and do your own visual inspection of the traces on your board to confirm if there are any further breaks that require repair.
	* If there are no signs of water damage, here are some steps you can take to narrow down and finally repair the issue.
	  * If the charge light does not come on at all and you've ruled out the power adapter or the charge light comes on for a second and turns off and you've ruled out the battery, the issue may be the port itself or the EM8 filter near the charge port. You'll need to perform a visual inspection of the port itself and the PCB around the port for anything that looks off. If you do not see any obvious issues, you'll need to plug in the console while you have it disassembled and try and trace the power lines from the port with a multimeter. If you see power at the port and no where else, you should try to reflow the solder on the pins. To narrow down if the issue is with EM8, typically one can just apply pressure to the component (with your fingers) and plug the console in with a battery. If the console charges normally in this case, [you may need to reflow the solder connected to EM8 or replace it entirely.](https://www.youtube.com/watch?v=O03_c7dS_8U) Feel free to take clear pictures and ask around on [discord](https://discord.gg/gameboy) or reddit if you have questions.
	  * If the charge light does not come on at all and you've ruled out the power adapter, the issue may be with the component F2. F2 is a small surface mount fuse located near the link port on the back of the PCB. With your multimeter, check and see if you have continuity across the component. If not, you'll need to replace this fuse. [Check out this (WIP) spreadsheet for the P/N and spec of a replacement fuse.](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/) Do keep in mind that fuses are safety devices and they only ever blow to protect the system from faults. If your fuse does not have continuity across it, that means it has blown due to a fault. You need to ensure that the fault is cleared before replacing the fuse or the next fuse will blow too. If you opt to bypass the fuse instead of replacing it and your system develops a fault, you could destroy your system entirely with no hope of repair. F2 typically blows when there is a short across the charge port or if there is a fault with the charger itself. 
	  * If the charge light comes on for a second and shuts off and you've already ruled out the battery, this could indicate a blown fuse. Does your console boot normally? If the console does not boot on a known (or at least assumed) good battery, you'll need to check the component F1. This is a surface mount fuse and it is located on the front of the PCB right underneath the A and B buttons. With your multimeter, check and see if you have continuity across the component. If not, you'll need to replace this fuse. [Check out this (WIP) spreadsheet for the P/N and spec of a replacement fuse.](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/)
	* If none of this helped, congrats, you have a unique issue. Try posting on discord or reddit for help (with good pictures). 
	
* Shell is cracked or broken in multiple places

  * What is it? The shells of some late model AGS consoles are made with defective plastics that tend to get extremely brittle over time. This issue seems most prevalent with Pearl Blue AGS-101 consoles but may affect Graphite AGS-101 consoles or other late model units. [See this imgur album](https://imgur.com/a/dhfax) for more information. 
  * How do I fix it? Well, unfortunately, there is know currently known fix for this issue. If the console is already broken, you can try to glue it back together but the structural damage to the plastic has already been done and this will likely be temporary at best. The only way to "fix" this is to reshell the console in either a new aftermarket shell or with a salvaged OEM shell from another SP. 
  

## **Game Boy Advance SP Mods**

Looking for a backlight mod? Why not check out [this guide](../wiki/backlightmods#ags) from /u/Admiral_Butter_Crust on all the different backlight kits for AGS. 
 
* AGS-001 increased brightness mod ("AGS-010") and extended life battery – [Written Guide](https://imgur.com/a/5Ptdh)

* Funnyplaying Replacement IPS LCD kit (Funnyplaying v1, based on AGB v2 mod, works on both models of AGS, parts from [Funnyplaying](https://funnyplaying.com/products/gbasp-ips-laminated-display-lcd-kits) – [Video Guide](https://www.youtube.com/watch?v=PH3Pzn24smc)

* One Chip Replacement IPS LCD kit (v1, similar to funnyplaying mod, parts from [RGRS](https://retrogamerepairshop.com/products/game-boy-advance-sp-backlight-mod-kit)) – [Video](https://youtu.be/fR3bml4oqTo)

* Replacement NDSL LCD kit (From BennVenn, smaller than stock, same as AGB kit) – coming soon^^^TM

* AGS-101 LCD (for AGS-001 models, required parts: [a voltage regulator](https://bennvenn.myshopify.com/collections/cheap-stuff/products/backlit-sp-lcd-101-led-driver-board) and, optionally, [a brightness controller.](https://bennvenn.myshopify.com/collections/cheap-stuff/products/digital-backlight-brightness-controller-for-gbc-and-gba-101-lcds?variant=48320644564)) – [Video Guide](https://www.youtube.com/watch?v=Z0ttua-EDDk) (deprecated)

* DSi Battery Mod – [Written Guide](https://imgur.com/a/1KNWp)
    * A note on these mods, DSi batteries are 12+ years old at this point and aftermarket replacements often lie about the capacity. This was a better mod when Nintendo still sold newly manufactured DSi batteries. Beware. 

* "Makho Battery Mod," a cheap, high capacity (~950mAh), and 100% reversable battery mod – [Youtube](https://www.youtube.com/watch?v=VjnONhSVvpA)
    * Want to bump it up to 1640mAh? If your console is IPS modded, [there should be room behind the LCD for two more batteries to install in parallel with the original.](https://imgur.com/a/wZgPfAe) You'll need a 303030 and a 303450 sized battery. Put all three batteries in parallel (red to red to + and black to black to - ). Pics from /u/jeeper5150 and [mod](https://www.reddit.com/r/Gameboy/comments/fc3or4/1640mah_gba_sp/) from /u/jeff93063 

* LED Button/Emblem Mod – [Pictures](https://imgur.com/a/dhLK4) and [Video](https://www.youtube.com/watch?v=V8zDdRCFC-o)

* LED Emblem – [Written Guide](https://imgur.com/a/JXCUR)

* Overclock switch – [Written Guide](https://imgur.com/a/vfyhe)

* Install a new shell – [Written Guide](https://imgur.com/a/7iYbx)

* Replace hinge pins (shell swap) – [Written Guide](https://imgur.com/a/z21z1) or [this thread/video guide](https://www.reddit.com/r/Gameboy/comments/bxzub8/how_to_easily_remove_the_hinges_from_a_gba_sp/)
    * [Tips on Game Boy [Advance] SP hinge replacement](https://www.reddit.com/r/Gameboy/comments/f6f2z1/tips_on_game_boy_sp_hinge_replacement/)

* Internal headphone jack mod – [Github repo with multiple installs documented](https://github.com/rorosaurus/gba-sp-headphone-jack)
	
* USB Type C Charge Port Mod - [Design files/instructions](https://github.com/rorosaurus/gba-sp-usb-c) - [Purchase (USA)](https://smile.amazon.com/dp/B08L72TZWD) - [Purchase (non-USA)](https://www.tindie.com/products/rorosaurus/usb-c-mod-for-game-boy-advance-sp/)
    * Alternate (centered) version - [Github repo](https://github.com/nMinhBang/GBA-SP_USB-C)
	
* Makho/RetroCNC Machined Aluminum replacement shell - [coming soon^tm](https://retro-cnc.com/products/game-boy-advance-sp)

* Helder's replacement custom power switch (parts from [Helder's site](https://www.heldergametech.com/shop/gba/gbasp-power-switch/)) 
	
 
