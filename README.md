# Jake krum - Settlers of Catan Board
The scope of this project is to develop a product that facilitates an LED driven experience for Settlers of Catan Board Game. The product should be battery powered and should be capable of powering up to 195 WS2812B RGB LEDs.

The product will comprise of 2 x PCBs that will be referred throughout the course of development as:
1. Master PCB
2. Secondary PCB

## Requirements
### Master PCB
* Necessary chips to work as an Arduino Uno. The MCU should support Arduino IDE and programming via single MicroUSB connector. This means providing USB-UART feature on board. It is also required to expose the SPI headers for additional debugging purposes.
* Ports that will allow for hot-swappable connection between this PCB and the ones that will be powered from it. This essentially means JST port that can connect to the secondary PCB. [This](https://jlcpcb.com/partdetail/Jst_SalesAmerica-B3P_VH_LF_SN/C160316) is the selected JST connector.
* Electric capability to power 195 WS2812B LED lights.
Lithium Ion battery IO for charging, and with enough voltage and capacity to run the whole system for at least an hour. The battery chemistry and size are not final and depend on the final recommendation / negotiation between contractor and customer.
* A port or set of soldering pads (TH) for a latching on/off switch to be easily installed. The [latch switch](https://www.amazon.com/dp/B01N751TAW/?coliid=I3CWPAK9FYR0DM&colid=2Q13YGGRGO5Q0&psc=1&ref_=lv_ov_lig_dp_it) is a 5-pin having built-in LED as well. The connection diagram of the switch is updated below. The latch ON/OFF will be connected directly after the Power ORING.
* The battery will be connected using [this](https://jlcpcb.com/partdetail/Jst_SalesAmerica-B3P_VH_LF_SN/C160316) connector. The middle pin of connector will be marked NC.
* A port or set of soldering pads (TH) for a charging port to be easily installed.
* A port or set of soldering pads (TH) for a [battery monitoring](https://www.amazon.com/Battery-Monitor-Capacity-Indicator-7-4V-56V/dp/B07CPYRP4P/ref=sr_1_1?crid=2FZFWZBFW3JP4&keywords=2s+li+ion+battery+monitor&qid=1678826163&sprefix=2s+li+ion+battery+mon%2Caps%2C817&sr=8-1) product. There will be 2 x soldering pads given after the ON/OFF latch circuit.
* Ports or soldering pads (TH) for (5) momentary push buttons to be easily installed and individually addressable.
* A port or set of soldering pads (TH) for (1) latching switch to be easily installed and individually addressable. [This](https://www.amazon.com/dp/B01N751TAW/?coliid=I3CWPAK9FYR0DM&colid=2Q13YGGRGO5Q0&psc=1&ref_=lv_ov_lig_dp_it) switch will be used so it is advised to please add some switching capability since MCU will need voltage level translation in order to handle the LED on this switch.
* Overall size should not exceed 3.5" x 3.5", though the battery and other buttons will be wired separately so this size limit only pertains to the PCB itself. There is a little bit of leeway with this sizing which can be discussed.
* 3 x TH pads that expose UART interface of STM32 (default UART only). If it is being used by another pin, then route the other pin elsewhere. The 3rd connection will be GND.
* 14 x TH pads for additional 6 digital inputs. Add debouncing capacitors and pull ups like before which will consume 12 connections. Remaining 2 x connections will be 3.3V and 5V.

#### Wiring diagram for Power ON/OFF Latch Switch
![image](https://user-images.githubusercontent.com/76909080/225118530-95e954ac-022a-475b-be2d-a2b5d80a3fc5.png)

### Secondary PCB
* It will feature 2 x JST ports 3-pin on either sides for IN and OUT connections forming daisy chain and will simply have 3 WS2812B LED lights in the center. [This](https://jlcpcb.com/partdetail/Jst_SalesAmerica-B3P_VH_LF_SN/C160316) is the selected JST connector for both IN and OUT.
* Size of the PCB will be 1.5" short diagonal x 1.7" long diagonal hexagonal PCB.
