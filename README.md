# TrinketBootloaderRepair
From the Adafruit website


he ATtiny85 does not have a protected-bootloader section. This means its possible to accidentally overwrite the bootloader (or even if you unplug the Trinket while uploading it might have difficulties from then on)

You can use an Arduino UNO to re-program the bootloader onto your Trinket (or Gemma). This loader isn't tested to work with any other kind of Arduino.

Connect:
Trinket VBAT+ pin to Arduino 5V (or just power it via a battery or USB cable)
Trinket GND pin to Arduino GND
Trinket RST to Arduino #10
Trinket #0 pin to Arduino #11
Trinket #1 pin to Arduino #12
Trinket #2 pin to Arduino #13
On a Gemma, alligator clips work well. the Reset pin is underneath the MiniUSB Jack. You may have to solder a wire temporarily. Alternatively, sometimes you can just hold the reset button down while running the sketch (type 'G' to start) and it might work. Soldering a wire works best.

Then download, uncompress and run the Trinketloader sketch, pick the one that matches your Arduino version!


Uncompress and open in the Arduino IDE, select the UNO and serial port to the UNO Arduino board you are uploading too and upload it to the UNO.
Open up the serial console at 9600 baud and when it tells you do, press the miniature button on the Trinket (or Gemma) or type in G into the serial console and click Send

You should see the following, the fuses, firmware burned and verified! It will take 2 seconds
