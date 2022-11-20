# Go Button - Reference Notes

## OSC Replies
* If you want Go Button to send OSC replies for every OSC message:
	1. set the UDP port in Go Button to 53000
	2. from your QLab device, send the OSC message "/alwaysReply #" where # can be 1, 2, 3, or 0
		* a value of 0 will turn off always replay

## thump loop
1. make a cue list to house the thump cues
2. first cue is the thump
3. second cue is a wait cue
4. third cue is a restarts the group cue, making in the whole thing run on a loop for whoever long the wait value is