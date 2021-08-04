---
layout: category
title: Consoles
---

Game Boys are old and getting older. There are some common problems that many systems have, or some more specific to one model. It is highly recommended that any issues with the system be fixed before installing mods. Keep in mind that these suggestions are just guidelines and are by no means requirements for fixing issues. 

[Feel free to start here for the most common issues (which are also listed below).](../wiki/commonissues)

There is also a section (directly below) on common issues related to specific Game Paks such as garbled "Nintendo" logos or battery related issues. 

Last Content Revision: 2020-12-16

# Contents

* [Games Problems and Repair](#games)

* [Common issues that affect multiple systems](#commonproblems)

* [Common mods for any system](#commonmods)

* [**Original Game Boy (DMG)**](gameboy) 

* [**Game Boy Pocket (MGB)**](pocket) 

* [**Game Boy Light (MGL)**](light) 

* [**Game Boy Color (CGB)**](color)
 
* [**Game Boy Advance (AGB)**](advance) 
	
* [**Game Boy Advance SP (AGS)**](advancesp)

* [**Game Boy Micro (OXY)**](micro)

* [**Other Game Boy Consoles**](others)

# games

## **Game Pak Problems**

This section only really applies to OEM Game Paks and has little bearing on bootleg or aftermarket hardware. [Check out this visual guide](gamechecker/) or even the /r/gameverifying [wiki](https://www.reddit.com/r/gameverifying/wiki/index) to find out how to spot bootleg hardware. 

* [How to replace a battery in a Game Boy cartridge](https://www.youtube.com/watch?v=n3FsANHj300). If you use the "tape method" you will be shunned and made fun of, simultaneously. Solder and a tabbed CR1616 (must for GBA games) or tabbed CR2025/CR2032 are required. 
    * Recommend using Panasonic tabbed cells. You can get [tabbed CR1616 cells](https://www.digikey.com/product-detail/en/panasonic-bsg/CR-1616-F2N/P273-ND/301860) and [tabbed CR2032 cells](https://www.digikey.com/product-detail/en/panasonic-bsg/CR-2032-F2N/P657-ND/2404062) from digikey or [tabbed CR1616 cells](https://www.mortoffgames.com/gameboy-color/repair-and-replacement-parts35/game-repair-parts39/cr1616-coin-cell-battery-with-tabs-panasonic-) from Mortoff Games. These are equivalent to OEM parts and were actually the OEM for some carts. 
    * If you're only doing one or two games, shipping costs can be prohibitive on the quality batteries. That's where the no-name tabbed cells come in. Search "tabbed CR1616" or whatever size battery you're looking for on ebay or aliexpress. You'll likely find a pack of several for the cost of one of the above. A lot of the stores listed on the main page also carry generic cells, including Mortoff Games. 
* Doing a replacement before the battery dies? Why not [back up the save first with one of the readers from the other section of the wiki.](https://www.reddit.com/r/Gameboy/wiki/cartreaders) It's probably not worth replacing the cell if it's less than 10 years old or more than 3.0v when measured in circuit with a multimeter. 
    * Game Boy and Game Boy Color games mostly used tabbed CR1616 cells with some notable exceptions like Pokémon Crystal which used a CR2025. All standard sized carts should fit a tabbed CR2032 sized battery with no issue or a CR2025. The bigger the battery, the higher the capacity.  
    * Note on GBA games -- the above process is identical but a tabbed CR1616 must be used and the games are secured by a tripoint screw instead of a game bit screw. If your game is not [one of the following on this list](https://gbatemp.net/threads/gameboy-advance-gba-games-requiring-batteries.322803/) it does not need a battery to save. If it has a battery anyway and is not on that list, it's likely a reproduction or bootleg cartridge. 
	    * Additional note on the Pokemon games, specifically Ruby, Sapphire, and Emerald. The battery is not required for saving but instead for the Real-Time Clock (RTC) hardware. Without this battery, certain in-game events will not work such as Shoal Cave tides or berry growing. If this battery is dead, upon starting the game, you'll get a message that ["The internal battery has run dry."](http://www.vbalink.info/img/matty/Emerald-1.png) but everything else (aside from RTC based events) should still work normally, including saves. 
		* Due to a quirk with the initilization of the RTC hardware, if you replace the battery in one of these games without deleting your save, your RTC still may not work despite the error message no longer occuring on the main menu. While not the exact same issue, the symptoms are identical to [the berry glitch](https://bulbapedia.bulbagarden.net/wiki/Berry_glitch) from Ruby and Sapphire (but it affects Emerald as well) but the fix is different. There are several different ways to fix this:
		    * Start a new game.
			* Use homebrew to edit the offset. The original Game Boy Advance version has been taken down as the original site was not maintained. It may be found by searching "rtcread.gba" ([or just clicking here](https://web.archive.org/web/20180811045454if_/http://furlocks-forest.net/wiki/uploadedfiles/rtcread.zip)) but otherwise [the software has been ported to DS as well.](https://sourceforge.net/projects/rtcread-ds/) Run the software on a DS or DS Lite with a SLOT-1 flash cart and the game you wish to fix in SLOT-2. From there, set the date to a date that is at or past the previous offset. The current date is usually a good bet. This is the least destructive method. 
			* Use the [pokemon-chest](https://gbatemp.net/threads/release-pkmn-chest-a-pokemon-bank-for-the-nintendo-ds-i.549249/) DS homebrew (will require dumping the save and running on a DSi or 3DS or running directly on a DS or DS Lite with an R4 or equivalent) [to reset the RTC.](https://gbatemp.net/threads/how-to-reset-the-rtc-in-gba-pokemon-games-after-replacing-the-battery.558620/) This is similar to the method above.
			* Dump your save and use [PKHeX](https://projectpokemon.org/home/files/file/1-pkhex/) or similar save editor to enable the clock reset flag and variable, flash your save back to the game, then boot the game and press L+B+Select on the title screen to use the official clock setting tool. 
			* Dump the save and use a hex editor to adjust [0x00A0 (the RTC value offset).](https://web.archive.org/web/20160409163543/http://furlocks-forest.net/wiki/?page=Ruby/Sapphire_Save_Data_Map) PkHeX may also be able to do this for you. 
			* There may be other methods and this guide will be updated when appropriate but any of the above methods are tested and will resolve the issue. Do note that some methods rely on changing the *software* value while others will change the *hardware* value. Do not change both or your issue will not be resolved. Pick one method only. A good way to ensure that things are working properly is to go to Littleroot town to check the current in-game time, participate in the Lilycove Lottery, wait until midnight, and try to participate again.
			
* Game does not boot -- This problem more commonly affects original Game Boy (Color) carts but may also affect Game Boy Advance carts as well. 
    * What is it? When starting a Game Boy console with a game inserted, the console freezes on the boot screen with a [garbled or incomplete Nintendo logo.](https://i.redd.it/7n5f50urdy821.jpg) Another manifestation can be if the cart does boot but seems to freeze on startup or intermittently. As a form of copy protection, the actual "Nintendo" logo is stored within the ROM of the game and read by the Game Boy when booting and compared to a copy stored internally within the Game Boy. If the console cannot read this logo, it does not boot the game. 
	* How do I fix it? Do not blow in your carts or your console ([this is what years of blowing looks like on the cart reader](https://i.imgur.com/UdeoFC8.jpg)). Simply remove and reinsert the game. If this does not help, the most common cause is dirty pin on either the cart, the console, or both. If cleaning the cart and the console does not resolve the issue, another common cause may be broken solder joints. [
BOBdotEXE sums up these troubleshooting steps nicely](https://www.youtube.com/watch?v=0gqNEyQLecQ).
	    * The cart may be cleaned without disassembly but disassembly does make the job easier. You may also take this opportunity to service the battery (if equipped) and to inspect for damage or corrosion. Recommended cleaning method is isopropyl alcohol on a cotton swab. Gently rub an isopropyl alcohol saturated cotton swab along the pins. Repeat with a fresh swab and more isopropyl alcohol until the swab comes away from the pins clean. 
		* If you can disassemble your cart, a better option for cleaning the pins is to use an artists eraser. Simply rub the eraser along the pins until they appear cleaned. Please see the above video for an example. 
		* The cart reader may be cleaned with [the official Game Boy cleaning kit](https://img1.etsystatic.com/054/0/9074196/il_fullxfull.732294003_55lg.jpg) but since you likely don't have one of those (not gatekeeping, they just didn't sell well and have been long since discontinued), there are also [third party options available.](https://www.retromodding.com/products/1upcards-game-boy-console-cleaner?_pos=7&_sid=1a99c71b0&_ss=r) Another good option is to use a credit card sized object wrapped in a cotton t-shirt or similar thickness lint free cloth and use that to clean the cart slot. Isopropyl alcohol may help this process, same as above. If using this method, always move in and out and never side to side else you risk damaging the pins. 
		* Visible damage or corrosion to the cartridge pins is a bad sign. It may be indicative of other issues but will need to be dealt with before moving on. If a gold finger is broken or disconnected, unfortunately, it's game over for that cart. You'll need to replace the PCB with a suitable donor, or, if applicable, [a new PCB.](https://github.com/HDR/NintendoPCBs) As long as the contacts are only damaged or dirty on the surface, they can be restored. 
		    * Light surface damage, corrosion, or other gunk that cannot be cleaned with isopropyl alcohol and a cotton swab can still be dealt with but will require more extreme measures. Sometimes, the contacts will need a good scrub but if that absolutely does not work, another option is a mild abrasive. This is only for visible issues. If the pins are visibly clean, do not polish them. Some people have reported success with Brasso or other surface polishing compounds, other people use a baking soda paste. When used very liberally, compounds like this generally will take off anything built up on the surface layer of the contacts without actually damaging the contacts. When using this, you only want to use up and down motions to polish, not side to side as this may clean the pins unevenly. Make sure you clean up afterwords with isopropyl alcohol or whatever your preferred cleaning solution. 
			* Do NOT use sandpaper. Ever. This will cause damage to the pins and create small crevices for dirt and other detritus to gather and will cause more issues in the long run. If you're going to do this anyway, no less than 2000 grit but higher is better. This is still a very bad option. The above option will work better even though it will take more time or supplies you don't have. There is no shortcut here. 
			* Soldering directly to the contacts is never acceptable **except** for data recovery purposes. Solder on the gold contacts is a bad idea for several reason, the first is that the solder will form a non-conductive oxide layer on the outside when subjected to repeated physical wear. Best case scenario means that you'll have to disassemble the cart and redo the contacts again with more solder. Worst case scenario is that the oxide layer will rub off onto the cart reader of your Game Boy and start causing issues reading ALL of your games. This is also why your cheap reproduction/bootleg cartridges with the silver pins need to be cleaned constantly or only work for a month or so.  
	    * Broken solder joints. Game Boy game PCBs are very thin at 0.9mm thick and, unfortunately, very flexible. Over the years, inserting and removing the cartridge will cause the PCB to flex a little and this will put stress on the solder joints. Eventually, this stress will lead to fractures and these fractures are just small enough to not be visible to the naked eye but big enough to cause electrical connectivity issues. While annoying, the solution is rather simple, albeit difficult if you're not experienced with soldering. You'll need to redo the solder on the pins of the MROM chip (the one on the lower right in most Game Boy cartridges) and potentially the MBC chip as well (the top left in most Game Boy cartridges). Removing the battery, if equipped, while resoldering is highly recommended. See the above linked video for an example on redoing the solder joints in the cart. Using flux will yield significantly better results. 
		    * When inspecting a cartridge for stress fractures, you'd have to do it with the game assembled and inserted into a console otherwise the PCB will not flex and the fractures will not be visible. Due to the optical properties (i.e. not invisible) of the casing and all Game Boys, this makes physical inspection nearly impossible. 

* Corrupt or missing sprites (especially in Pokemon RBYGSC)
    * What is it? When playing the game, ["large" sprites will appear with data missing (corrupt) or just as a black square.](https://www.reddit.com/r/Gameboy/comments/fxfnku/whats_wrong_with_oak/) This is especially apparent in the opening scene with Prof Oak or in Pokemon battles in the Pokemon games. Some games will use a portion of the save RAM to cache data and this issue occurs when the save ram is missing or otherwise not working properly. 
    * How do I fix it? Well, the most common fix is actually the exact same as the above fixes mentioned in the "game does not boot" section. Walk through the same fixes recommended there in order. Specifically, try cleaning the pins and if that does not work, you'll need to work your way up to touching up the solder joints on the SRAM chip (bottom left) and/or the MBC chip (top left). 
	
#commonproblems

## **Common problems**

Each section may have multiple subsections. If using this as a troubleshooting guide, one should work through the relevant section in order. For example, the most likely issue is listed first and the least likely issue is listed last or the easiest solution listed first with the most potentially destructive solution listed last. Working out of order can make troubleshooting much more difficult. 
 
* **Game Boy won’t power on** - The two most common problems that keep all Game Boys from powering on is faulty power switches or blown fuses. There is a third option on consoles with a barrel jack DC connector. 
 
    * **Dirty or damaged switches** can usually be fixed by cleaning out the switch. The most effective method to clean the power switch [is to disassemble the switch and ensure everything is clean from the inside-out.](https://www.youtube.com/watch?v=G946mQCkIQc) Less effective methods to clean the switch out are to spray contact cleaner inside the switch (or put a couple drops of rubbing alcohol), and simply work the switch back and forth. Make sure to let the switch dry out before turning it back on. Opening the switch is the most reliable and best solution but other methods may still help. The video example is for the AGB, but this process and issue applies to all models of Game Boy. 
 
    * **Blown fuses** are a bit harder to fix simply because of the tiny soldering required. To test your fuse, a multimeter is usually needed. Most Game Boys have two fuses, usually marked “F1” and “F2” on the main boards. Usually one fuse is connected to the power jack (Charging port in SP and Micro systems or DC jack on CGB and MGB systems) and the other is connected to the battery inputs. Some have had success by bridging the fuse with a wire or solder, but if something is still shorted, you will likely irreparably damage your system. Note that the “power jack fuse” in pre-GBA Game Boys is actually a diode being used as a fuse. Please see [this (WIP) list of Game Boy components](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/) to find the proper replacement fuse. 
	
	* **Damaged DC power jack** in Game Boy Pocket and Game Boy Color systems can make the console appear dead. To test this, you'll need to test the console on DC power instead of batteries. If it works like normal, the jack itself could be bad. Like the headphone port, the DC jack in these two consoles also has a physical switch that goes open circuit when the power plug is inserted. The easiest fix is to remove the jack entirely and just bridge the proper connections (pins 2 and 3). Leaving the jack and bridging the connections simultaneously will also work but may be dangerous as it will then be connected in parallel to any batteries that are inserted in the console. Alkaline batteries can explode. 
	* **Bad battery or battery connector** in some models can cause issues. In models that came with rechargeable batteries (SP and Micro), the battery may need replacement. A new section of this wiki will be added soon with more detail on good choices for these consoles. On alkaline models, the connectors can get dirty. You can sometimes just spin the batteries in place to get them working but actually cleaning the contacts is the batter solution. Corrosion can be removed with distilled white vinegar, otherwise the contacts can be cleaned with isopropyl alcohol or electrical contact cleaner. 
 
* Yellowing of the shell and/or battery cover
 
  * What is it? Over time, UV light, smoke, and general pollutants in the air will give your console a more yellowed appearance. The degree of this yellowing varies but most used systems have at least a little bit.
  * How do I fix it? With Retrobrite! Retrobrite is a solution you can make at home from easily sourced materials. There are tons of recipes and how-to videos on the internet about this stuff but if you want to KISS (Keep It Simple, Stupid!) Then follow [this](https://www.youtube.com/watch?v=3PImZt5km9s) video and you should get good results.
 
* Fuzz or static when using headphones
 
  * What is it? Sometimes when using headphones, you will hear crackling or static noise in the headphones. It is especially noticeable when twisting the plug in the jack. It’s a pretty rare problem but generally easy to fix.
  * How do I fix it? What you will need:
 
      * [QD Electronics Cleaner](https://www.homedepot.com/catalog/productImages/1000/6d/6d55c965-a581-4507-900a-aee92f61c94e_1000.jpg) -- found at Home Depot and most auto parts stores -- referred to generically as "contact cleaner" (not the stuff for corrective lenses, but the stuff for electronics)
      * Pipe cleaners -- found at some grocery stores and sometimes the Wal-Mart craft aisle
      * Spray the end of a pipe cleaner and stick it in the jack, moving it back and forth in the jack. This will clean the jack and help free any stuck parts in there. You also want to make sure that the headphone detect switch inside the jack gets a cleaning. 
  
  * This issue could also be caused by a dirty volume wheel (or slider on the SP, it's the same thing). You can try to clean the volume wheel by spraying contact cleaner inside it but for best, long term results, replacement may be required. 
  
* Speaker does not work but headphones do
  
  * What is it? No sound on Game Boy Pocket, Color, or Advance out of the internal speaker. 
  * How do I fix it? This is a complicated situation as this is a symptom of multiple different causes

      * The speaker itself may be bad: You can test this by desoldering the speaker and measuring the resistance across the contacts with a multimeter. You should get 8 ohms on a good speaker. Anything else (or open circuit) means a bad speaker. You can also just try a known good speaker instead. Do note that in most cases, the electrolytic capacitors in the console may have also gone bad and it is a good idea to service those at the same time or else a replacement speaker may also die. 
	  * The headphone jack is dirty or bad: Every Game Boy headphone jack has a [physical switch](https://imgur.com/Q34epck) that is actuated by inserting headphones. When this switch is open circuit, the Game Boy switches the internal speaker off. You may have luck just trying to clean the headphone jack or you may have to bridge the circuit or install your own switch. The jack may be replaced but a donor would need to be sourced as this is a custom part. 
	  * Corrosion or other liquid damage: Neither the jack nor the speaker is bad. On Game Boy Color consoles in particular, corrosion in the headphone jack area is common and this can cause a broken connection between the headphone jack and the rest of the system. This will manifest in a perfectly working switch when tested with a multimeter but the console will still not work properly. Diagnosis and repair must be done trace by trace by checking both sides of the PCB simultaneously. 
 
* Corroded Battery Contacts
 
  * What are they? Sometimes alkaline batteries will leak when left in systems for too long. Cheaper batteries tend to puke up their guts quicker. This will cause the nickel plating on the battery contacts to corrode, leading to a greyish/blue crust on the contacts.
  * How do I fix it? This depends on how far gone the contacts are. If there’s only a little bit of corrosion, you can use a Q-tip and a bit of vinegar and water and scrub the contacts with it. For more advanced cases, the contacts may need to be removed and soaked:
 
      * Use a tripoint screwdriver to open the case. This driver can be found on Amazon or from sites like [Handheld-Legend](https://handheldlegend.com/collections/dmg/products/tri-wing-screwdriver-for-nintendo-game-boy-original-color-advance-and-ds?variant=35317249155) or [Mortoff Games](https://www.mortoffgames.com/gameboy-original/repair-replacement-parts/system-repair-parts/triwing-security-screw-driver) though getting a full toolkit from [ifixit](https://www.ifixit.com/Store/Tools/Mako-Driver-Kit--64-Precision-Bits/IF145-299?o=4) or the like is not a bad idea either. 
      * Using a small screwdriver, press on the tab holding each of the 3 larger contacts (DMG, other systems only have one contact plate) in place and push down while pressing to push the contacts out of the shell.
      * Give them a bath in a 50/50 vinegar and water solution for about 15 minutes.
 
  If the nickel plating is eaten through, then the contacts will need to be replaced.
 
  [Kitsch-Bent](http://store.kitsch-bent.com/product/battery-contacts) sells some exact fit replacement contacts for the original Game Boy (DMG) and the Game Boy Color (CGB). The only issue is they’re plated with zinc. This means that you will have to take a bit of sandpaper and remove the zinc plating from the two PCB mount contacts where a solder joint needs to be made. Either that or set your soldering iron to 750 F to melt the zinc plating and hope you don't damage the board. Other than that, they’re great contacts which will last a long time.

* Speaker Wire Replacement
 
  If you need to replace the speaker wire, use 26 AWG stranded wire with PTFE or Silicone insulation. Solid core wire is not recommended as it will not bend easily to fit in the tight space allowed for the speaker.
  
  
The Game Boy community has one of the largest modding communities out of other retro gaming communities. Mods are simply any modifications to the Game Boy system to change it from stock. They can be simple or complex. The most popular modifications add light to the screens of the older Game Boy systems that relied on external light to be seen or even retrofit a newer screen into the console. Other popular mods include painting systems for a custom look, adding rechargeable batteries to systems that didn’t have it, clearing up the fuzzy sound, or even speeding up and slowing down games. Some modders want lots of mods in their systems, some only want one or two. Whatever your preference, there are a lot of experienced modders here on [discord](discord.gg/gameboy) happy to help when you run into trouble. For some of the more popular system specific mods, see below. Not all consoles are listed because not all consoles have mod kits available. Not all mod kits are listed either but submit a pull request ([here](https://github.com/GameBoy/gameboy.github.io)) to correct this. Some kits may have generic versions or may be acquired through less than legitimate channels. Where applicable, the legitimate source for these kits is what is listed.
  
#commonmods
 
## **Common Mods**

 Items in this section apply to all consoles or otherwise don't fit into one of the sections this page is split in to. 
 

* How to reverse shell discoloration (works also for clear consoles!) – [Instructables] (http://www.instructables.com/id/Retr0bright-how-to-turn-a-yellow-Gameboy-white-aga/)  
    * Works on carts too! – [Youtube](https://www.youtube.com/watch?v=s3uMlDgVbVw)

* Spray painting the console (there are many different ways of doing this, worth a quick google!) – [Written guide](https://www.reddit.com/r/customcontrollers/comments/583jv1/how_to_paint_a_custom_controller_a_step_by_step/)/[Step by step image guide](http://caseydmg.tumblr.com/post/38063928433/my-guide-to-painting-your-dmg-gameboy)/[Video Guide](https://www.youtube.com/watch?v=34I45k71Vys)  

* Spray painting clear consoles from the inside – same as normal but from the inside! [Here](http://imgur.com/gallery/92za8) is the inspiration! (credit to /u/kemakill)  

* LED in game cartridge – [Video Guide]( https://www.youtube.com/watch?v=CK7t0WsVTL8)  

* Tetris logo lit up on cartridge – [Step by step guide](https://www.reddit.com/r/Koji_Kendo/comments/69su2p/tetris_led_lit_logo_ver_2/)    

* Rechargeable game battery – [Step by step guide](https://imgur.com/a/Sn0U7)    

* Batteryless saving for original Game Boy games (SRAM -> FRAM) - [Thread with more info](https://www.reddit.com/r/Gameboy/comments/fe3tec/non_volatile_fram_replacement_for_game_boy_with/)

* Batteryless saving for Game Boy Advance games (SRAM -> FRAM, does NOT apply to Pokemon) - [Youtube video](https://www.youtube.com/watch?v=OUO6ohZbQbU)