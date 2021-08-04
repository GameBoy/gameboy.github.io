---
layout: wiki

title: Game Boy Common Issues
category: Wiki

---
All of these issues are covered in the [full wiki page](repairs) (most with more info) but this is just a quick document to detail the most common issues.
 

## **Game Pak Problems**

Bootleg spotting: [Check out this visual guide](gamechecker) or even the /r/gameverifying [wiki](https://www.reddit.com/r/gameverifying/wiki/index)

* [How to replace a battery in a Game Boy cartridge](https://www.youtube.com/watch?v=n3FsANHj300). If you use the "tape method" you will be shunned and made fun of, simultaneously. Solder and a tabbed CR1616 (must for GBA games) or tabbed CR2025/CR2032 are required. 
   
* [Garbled or incomplete Nintendo logo](https://i.redd.it/7n5f50urdy821.jpg) or corrupt or missing sprites in Pokemon
	* How do I fix it? 
	 * Check another game. If multiple games do this, the issue is with your console. Check your mods and ensure there are no shorts or [clean the cart reader.](https://www.youtube.com/watch?v=y-gE7t9Mk3w)
	 * Check another Game Boy. If the cart fails to boot on that too, [try following these steps.](https://www.youtube.com/watch?v=0gqNEyQLecQ).

## **Common problems**

* **Power LED flickers, low battery light comes on early or intermittently, or the console randomly resets** are all issues caused by a dirty or faulty power switch. [Switch will need to be opened and cleaned.](https://www.youtube.com/watch?v=G946mQCkIQc)

* **Game Boy won’t power on**
 
    * On an unmodded console, the most common issue is a **dirty or damaged power switch** and can usually be fixed by cleaning out the switch. See above.
 
    * If that doesn't fix the issue, another common one, especially on consoles that have been disassembled are **blown fuses.** To test your fuse, a multimeter is usually needed. Most Game Boys have two fuses, usually marked “F1” and “F2” on the main boards. Usually one fuse is connected to the power jack (Charging port in SP and Micro systems or DC jack on CGB and MGB systems) and the other is connected to the battery inputs. Some have had success by bridging the fuse with a wire or solder, but if something is still shorted, you will likely irreparably damage your system. Note that the “power jack fuse” in pre-GBA Game Boys is actually a diode being used as a fuse. Please see [this (WIP) list of Game Boy components](https://docs.google.com/spreadsheets/d/17RfgOaR-P8M0cC5BojwuY52GbZUefLFm82To7ja963o/) to find the proper replacement fuse. 
	
    * **Damaged DC power jack** in Game Boy Pocket and Game Boy Color systems can make the console appear dead. To test this, you'll need to test the console on DC power instead of batteries. If it works like normal, the jack itself could be bad. Like the headphone port, the DC jack in these two consoles also has a physical switch that goes open circuit when the power plug is inserted. The easiest fix is to remove the jack entirely and just bridge the proper connections (pins 2 and 3). Leaving the jack and bridging the connections simultaneously will also work but may be dangerous as it will then be connected in parallel to any batteries that are inserted in the console. Alkaline batteries can explode. 

    * **Bad battery or battery connector** in some models can cause issues. In models that came with rechargeable batteries (SP and Micro), the battery may need replacement. A new section of this wiki will be added soon with more detail on good choices for these consoles. On alkaline models, the connectors can get dirty. You can sometimes just spin the batteries in place to get them working but actually cleaning the contacts is the batter solution. Corrosion can be removed with distilled white vinegar, otherwise the contacts can be cleaned with isopropyl alcohol or electrical contact cleaner. 
 
* **Speaker does not work but headphones do**
  
    * **The speaker itself may be bad:** You can test this by desoldering the speaker and measuring the resistance across the contacts with a multimeter. You should get 8 ohms on a good speaker. Anything else (or open circuit) means a bad speaker. You can also just try a known good speaker instead. Do note that in most cases, the electrolytic capacitors in the console may have also gone bad and it is a good idea to service those at the same time or else a replacement speaker may also die.

    * **The headphone jack is dirty or bad:** Every Game Boy headphone jack has a [physical switch](https://imgur.com/Q34epck) that is actuated by inserting headphones. When this switch is open circuit, the Game Boy switches the internal speaker off. You may have luck just trying to clean the headphone jack or you may have to bridge the circuit or install your own switch. The jack may be replaced but a donor would need to be sourced as this is a custom part.

    * **Corrosion or other liquid damage:** Neither the jack nor the speaker is bad. On Game Boy Color consoles in particular, corrosion in the headphone jack area is common and this can cause a broken connection between the headphone jack and the rest of the system. This will manifest in a perfectly working switch when tested with a multimeter but the console will still not work properly. Diagnosis and repair must be done trace by trace by checking both sides of the PCB simultaneously.
