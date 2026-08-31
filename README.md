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
