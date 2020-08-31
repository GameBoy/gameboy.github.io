---
layout: wiki

title: Game Boy Flash Carts
category: Wiki

---

There are three different styles of flash cart for Game Boy consoles, both for Game Boy (Color) and Game Boy Advance. Game Boy (Color) carts run on all models that can play original Game Boy games (so except the Game Boy Micro) and are used to run both Game Boy and Game Boy Color games. Game Boy Advance carts will only run on Game Boy Advance models and will only run Game Boy Advance Games. Even with a flash cart, you cannot run Game Boy Color games on an original Game Boy but a Game Boy flash cart will run Game Boy Color games on a Game Boy Color or original Game Boy games. For a more comprehensive list of known carts, please see [flashcartdb from insideGadgets.](https://flashcartdb.com)

**A note on bootlegs** 

Typically, hardware from insideGadgets or RetroStage or the like are designed to emulate OEM in hardware functionality and compatibility, however, most bootlegs work a little bit differently. Bootleg carts are built down to a price and to get them as cheap as possible, most use salvaged memory components or parts that otherwise are not suitable for this kind of use. One such example is that most bootleg Game Boy and Game Boy Color carts are built using parts designed for 3.3v systems and are then overdriven at 5v for use with the system. While this does not offer an risk of permanent damage to the console itself, this does make the cart use significantly more battery than it would otherwise. Additionally, this will reduce the usable life of the cart itself. 

Another issue, this one affecting both GB and GBA carts, is that the hardware typically only uses SRAM. As you know, SRAM requires power, either from the system itself, or from an internal battery, to maintain save data. The bootleg carts that ship with batteries typically have very poor life and last only a few months, even on a brand new battery. 

To overcome this issue, some carts have the game even further modified to copy the SRAM data to and from the flash chip that the ROM is stored on. This method does allow one to use SRAM without having to have a battery in the game but it is not without drawbacks. Because of hardware limitations, the the flash chip with the ROM cannot be read and written to simultaneously, so the game is designed to stop execution while saving so that the hardware may then read the contents of the SRAM and write to the flash chip. In most cases, this looks like the game itself is freezing when you save. Not too big of an issue but we're not done yet. 

There are two more considerations. This write operation to the flash chip takes even more power than just running the game and is extremely sensitive to interruptions. That means, if you save your game on low battery, there is a high chance of corrupting the write. Because the game is writing to the chip that the ROM data is stored on, a corrupt write will not just mean you lose your save data, it means you lose the entire game. And last, this modification is done on a per game and per cart basis so every game is going to be different. That means that these carts cannot be reflashed if you want to retain this functionality. You cannot dump one bootleg for flashing on to another unless they use the exact same version PCB with the same make and model flash and SRAM chips. 

Because of the behavior mentioned above, this also makes save data manipulation rather difficult. To back up a save on these carts, you would have to dump the entire ROM and then boot that dump in an emulator, load the game in that emulator, and then back up *that* save (and if you try and save while playing the dumped game in an emulator, the game will likely crash and not recover). Restoring save files is even more difficult as it requires dumping the ROM, rooting around in a hex editor until you find where the save is stored, and then overwriting the save within the ROM itself. Once overwritten, you then have to flash this modified ROM back to the cart. 

Most bootlegs can be flashed with normal Game Boy games as long as the game is compatible with MBC5 for Game Boy and Game Boy Color bootlegs or as long as the game is compatible with SRAM (and the cart has a big enough SRAM chip) for Game Boy Advance. Saving will work as expected on a normal cart as long as your bootleg game has a working save battery installed. 

# There are Three Types of ROM Carts

The three types are as follows, internal memory single ROM carts, internal memory multi ROM carts, and external memory multi ROM carts. 

# **Internal Memory Single ROM Carts** 

These carts imitate OEM carts in both form and function. They can only hold one game at a time, normally. Most common bootlegs are of this style. A recommended vendor for these style of carts (both GB and GBA) is [insideGadgets.](https://shop.insidegadgets.com/) These style carts often imitate or emulate OEM hardware. 

When considering a cart like this, there are often multiple things that need to be considered. Not all game hardware is the same and even then, some games are one-off custom as far as hardware goes. The vast majority of games are supported between all the aftermarket carts but there are still some that require OEM hardware to function (usually salvaged from another, less desirable game), or that just don't function at all (yet?) with aftermarket carts. 

**Game Boy and Game Boy Color**

For Game Boy and Game Boy Color, you need to consider which memory mapper the game you wish to use is supported. The vast majority of games either use or directly support the MBC5 mapper but there are some exceptions. A lot of older games use a MBC1 mapper which, depending on the specific game, may not be directly compatible with MBC5. There are patches for most of these games, however. 

Another consideration is going to be Real Time Clock support (RTC). The second generation Pokemon games in particular are popular choices with this feature. While this feature is not required for game play (between just not using certain aspects of the game and other game patches), it is only supported on the MBC3 mapper. Most higher quality flash carts are built for either direct MBC3 mapper support (with RTC) or for MBC1/5 emulation which should cover nearly every game. 

There are still some exceptions like the custom memory bank controller in the Pocket Camera, the HuC controllers, MBC6 and MBC7, the Wisdom Tree mapper, and so on but most of these games require additional hardware that is built into the cart and not currently usable with aftermarket cart hardware (at least, not without salvaging an OEM cart). There are also standard games that use a one-off controller, like the Japanese version of Pokemon Crystal which uses MBC30. 

**Game Boy Advance**

For Game Boy Advance carts, nearly every single game (aside from the NES Classics and Video series carts) uses the exact same mapper so that no longer needs to be considered. However, there are still some exceptions (namely the NES Classics or GBA Video series or games that have extra hardware like Boktai). With GBA games, you have to consider the save when choosing a cart. Most games can be patched to use a more common type of save (SRAM/FRAM) but some games do not play well with this behavior, especially if there is not enough SRAM available for the save data. 

SRAM is typically limited to 256K and some games store up to 1M. Games may be patched with [GBATA](https://digiex.net/threads/gbata-gameboy-advance-tool-rom-patch-into-remover-header-info-sram-save-patch.15059/) but YMMV. There are also extra considerations for extra hardware like RTC (Pokemon Ruby, Sapphire, and Emerald) or a light sensor (Boktai again) and insideGadgets carts do support these as long as you get the proper cart. Nearly all bootleg games are SRAM only (which is natively compatible with FRAM games but EEPROM and FLASH games must be patched) and there is not always a big enough save chip for all the data. 

# **Internal Memory Multi ROM Carts**

These carts usually have custom controllers in the hardware to allow the menu in the software to interact with the much higher memory that these carts come with. These are more common in bootlegs, e.g. 369in1 carts. Even though there is software that allows you to combine multiple ROMs for use with a single ROM cart, the distinction with these types of cart is the custom interface that allows the Game Boy to access more memory (though not all at once) than it would normally be allowed to. An OEM style cart with full compatibility will only allow up to 8MB of ROM on a Game Boy or Game Boy Color or 32MB on a Game Boy Advance (64MB for the video carts but those are non-standard). These carts have been known to map 2GB (though rarely is it every fully used). These are not recommended as every one works differently and not all of them work well. Long term reliability is often less than desired. 

# **External Memory Multi ROM Carts**

These are carts that use an external memory card, usually Micro SD, for the game and save storage. The hardware is not at all reminiscent of OEM games but it allows you to build and coordinate a library of all the games you want to play and is much more reliable than the internal memory versions. Common vendors for these types of carts are [Krikzz Everdrive (GB and GBA)](https://krikzz.com/store/), [EzFlash (GB and GBA)](http://www.ezflash.cn/), and [BennVenn's El Cheapo (GB only)](https://bennvenn.myshopify.com/collections/flash-carts)

