---
layout: wiki

title: Game Boy Repairs
category: Wiki

---
Last Content Revision: 2020-07-26

Game Boys are old and getting older. There are some common problems that many systems have, or some more specific to one model. It is highly recommended that any issues with the system be fixed before installing mods. Keep in mind that these suggestions are just guidelines and are by no means requirements for fixing issues. 

[Feel free to start here for the most common issues (which are also listed below).](commonissues)

There is also a section (directly below) on common issues related to specific Game Paks such as garbled "Nintendo" logos or battery related issues. 
 
# Contents

* [Games](#games)

* [Common issues that affect multiple systems](#common)

* [Original Game Boy (DMG)](#dmg) 

* [Game Boy Pocket (MGB)](#mgb) 

* [Game Boy Color (CGB)](#cgb)
 
* [Game Boy Advance (AGB)](#agb) 
	
* [Game Boy Advance SP (AGS)](#ags)

* [Game Boy Micro (OXY)](#oxy)
 
 
# Games
 
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



# Common

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



# DMG

## **Original Game Boy Problems**
 
* [Dead Vertical Lines on DMG](http://www.instructables.com/id/Game-Boy-DMG-Vertical-Line-Repair/)
 
* Screen Rot
 
  * What is it? With the classic Game Boy, screen rot can occur just about anywhere on the LCD. Sometimes it’s just a few small specs of black right in the middle of the LCD, sometimes it’s a whole corner of the LCD filled with black splotches. It is NOT mold or water damage, despite what some people will tell you.
  * How do I fix it? Unfortunately, there’s no known repair for this other than to just replace the entire LCD board. Unless you have legendary soldering skills, removing the LCD from the board will be quite difficult. 
 
* Vertical lines in the LCD
 
  * What are they? This is a VERY common problem with DMGs. These show up as missing vertical lines on the LCD. Sometimes if you press on the rubber strip below the LCD, you can get the lines to disappear for a short period of time.
  * How do I fix it? Fortunately, this problem is generally pretty easy to fix. See [here](https://www.youtube.com/watch?v=l4PArFarm_) or [here](http://www.instructables.com/id/Game-Boy-DMG-Vertical-Line-Repair/). One thing worth noting is that you should continue with the iron until you can briefly run the iron across the entire bottom of the LCD and the lines don’t show up anymore. You can get the lines to disappear but until you make sure they stop showing up with heat applied, it won’t be a long-lasting repair. 500° F / 260° C is an adequate amount of heat to use.
 
* Horizontal lines in the LCD
 
  * What are they? Not nearly as common a problem as vertical lines, but they do still show up every now and then. The problem is similar to vertical lines, but instead the lines show up horizontally across the screen.
  * How do I fix it? You will have to lift the LCD from its plastic bezel to gain access to the horizontal ribbon cable. This is a much more difficult fix than the vertical lines fix, but it can be done.
 
      * Remove the 2 screws holding down the vertical ribbon cable.
      * Carefully pry the LCD free from the plastic bezel using a plastic implement of some sort.
      * Prop up the LCD so you can access the horizontal ribbon cable with a soldering iron. The area of interest looks much like the area on the vertical cable underneath the rubber strip.
      * Gently run the iron back and forth across this area until the lines disappear. 500° F / 260° C is an adequate amount of heat to use.

* Splotchy circles in LCD (after backlight/bivert install)
 
  * What are they? Circles under the LCD that looks like trapped liquid. See [this image for an example.](https://i.redd.it/wsvc4e42n7u41.jpg) This phenomenon is called "Newtonian Rings" and is common in these circumstances. 
  * How do I fix it? The fix will involve either completely separating the glass LCD from the plastic polarizer layer (air gap) or completely joining them together (adhesive polarizer). See this video from /u/esotericsean for [a method of air gapping the polarizer.](https://www.youtube.com/watch?v=-6_s_kNVT0o) If you want to join the polarizer to the LCD OEM style, you'll need a polarizer with pre-applied adhesive. Air gapping is the preferred method. This also applied to Game Boy Pocket. 



# MGB
 
## **Game Boy Pocket Problems**

Don't forget that [the common problems section](commonissues) also has more info, such as failure to power on or speaker issues. 
 
* Lost game saves
 
  * What is it? Game saves become corrupted after playing in modified MGB consoles. The original power regulator in the console has difficulty supplying an adequate amount of power for both the console and the mods (e.g. back light) when the batteries start to run low and such the game begins drawing current from the SRAM battery backup instead of the cartridge slot. This will corrupt saves or delete them entirely if the battery is depleted.
  * How do I fix it? For the most part, installing a lithium ion battery will help to resolve the power delivery issues as the voltage supplied is quite a bit higher and more consistent but the best solution is to install a 5v voltage regulator for the cartridge slot. The voltage regulator should be able to handle low voltages if your console is still using AAAs but [it should be wired directly into the cartridge slot](https://i.imgur.com/tYBwzmL.png).
 
* Flash carts do not work
 
  * What is it? Flash carts like the EverDrive will crash the system while loading a ROM. This is caused by the same issue as the corrupted save issue above and has a similar remedy. Basically, the flash cart draws more current than the system can provide
  * How do I fix it? While a lithium ion battery may curb the save related issue, this issue requires a separate voltage regulator to be installed. [The wiring is going to be the same](https://i.imgur.com/tYBwzmL.png) and the system will maintain full compatibility with all OEM carts afterwards.

* Splotchy circles in LCD (after backlight/bivert install)
 
  * What are they? Circles under the LCD that looks like trapped liquid. See [this image for an example.](https://i.redd.it/wsvc4e42n7u41.jpg) This phenomenon is called "Newtonian Rings" and is common in these circumstances. 
  * How do I fix it? The fix will involve either completely separating the glass LCD from the plastic polarizer layer (air gap) or completely joining them together (adhesive polarizer). See this video from /u/esotericsean for [a method of air gapping the polarizer.](https://www.youtube.com/watch?v=-6_s_kNVT0o) If you want to join the polarizer to the LCD OEM style, you'll need a polarizer with pre-applied adhesive. Air gapping is the preferred method. This also applied to the original Game Boy (DMG). 
  
 
 
# CGB 
 
## **Game Boy Color Problems**

Don't forget that [the common problems section](commonissues) also has more info, such as failure to power on or speaker issues. 
 
* [Game Boy Color Speaker Replacement](https://www.youtube.com/watch?v=oTU46y6HnrA)

* Do note that speaker failures are often accompanied by the capacitors failing. See [this video and the description](https://www.youtube.com/watch?v=hD1J6rPH40E) for more information. 




# AGB
 
## **Game Boy Advance Problems**

Don't forget that [the common problems section](commonissues) also has more info, such as failure to power on or speaker issues. 
 
* Cannot load games after AGS-101 screen install
 
  * What is it? The Game Boy will freeze upon booting and will refuse to load any games after installing a backlit LCD (AGS-101). This is caused by the metal shielding on the back of the LCD making contact with the pins on the cartridge connector on the front of the motherboard.
  * How do I fix it? Simply add some insulating material between the LCD and the motherboard itself. A small piece of electrical tape is usually enough to physically separate the components.
 
* Game Boy Advance power LED is always RED even on new batteries or LED will flicker
 
* Game Boy Advance will restart randomly or if jolted
 
  * What is it? Both of these issues are usually caused by the same problem. The power switch on the console tends to accumulate dirt and gunk and will make poor contact. This will result in your Game Boy getting worse battery life and it will significantly decrease the reliability.
  * How do I fix it? You'll need to clean or replace the power switch. Please see the "Common Problems" section for more info.
 
 
 
# AGS
 
 
## **Game Boy Advance SP Problems**

Don't forget that [the common problems section](commonissues) also has more info, such as failure to power on, speaker issues, or battery issues.
 
* One or both shoulder buttons do not work
 
  * What is it? When pressing either the L or R button, sometimes or always the input is not registered by the console. Like the power switch, the buttons internally tend to gather dirt and gunk and no longer make electrical contact when actuated.
  * How do I fix it? The console will need to be disassembled and the switch cleaned or replaced. Replacement switches can be sourced on places like Mouser, Digikey, or RetroModding, but usually cleaning the button is sufficient. Occasionally the buttons can be cleaned without disassembling by soaking in rubbing alcohol or electrical contact cleaner (please allow sufficient time to dry before reassembly), but disassembling the switch or replacing it entirely may yield the best results.
  
* Game Boy Advance SP power LED is always RED even on new batteries or LED will flicker
 
* Game Boy Advance SP will restart randomly or if jolted
 
  * What is it? Both of these issues are usually caused by the same problem. The power switch on the console tends to accumulate dirt and gunk and will make poor contact. This will result in your Game Boy getting worse battery life and it will significantly decrease the reliability.
  * How do I fix it? You'll need to clean or replace the power switch. Please see the "Common Problems" section for more info.
  
* When charging the console, the charge light does not come on at all
  
* When charging the console, the charge light only comes on for a second before turning off

  * What is it? These two problems are a symptom of greater issues. In most cases, this issue requires disassembly and soldering to repair. 
  * How do I fix it? If the light does not come on at all, double check that your charger works. If you do not have another console to test it with, try picking up a cheap USB charging cable for only a few dollars. You can find them on aliexpress or ebay or from your usual parts places. If the light comes on for a second and then shuts off, the first thing to check is the battery. If you have a multimeter, check to make sure the voltage on the battery is over 3.4 volts. If it is under 3 volts, recycle the battery and purchase a new one. If it is over 3 volts, you likely have another issue but the console will not boot unless the battery is at least 3.4 volts. If you do not have a multimeter, you can try to purchase a new battery but do be aware that the aftermarket cells are usually only 400-700 mAh despite what they may claim. If neither of these fixes resolve your issues, then you'll have to disassemble to console.
    * If neither a new battery or another charger helped, you'll need to take apart the console. Before you do any further troubleshooting or repairs, first check for any signs of water damage on the PCB. If the water indicator sticker (should be on the bottom of the PCB near the power switch) is tripped (appears solid red or pink or is missing entirely) or if you see any corrosion or other signs of water damage, you may wish to take pictures and consult help. If nothing else, take pictures first before cleaning the corrosion as the corrosion will likely only be in areas connected to circuits you may have trouble with. 
	* If there are no signs of water damage, here are some steps you can take to narrow down and finally repair the issue.
	* It has been observed that a common ingress of water into the console is from the front speaker grill. Due to where the cart reader sits on the board, water that makes its way in from there can become trapped and cause localized corrosion. The path of the charge circuit runs directly next to the speaker hole so it is easy for liquids to get trapped and those traces to get compromised. You can use a multimeter to probe continuity from D1 to F2, if you identify a break in the line a jumper wire between any suitable points in between may resolve the issue with the charge circuit. There may be additional components between D1 and F2 based on the board revision you are looking at, please refer to [Gekkio's AGS schematic of the AGS-CPU-11](https://github.com/Gekkio/gb-schematics/blob/master/AGS-CPU-11/schematic/AGS-CPU-11.pdf) and do your own visual inspection of the traces on your board to confirm if there are any further breaks that require repair.
	  * If the charge light does not come on at all and you've ruled out the power adapter or the charge light comes on for a second and turns off and you've ruled out the battery, the issue may be the port itself or the EM8 filter near the charge port. You'll need to perform a visual inspection of the port itself and the PCB around the port for anything that looks off. If you do not see any obvious issues, you'll need to plug in the console while you have it disassembled and try and trace the power lines from the port with a multimeter. If you see power at the port and no where else, you should try to reflow the solder on the pins. To narrow down if the issue is with EM8, typically one can just apply pressure to the component (with your fingers) and plug the console in with a battery. If the console charges normally in this case, [you may need to reflow the solder connected to EM8 or replace it entirely.](https://www.youtube.com/watch?v=O03_c7dS_8U) Feel free to take clear pictures and ask around on [discord](https://discord.gg/gameboy) or reddit if you have questions.
	  * If the charge light does not come on at all and you've ruled out the power adapter, the issue may be with the component F2. F2 is a small surface mount fuse located near the link port on the back of the PCB. With your multimeter, check and see if you have continuity across the component. If not, you'll need to replace this fuse. [Check out this (WIP) spreadsheet for the P/N and spec of a replacement fuse.](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/) Do keep in mind that fuses are safety devices and they only ever blow to protect the system from faults. If your fuse does not have continuity across it, that means it has blown due to a fault. You need to ensure that the fault is cleared before replacing the fuse or the next fuse will blow too. If you opt to bypass the fuse instead of replacing it and your system develops a fault, you could destroy your system entirely with no hope of repair. F2 typically blows when there is a short across the charge port or if there is a fault with the charger itself. 
	  * If the charge light comes on for a second and shuts off and you've already ruled out the battery, this could indicate a blown fuse. Does your console boot normally? If the console does not boot on a known (or at least assumed) good battery, you'll need to check the component F1. This is a surface mount fuse and it is located on the front of the PCB right underneath the A and B buttons. With your multimeter, check and see if you have continuity across the component. If not, you'll need to replace this fuse. [Check out this (WIP) spreadsheet for the P/N and spec of a replacement fuse.](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/)
	* If none of this helped, congrats, you have a unique issue. Try posting on discord or reddit for help (with good pictures). 
	
* Shell is cracked or broken in multiple places

  * What is it? The shells of some late model AGS consoles are made with defective plastics that tend to get extremely brittle over time. This issue seems most prevalent with Pearl Blue AGS-101 consoles but may affect Graphite AGS-101 consoles or other late model units. [See this imgur album](https://imgur.com/a/dhfax) for more information. 
  * How do I fix it? Well, unfortunately, there is know currently known fix for this issue. If the console is already broken, you can try to glue it back together but the structural damage to the plastic has already been done and this will likely be temporary at best. The only way to "fix" this is to reshell the console in either a new aftermarket shell or with a salvaged OEM shell from another SP. 
 
 
# OXY 
 
## **Game Boy Micro Problems**

Don't forget that [the common problems section](commonissues) also has more info, such as failure to power on, speaker issues, or battery issues. 

* Faceplate does not clip in or does not stay clipped in when installed. 

  * What is it? The plastic frame of some Game Boy Micro consoles are made with defective plastics that tend to get extremely brittle over time. This issue seems most prevalent with Silver colored consoles but may affect or other units as well. [See this imgur album](https://imgur.com/a/dhfax) for more information. 
  * How do I fix it? Well, unfortunately, there is know currently known fix for this issue. If the console is already broken, you can try to use double-sided tape or other adhesives to hold the faceplate on but the structural damage to the plastic has already been done and any fixes will likely be temporary at best. The only way to "fix" this is to replace the front internal frame of the console with a salvaged OEM frame from another console.
