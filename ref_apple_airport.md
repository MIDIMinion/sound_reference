# Apple Airport Extreme Notes

## Factory Reset
1. Make sure that the base station is connected to power.
2. Press and hold the reset button for about 5 seconds, until the status light on the base station flashes amber rapidly. Then release the button.
3. Wait about a minute for the base station to finish restarting.
4. Open AirPort Utility, which is in the Utilities folder of your Applications folder.
5. Click the Other Wi-Fi Devices button, then select your base station from the list. Click Edit.
6. Click the Other Options button.
7. Click ”Restore previous settings,” then click Next until you get to the final window.
8. When AirPort Utility indicates that setup is complete, click Done.

## Setup
* under the "Internet" tab:
	* set the IPv4 Address to what you want the WAP's LAN Address to be
	* set the Router Address to what you want the WAP's Lan Address to be
		* assuming you want this WAP to act as your network's router
* under the "Network" tab:
	* set the Router Mode to DHCP
	* define the DHCP range
		* it's good practice to keep the range as small as possible, to support only slightly more addresses than the number of wireless devices you plan to connect
* click "update" to confirm your settings