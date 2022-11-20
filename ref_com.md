# Com - Reference Notes

## Checking Termination
1. using a multimeter, measure the resistance between pins #1 and #3 on one of the channel A XLR connectors
2. If the channel is terminated properly, then the resistance should measure approx. 4k ohms
	* a very high resistance indicates no termination
	* a resistance of 2K ohms indicates a double termination
3. repeat for other channels
4. check resistance between chassis ground and pin #1. Using an ohmmeter, measure the resistance from pin #1 on the mainstation or power supply to chassis ground.
	* the measurement should read 10 ohms
	* a high reading (over 100 ohms) indicates the 10 ohm resistor in the unit has failed and needs repalcement
		* failure to replace a failed resistor results in an audible buzz in the system
	* a reading of less than 10 ohms (or a short) typically indicates that the shell and pin #1 of the cable are shorte together

## Mic Gain Controls
The following beltpacks have individual control over mic gain:
* RS-602
    1) press and hold setup button until "P" is displayed
    2) press the A call button repeatedly I told the display shows "A"
    3) the A volume knob can be used to set the gain of the mic, with clockwise being louder and counterclockwise being quieter
    4) press the setup button again to save the settings to the beltpacks

## Tempest 2400 Basestation
* General troubleshooting
    * Take the whole tempest system, put it in a box, and throw it in the trash...
    * Wireless cutting in and out on a wired com channel can indicate a need to null the wireless basestation

## Clear-Com SB-704
* 10 channels on the back are self terminating
* channels 1-5 and 6-10 share a power rail, respectively. If you have an external PSU plugged into any channel in one of those ranges, the whole range of channels gets extra juice


## Repair Info
* MS-440
    * Talk button bulb: 5v 30mA radial bi-pin