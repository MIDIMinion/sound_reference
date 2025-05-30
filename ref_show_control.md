# Show Control - Reference Notes


## General Notes
* Organize show control between departments as early as possible, certainly before shop prep/load in
* have a dedicated chunk of time between QT/focus and the start of tech to have all the departments sit down and try out the show control system

## OSC 

### Ports
* QLab: 53000
* Go Button: 53100
* Galileo 616: 15006

### General Notes
* If you're using unmanaged switches, wherever possible, have a dedicated OSC network
    * non-OSC operations (like screen sharing, file sharing, etc) should happen on a different network. It doesn't take long to max out your gigabit switch when moving files and video around
* have as few hops through switches as possible
* when QLab triggers lights via OSC, send messages as a different user than the board op. Otherwise, your OSC commands will clear the command line
    * Evan Cook suggests: /eos/user/99/cue/{your target cue list here}/{your target cue number here}/fire

### Triggering QLab from Eos via OSC
* don't
* but if you must:
1. in the lighting console, set the primary console's ethernet port to the same IP range and subnet mask as the QLab machine
	* i've found that setting the lighting console to be the highest possible IP of all of the OSC devices is helpful
2. set the transmit IP to X.X.X.255
	* this IP will broadcast to all addresses in the IP range
	* **note:** as of Eos 2.8, you can add multiple IP addresses to the transmit IP field, separating them with a space
	* Prior versions of Eos may need to use a third party application like OSC Router
3. set the transmit port to 53000
* also: "Implicit OSC Output"
* read up in EOS manual on "OSC Filter Out"
4. in the Eos OSC Setup menu, find "OSC Cue Send String"
	* this is basically a custom string you can have eos send with every "fire"
5. enter the string "/cue/%1/start"
	* %1 acts as a variable to send the cue number of the fired lighting cue in the OSC string
	* other variables are available:
		* %1 - cue number
		* %2 - cuelist number
		* %3 - cue whole number only (i.e. if it's cue 17.5, send only 17)
		* %4 - cue point number only (i.e. if it's cue 17.5, send only 5)
		* %5 - cue label
		* *courtesy of [ETC](https://tinyurl.com/45awbhfa)*
		* there's more good info [here](https://tinyurl.com/3ft3d45h)

##### Clearing out Junk OSC from EOS
* [Eos Family Console Forum](https://tinyurl.com/uf6bex4w)
* [EosSyncLib](https://tinyurl.com/uzmr3mw)
* /eos/filter/add
	* eos will only send OSC messages to the device that matches the filter
	* ex. /eos/filter/add=/eos/out/param/\*
		* eos will only send OSC messages to this device that start with "/eos/out/param/"
	* QLab syntax is /eos/filter/add "/cue/\*"
		* QLab uses a space (" ") wherever Eos uses an equals ("=") to attach argument tags to the OSC string
* /eos/filter/remove
	* remove an existing filter
	* ex. /eos/filter/remove=/eos/out/param/\*
* /eos/filter/clear
	* clear all filters, so that the device will receive all filters from Eos

### Galileo 616
* port: 15006
* Mute Outputs:
	* /output/1/mute 1.0
	* /output/1-10/mute 1.0
	* /output/1,3,4/mute 1.0
* Unmute Outputs:
	* /output/#/mute 0.0

### Galaxy 816 (Normal Mode)  
* port: 25004
* Mute Outputs:
	* /processing/output/1/mute 1
	* /processing/output/([1-9])/mute 1 and another cue that says /processing/output/(1[0-6])/mute 1
* Unmute Outputs:
  	* /processing/output/1/mute 0
* the galaxy assumes that any values sent to it via OSC are in sample rates at 96kHz.
	* if you're trying to set delay times, multiply the value in ms you WANT by 96. the resulting number is the value (in samples) that should be sent to the galaxy
		* ex. 80ms * 96 = 7680 (send this value to galaxy)
### Galaxy 816 (Spacemap Go Mode)  
* port: 38033
* the Spacemap System IP configuration matters a great deal in a Galaxy system that includes a Galaxy in Spacemap mode. If your Galaxies are 10.0.1.20,.21,and .22, the Spacemap System IP Configuration should end in .23, not .19. If you are responsible for a future system that includes Galaxies in Spacemap mode, contact Meyer in advance to learn current best practices.

### wave tool
* port: 50035
* Ip address must be computer running wave tool main license. Cannot trigger OSC message on client computer 
/wtchat/QLAB/{dest} "message"
*{Dest} can be All or name set in preferences* 

## MIDI

### Weird MIDI Encounters
* console sending Note messages into a midi solutions thru, then into two MIDI Sport 4x4's for main and redundant QLab rigs. Backup rig was receiving a different Note message than the main rig. Swapping the USB A>B cable on the backup rig's MIDI sport seemed to fix the problem

## Devices that can power MIDI Solutions Quadra Merges
* CL3/CL5 consoles

### JL Cooper MLA's
* these can only be used in transmitting/receiving pairs
	* the MLA converts MIDI to a different serial protocol/signal type before transmission. the receiving MLA converts it back to MIDI
	* Note On/Off messages will appear as control change messages without the receiving MLA

### MIDI Control of the Lexicon PCM90
* recalling a specific preset in a specific bank is as follows:
	* two midi cues need to be fired at the same time:
		* control change message where the control number is 32 and the control value is the number of the bank you want to recall
			* 0-4: Program Banks 0-4
			* 5-6: Internal register bank R0 & R1
			* 7-11: reserved for ROM Card Banks
			* 12-...: memory card banks
		* program change message where the program # is the preset you want to recall
			* note that the program number is 10x of what the preset # is. so preset 4.2 is program 42
	* Example: recall bank: P0 preset: 4.2
		* control change: Ch # | 32 | 0
		* program change: Ch# | 42

### Timecode
* LTC2: smpte ltc wave file generator
	* https://elteesee.pehrhovey.net/
* Owen Meadows' [Timecode / Music Sync Point Calculator](https://tinyurl.com/4n85x484)
	* used to find the timecode and/or standard time value of a given measure and beat in a score
* Owen Meadows' [Timecode / Score Mapping Calculator](https://tinyurl.com/mrynd4uf)
	* used to find the timecode and time standard value at chosen markers in a piece of music
