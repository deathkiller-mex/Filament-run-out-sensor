# Filament-run-out-sensor (Klipper Only)

# IDEA

So I've had this idea for a while, which basically consists of making my own filament run-out sensor rather than buying one (yes, I'd rather tinker and spend a few hrs rather than buying a cheap one...), especially since this type of sensor is incredibly simple. My idea consists of something like this:

- |LED|F|Rec| -------> HIGH = Filament available
- |LED| |Rec| -------> LOW = Out of filament
Symbol meanings:

- Rec ----> IR Receiver
- F ----> Filament
- LED ----> IR (InfraRed LED)
- | ----> Hypothetical/possible wall

So with this setup, once the IR receiver senses the IR LED, the printer will take the signal and interpret it as, "Oh, there is no filament; let's stop the printer."


# Important note: this setup was designed and tested for the Ender V3 SE; every other printer except the KE pls scroll down to the "Other Printers compatibility."


# Wiring
There is no need for a cutom PCB or PCB or anything; you can just solder on the LED legs as follows:
<img width="502" height="562" alt="image" src="https://github.com/user-attachments/assets/0e5425e5-351e-4f97-948f-e4e5539a7be8" />

As u can see, the wiring is simple; the main thing is that for the cables (GND, DATA, VCC/+5V) u are going to need a lot of cable, enough to go from the bottom of the printer to the spool holder (Spoiler: the sensor will be located at the spool holder). Try to leave enough room for wire management so that they are not loose, causing them to get tangled with the printer.

DON'T CONNECT IT TO THE PRINTER JUST YET, SINCE AFTER SOLDERING U MUST FIRST PUT THE COMPONENTS ON THE ENCLOSURE!

# Enclosure & instructions

# Ender 3 V3 SE and KE:
<img width="1099" height="610" alt="image" src="https://github.com/user-attachments/assets/c4d66cb9-175d-427e-8abf-55f729a6e566" />

1. So once u have everything wired correctly, put the components inside the enclosure.
2. Insert the IR LED and the NPN into the holes (it doesn't matter where each one goes.
3. After that, grab ur hot glue gun and put some glue on the leds to make sure they dont lossen up and more glue at the cables and resistors (MAKE SURE THAT U CAN STLL PUT THE LID; IF U WANT U CAN FILL THE WHOLE THING UP, I DON'T RECOMMEND IT BUT IF U ARE GOING TO DO IT, ENSURE THE LID STILL FITS!!!)

<img width="550" height="305" alt="no lid" src="https://github.com/user-attachments/assets/3f03c4d0-6f87-4005-9eb5-8111bcda1747" />

5. NOW I WOULD RECOMMEND NOT PUTTING THE LID IN JUST YET, AND FIRST CONNECT EVERYTHING TO THE PRINTER SO IT IS EASIER TO TROUBLESHOOT.
6. Open the printer up. **Disconnect it!!!**
7. Here is the pinout (PLS VERIFY THE PINOUT IS CORRECT JUST IN CASE) 
<img width="338" height="311" alt="image" src="https://github.com/user-attachments/assets/b31d0cd7-abd3-4b5f-ae3a-cfa432e7abfb" />

**IGNORE THE 24V PIN; WE WILL NOT BE USING THAT ONE**
7. Now just follow the schematic and connect to each pin; you can use jumper wires with some silicone or a connector (I added the exact connector on the BOM).
* Quick NOTE: If you can't find the exact pin, it is labeled J12 near the green connectors.
8. Reassemble the printer.
8. Now go into the code file "Klipper config" and do the necessary changes to the printer to add the sensor and the pause config.
9. After doing the necessary changes, test the sensor and ensure both the config and the sensor work properly.
10. Once everything works properly u can put the lid on using super glue. It should look like this.
  <img width="1129" height="604" alt="image" src="https://github.com/user-attachments/assets/624118d4-64bb-4314-a374-2dba80ddb022" />
11. Finally, to secure the sensor, unscrew the filament holder, place the sensor, put the holder back, and screw it.
12. That's it. Enjoy!! :)

# Other Printers compatibility.

- If u have another printer besides the one above, the building process should be the same buuuuut you will need to download the parts labeled "Universal" in the CAD folder.
- To screw the sensor into the printer sheck the dimensions on the pic folder and find a spot where it fits. :/ sorry but idk or own other printers besides the Ender and SE.
- For wiring, look for similar ports to connect the sensor into (Most commercial sensors work a similar way, so what u can do is look for a sensor online and check where the manufacturer indicates to connect the sensor to).
- 💀💀💀IMPORTANT, PLS MAKE SURE UR PRINTER HAS AN INTERNAL RESISTOR LIKE THE ENDER V3 SE CAPABLE OF HANDLING THE SHORT!! What does this mean? Ensure your firmware activates the mainboard's internal pull-up resistor to handle the logic state safely.
- Also note that the connector might be different, so ensure u buy the correct one.
- Configuration changes should be universal, but ensure compatibility beforehand pls.


# BOM

Note on the BOM: all of these are recommended sellers; honestly, if u won't be using IR LED or NPN, go to ur nearby store and buy single components as this and most part lists online come in packs and u will only need one of each. With that in mind, the only thing I do recommend buying is at least 5M of wire since I estimate around 60cm to 1M to be used, so 5M allows for error made when cutting.

|Part|Amount|Price|Link|
|:-------:|:----:|:--:|:--:|
|IR LED 940nm and Q PHOTO NPN|1|$3.77|[Aliexpress](https://www.aliexpress.com/item/3256803143839703.html?spm=a2g0o.order_list.order_list_main.25.49f61802DPEsUi)|
|Cable|5M|$2.09|[Aliexpress](https://www.aliexpress.us/item/3256804149903490.html?spm=a2g0o.order_list.order_list_main.14.49f61802DPEsUi&gatewayAdapt=glo2usa)|
|JST-XH 2.54mm (4-pin)|1|$3.48|[Aliexpress](https://www.aliexpress.com/item/3256803495901819.html?spm=a2g0o.cart.0.0.401a7a9do6m4Tx&mp=1&pdp_npi=6%40dis%21USD%21USD%203.48%21USD%203.48%21%21USD%203.41%21%21%21%402101e7a317882918157682275e0ccf%2112000026787314843%21ct%21US%216359134517%21%211%210%21)|
|220 ohm resistor|1|$1.51|[Aliexpress](https://www.aliexpress.com/item/3256809104654732.html?spm=a2g0o.cart.0.0.401a7a9do6m4Tx&mp=1&pdp_npi=6%40dis%21USD%21USD%203.02%21USD%201.51%21%21USD%201.50%21%21%21%402101e7a317882918157682275e0ccf%2112000048633255432%21ct%21US%216359134517%21%211%210%21)|
|Aprox Total| |$11.52| |


