# Filament-run-out-sensor

# IDEA

So I've had this idea for a while, which basically consists of making my own filament run-out sensor rather than buying one (yes, I'd rather thinker and spend a few hrs rather than buying a cheap one...), especially since this type of sensor is incredibly simple. My idea consists of something like this:

- |LED|F|Rec| -------> HIGH = Fialment available
- |LED| |Rec| -------> LOW = Out of filament
Symbol meanings:

- Rec ----> IR Receiver
- F ----> Filament
- LED ----> IR (InfraRed LED)
- | ----> Hypothetical/possible wall

So with this setup, once the IR receiver senses the IR LED, the printer will take the signal and interpret it as, "Oh, there is no filament; let's stop the printer."









# BOM

|Part|Amount|Price|Link|
|:-------:|:----:|:--:|:--:|
|IR LED 940nm and Q PHOTO NPN|1|$3.77|[Aliexpress](https://www.aliexpress.com/item/3256803143839703.html?spm=a2g0o.order_list.order_list_main.25.49f61802DPEsUi)|
|Cable|5M|$1.61|[Aliexpress](https://www.aliexpress.us/item/3256804149903490.html?spm=a2g0o.order_list.order_list_main.14.49f61802DPEsUi&gatewayAdapt=glo2usa)|
|Aprox Total| |$8.14| |
