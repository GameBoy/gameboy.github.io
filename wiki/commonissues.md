---
layout: wiki

title: Game Boy Common Issues
category: Wiki

---
All of these issues are covered in the relevant [console page](../consoles) (most with more info) but this is just a quick document to detail the most common issues.
 

## **Game Pak Problems**

Bootleg spotting: [Check out this visual guide](gamechecker) or even the /r/gameverifying [wiki](https://www.reddit.com/r/gameverifying/wiki/index)

* [How to replace a battery in a Game Boy cartridge](https://www.youtube.com/watch?v=n3FsANHj300). If you use the "tape method" you will be shunned and made fun of, simultaneously. Solder and a tabbed CR1616 (must for GBA games) or tabbed CR2025/CR2032 are required. 
   
* [Garbled or incomplete Nintendo logo](https://i.redd.it/7n5f50urdy821.jpg) or corrupt or missing sprites in Pokemon
	* How do I fix it? 
	 * Check another game. If multiple games do this, the issue is with your console. Check your mods and ensure there are no shorts or [clean the cart reader.](https://www.youtube.com/watch?v=y-gE7t9Mk3w)
	 * Check another Game Boy. If the cart fails to boot on that too, [try following these steps.](https://www.youtube.com/watch?v=0gqNEyQLecQ).

## **Common problems**

* **Power LED flickers, low battery light comes on early or intermittently, or the console randomly resets** are all issues caused by a dirty or faulty power switch.  Dirty or damaged switches can usually be fixed by cleaning out the switch. The most effective method to clean the power switch is to disassemble the switch and ensure everything is clean all the oxidation and buildup from the inside-out. The far less effective method to clean the switch is to spray contact cleaner or isopropyl alcohol inside the switch and simply work the switch back and forth. Make sure to let the switch dry out before turning it back on. Opening the switch is the most reliable and best long term solution. Other methods may still help, but should be considered a temporary fix. AGBs exhibit a flickering lower power LED and are the simplest to clean. [Video](https://www.youtube.com/watch?v=G946mQCkIQc) CGBs and MGBs share a similar physical switch body and are opened the same way. Cleaning the power switch is the same method as AGB. [Video](https://youtu.be/EVTKBHR0vVw)

* **Game Boy won’t power on**
 
    * On an unmodded console, the most common issue is a **dirty or damaged power switch** and can usually be fixed by cleaning out the switch. See above.
 
	* **Blown fuses** are a bit harder to fix simply because of the tiny soldering required. To test your fuse, a multimeter is usually needed. Simply measuring continuity across the fuse will tell you if the fuse has blown. Continuity shows power is flowing and the fuse is good. No continuity means the fuse has blown and opened circuit. Most Game Boys have two fuses, usually marked “F1” and “F2” on the main boards. Usually one fuse is connected to the battery terminals and the other fuse connected to the external power input, ie charging port in AGS and OXY or DC jack on CGB and MGB. Note, fuses are safety devices and a blown fuse is cause for further investigation and diagnostics. Please see [this (WIP) list of Game Boy components](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/) to find the proper replacement fuse.
	
	* **Damaged DC power jack** in a Game Boy Pocket or Game Boy Color system can make the console appear dead. A simple [USB to DC power](https://retrogamerepairshop.com/products/jellybelly-game-boy-color-pocket-light-3-3v-usb-cable?_pos=1&_sid=b642ce805&_ss=r&variant=32547179233354) adapter can help diagnose this issue. Similarly to the headphone jack, a physical switch exists in the DC jack that disconnects the battery terminals from the system when on DC power. Contacts within the DC jack may corrode from moisture and open the physical switch permanently. Careful cleaning can help, but with the center pin in the way, thorough cleaning may be difficult. Limited new and used DC jacks are available through eBay and AliExpress. For diagnostics, pin 2 and 3 as labeled on the console may be bridged. This should not be a permanent fix without fully removing the DC jack. Applying power to batteries with a DC jack inserted is dangerous. Alkaline batteries can explode.

	* **Bad battery or battery connector** in some models can cause issues. In models that came with rechargeable batteries (AGS and OXY), the battery may need replacement. [AGS](https://www.retromodding.com/products/makho-game-boy-advance-sp-battery) [OXY](https://retrogamerepairshop.com/collections/game-boy-micro/products/game-boy-micro-750mah-high-capacity-replacement-battery-by-makho?variant=37848673255596)
On alkaline models, the connectors can get dirty or completely corroded. In cases of mild dirt or corrosion, a simple clean with a cotton swap and isopropyl will resolve the issue. In heavier cases of corrosion without physical damage, distilled vinegar and a cotton swab may be used to clean away all the corrosion. Terminals can be desoldered from the console and removed from the case shell to be soaked in vinegar for more severe corrosion. When vinegar is used, isopropyl should be used to wash away the vinegar as it is corrosive and will damage the board. In extreme cases of corrosion and battery leakage, the terminals will be corroded through and require replacement. [DMG](https://retrogamerepairshop.com/collections/cloud-game-store/products/game-boy-dmg-original-high-quality-replacement-battery-contact-terminals?variant=37893135794348) [MGB](https://retrogamerepairshop.com/collections/cloud-game-store/products/gbp-game-boy-pocket-high-quality-replacement-battery-contact-terminals?variant=37893131305132) [MGL/CGB](https://retrogamerepairshop.com/collections/cloud-game-store/products/game-boy-color-high-quality-replacement-battery-contact-terminals?variant=37508302799020) [AGB](https://retrogamerepairshop.com/collections/cloud-game-store/products/gba-game-boy-advance-high-quality-replacement-battery-contact-terminals?variant=37893117411500)
 
* **Speaker does not work but headphones do**
  
    * **The speaker itself may be bad:** You can test this by desoldering the speaker and measuring the resistance across the contacts with a multimeter. You should get 8 ohms on a good speaker. Anything else (or open circuit) means a bad speaker. You can also just try a known good speaker instead. Do note that in most cases, the electrolytic capacitors in the console may have also gone bad and it is a good idea to service those at the same time or else a replacement speaker may also die.

    * **The headphone jack is dirty or bad:** Every Game Boy headphone jack has a [physical switch](https://imgur.com/Q34epck) that is actuated by inserting headphones. When this switch is open circuit, the Game Boy switches the internal speaker off. You may have luck just trying to clean the headphone jack or you may have to bridge the circuit or install your own switch. The jack may be replaced but a donor would need to be sourced as this is a custom part.

    * **Corrosion or other liquid damage:** Neither the jack nor the speaker is bad. On Game Boy Color consoles in particular, corrosion in the headphone jack area is common and this can cause a broken connection between the headphone jack and the rest of the system. This will manifest in a perfectly working switch when tested with a multimeter but the console will still not work properly. Diagnosis and repair must be done trace by trace by checking both sides of the PCB simultaneously.
