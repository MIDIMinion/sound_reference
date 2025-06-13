# Yamaha MRX7-D - Reference Notes

## Basics
* Control happens over the Dante Primary port
* Default IP address: 192.168.02
* Use Provisionair Designer to build your processor file
* Use Provisionair Controller to build a control interface
* Use Provisionair Kiosk to _run_ your control interface
    * ohmygod Yamaha, what if it wasn't 3 pieces of software?!
* Pay very close attention when you're syncing to the processor
    * Unless you're updating a change in your project file, you really should be syncing from device to computer
* _save often!_

## What to do when it crashes
1. Pray that you have a recent save of the project file AND your Dante patch
2. Unplug the processor from the Dante network and follow instructions to initialize it:
    1. (this is where I'll put those instructions)
3. After you initialize the processor, connect your control computer directly to the Dante Primary port on the back of the processor
4. Establish a connection using Provisionair Designer and your project file
5. Sync from computer to device
6. Pray a second time
    * Maybe try a diety that you haven't prayed to before
7. If all seems happy, disconnect the control computer from the processor, and then put the processor back on the Dante network
8. Load a saved Dante preset for the processor
    * Initializing the processor breaks Dante subscriptions, so you'll need to go through an re-sibscribe

## Notes about laying out the internal processor
* put meters on your inputs and outputs - this is going to help you later on when trying to troubleshoot signal flow
    * you can then also put these into the visual/control layout for Provisionaire Control/Kiosk