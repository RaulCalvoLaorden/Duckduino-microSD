# Duckduino-microSD
Interpreter that runs on an arduino, decodes and executes ducky script on a microSD card.

## Benefits Over Alternatives
Once the arduino has been programmed, you need only deal with ducky scripts on a microSD card. No reprogramming the arduino to change scripts!

## Setup

(modified)

Import Library [FingerprintUSBHost](https://github.com/keyboardio/FingerprintUSBHost) (Download .ZIP and import in Arduino IDE: Sketch -> Include Library -> add .ZIP library )

## Keep in mind...
Long lines of strings may crash the arduino due to taking up too much RAM, if you have a line "STRING ..." over 300 characters then split it into separate lines of strings, this won't affect how your script runs, it just reduces how much of your script is held in memory at any one time.

I have seen some ducky scripts that put hyphens (-) in between keys to be pressed simultaneously eg."CTRL-ALT DELETE". Note that when using duckduino-microSD you must not use hyphens and instead just use spaces eg."CTRL ALT DELETE"

The following duckyscript features are not yet implemented: DEFAULT_DELAY, REPLAY. This project uses arduino's inbuilt <a href="https://github.com/arduino-libraries/Keyboard/blob/master/src/Keyboard.h">keyboard.h</a> library, any keys not implemented in that will not work with this. eg: PRINTSCREEN.

This has only been tested on the following <a href="https://www.amazon.co.uk/Micro-Adapter-Reader-Module-Arduino/dp/B00NNDBIRK">microSD module</a>, I'm sure others will work, though no guarantees.
