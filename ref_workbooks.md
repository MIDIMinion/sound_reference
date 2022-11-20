# Workbook Reference Info

## Overview
1. console input patch
2. console output patch
3. rio/stagebox patch
4. speaker schedule
5. mic schedule
6. IP schedule
7. QLab output patch
8. dante patch
9. cue list
10. mic tracking (musicals)
11. instrument assignment by song (musicals)


### 1 - [console] input patch
* divided into banks of 8 channels
* columns:
	* channels
		* which channel/fader is the signal on?
	* description
		* what is the signal?
	* source
		* where does the signal get into the console?
	* routing
		* where is the signal going inside the console?
	* details
		* DCAs, mute groups, processing

### 2 - [console] output patch
* divided by mixes/matrices/stereo/mono
* columns:
	* mix/matrix/bus
		* which fader is the signal on?
	* description
		* what is the signal?
	* Output
		* where does the signal get out of the console?
	* destination
		* what does the signal go to downstream of the console?
	* delay (ms)
		* is there delay? how much?

### 3 - [location/purpose] rio patch
* page split in half vertically between inputs & outputs
* columns:
	* channel
		* which input/output?
	* description
		* what is the input/output?

### 4 - speaker schedule
* speaker number
* make
* model
* amplifier
* position
* pan
* tilt
* details
	* horizontal spread angle

### 5 - mic schedule
* mic number
* make
* model
* instrument
* location
* notes

### 6 - IP schedule
* device name
* device type
* interface
* IP address
* subnet mask
* note

### 7 - QLab output patch
* number
* cue output
* output name

### 8 - dante patch
* looks like dante controller
* dante receivers
* receiver number
* dante transmitters
* transmitter number

### 9 - cue list
* act
* scene
* page
* cue
* effect/description
