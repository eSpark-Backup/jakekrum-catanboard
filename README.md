# Jake krum - Settlers of Catan Board
The scope of this project is to develop a product that facilitates an LED driven experience for Settlers of Catan Board Game. The product should be battery powered and should be capable of powering up to 195 WS2812B RGB LEDs.

The product will comprise of 2 x PCBs that will be referred throughout the course of development as:
1. Master PCB
2. Secondary PCB

## Requirements
### Master PCB
* Necessary chips to work as an Arduino Uno. The MCU should support Arduino IDE and programming via single MicroUSB connector. This means providing USB-UART feature on board. It is also required to expose the SPI headers for additional debugging purposes.
* Ports that will allow for hot-swappable connection between this PCB and the ones that will be powered from it. This essentially means JST port that can connect to the secondary PCB.
* Electric capability to power 195 WS2812B LED lights.
Lithium Ion battery IO for charging, and with enough voltage and capacity to run the whole system for at least an hour. The battery chemistry and size are not final and depend on the final recommendation / negotiation between contractor and customer.
* A port or set of soldering pads (TH) for a latching on/off switch to be easily installed.
* A port or set of soldering pads (TH) for a charging port to be easily installed.
* A port or set of soldering pads (TH) for a battery monitoring product. There will be 2 x soldering pads given after the latch circuit.
* Ports or soldering pads (TH) for (5) momentary push buttons to be easily installed and individually addressable.
* A port or set of soldering pads (TH) for (1) latching switch to be easily installed and individually addressable.
* Overall size should not exceed 3.5" x 3.5", though the battery and other buttons will be wired separately so this size limit only pertains to the PCB itself. There is a little bit of leeway with this sizing which can be discussed.

### Secondary PCB
* It will feature 2 x JST ports 3-pin on either sides for IN and OUT connections forming daisy chain and will simply have 3 WS2812B LED lights in the center.
* Size of the PCB will be 1.5" short diagonal x 1.7" long diagonal hexagonal PCB.
