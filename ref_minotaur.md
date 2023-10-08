# Minotaur - Reference Notes

*many of the notes in this section are echos of what's already been said in Daniel Lundberg's blog on minotaur, as well as the video of the livestream he did with TSDCA. If you're not able to access either of those, then hopefull these notes can suffice*

## Category, Method, Group
* Category - What is it?
	* amplifiers, cable, roadcases, perishables, etc
* Method - Where do we get it?
	* Rent, rent-major, buy, in house, etc
* Group - Where does it go?
	* Bundled Cable, FOH Rack 1, SL Speaker Tower, etc.

## Starting Fresh - Suggested Order of Operations
With your shiny new minotaur file, the world is your oyster to label! Here are some suggested steps to take that will hopefully set you up to keep your show's label database organized and easy to use:

1. Fill in your show info
	* go to the main menu (Cmd + 1) and click on the title above the menu tabs
	* this is where you can add your show name, logos, colors, designer names. everything you need to make your paperwork look super professional
2. Add your groups
	* groups are how you organize the equipment and cables in your system
	* the more detail, the better
	* some example groups might be:

	| group | what things in this group are/do |
	| --- | --- |
	| racks-foh com | all the cables & equipment inside the foh com rack |
	| racks-amp | all the cables & equipment inside the amp rack |
	| interconnects-ampland | all of the cables that connect one amp to another amp within ampland |
	| loose-band | all the cable that connects loose things in the band, sucha as microphones to stage boxes or headphones to avioms |
	| speakers-front fills | speakers and cables involved in front fills |
	| com-tech | cable and gak involved with tech com |
	| spare | spare stuff! |

3. Add your equipment and cable
	* this is where you take the equipment and cable that you've out in your shop bid and add it to minotaur under the "Equipment" tab. Two points of clarification:
		* the Equipment List is YOUR gear that you want to be making labels for to build your show
		* the Equipment Library is a list of possible equipment to add to your Equipment List
	* a good way to go about doing it is to go to the "Equipment Library", and searching for the model using Cmd + F
	* when you find the piece of gear you're looking for, click the + next to the record to add one or several to your equipment list
4. Review your equipment list
	* make sure you have all of your stuff!
5. Expand your equipment list
	* you've added 3 behringer X32's. weird choice, but now would be the time to specify which one is the FOH console, which one is the monitor console, and which one gets tossed in the dumpster
	* to do this, find the piece of gear in your Equipment List, click "Split", and give the pieve of equipment a useful description like "FOH Console" or "Dumpster Filler", and hit ok
	* DON'T FORGET TO PUT THINGS IN GROUPS!
		* now is where you specify that your "Band Rio" goes in the "racks-band" group, and your "FOH Rio" goes in the "racks-FOH" group
6. Build your cable labels *FROM* your equipment list
	* building cable from the equipment list can be slower and clunkier than just hitting Cmd + N in the cable menu, but it comes with the benefit of finding out if you haven't asked the shop for enough cable BEFORE you're at the shop
		* the second added benefit of this method is that once you've finished building all of your cable, what remains in your equipment list can be considered your spare cable
	* while you're building your cable labels, pay close attention to the following things:
		* does this cable need stek labels?
		* are my source/destination fields consistent and accurate?
		* should this cable be a mult?
		* do I have the correct tails in the mult? do they need to be stek'd tails? panels? stage boxes? baluns?
	* this is also the time to sort your cable into the groups you laid out earlier, making them easier to find as your list of cables grows and grows

## Tips & Tricks
* the cable that plugs into a rack/device that needs a stek label is where you should generate the stek label from
	* if a cable connects to FOH Rack, and needs a stek there, set the source/destination of the cable to "FOH Rack"
	* then, when it's time to print, putting "FOH Rack" in the field labeled "Device (Rack)" will print all the stek labels just for the FOH Rack
* Method 0
	* giving a cable/equipment a method of "0" will omit it from being printed on checklists

## Mult Splitting
mult splitting can save a lot of time if you have a lot of mults carrying the same lines on them

* example: lighting tech com where each com box chains out of the one preceeding it:
1. make a 6-pair mult called "\_LX Com"
	* remember to give it Method 0, so it doesn't get counted in checklists!
2. fill out the descriptions for the lines of the tail
3. make a 6-pair mult called "LD Com"
4. in the inspector window at the bottom of the page, click in the text box below "Split", and select "\_LX Com"
	* the tail line descriptions will populate with \_LX Main's line descriptions
	* if you select "Source", it'll split the mult "at the source" so they share the same desitination
	* if you select "Destination", it'll split the mult " at the destination" so they share the same source
5. fill in the remaining line labels
* mult splitting is also helpful if things change; updating the reference mult "\_LD Com" will also update any mults that are split off it



## Shortcuts
| Keystroke | Command |
|---|---|
| Cmd + E | delete |
| Cmd + S | split record (equipment lists) |
| Cmd + J | show all |
| Cmd + T | omit record from view |
| Cmd + up/down | cycle through pages in print preview |
| Cmd + I | inspector (color code is the first field) |
| Cmd + D | duplicate |
| Cmd + Shift + D | duplicate a number of times |
| Cmd + Shift + C | cables |
| Cmd + Shift + L | lines |
| Cmd + Shift + T | tails |
| Cmd + Shift + E | equipment list |
| Cmd + Shift + B | bundle list |
| Cmd + Shift + A | box list |
| Cmd + Shift + H | equipment history |

## File Structures
* a .mino file needs the following folders to exist in whatever directory it's in, in order to not throw a bunch of error prompts
	* Minotaur CAD Links
	* Minotaur Backup
	* Minotaur Previous Revisions


## Combining Equipment Libraries
*I'm still testing this, so proceed with caution, and remember to backup important documents*


## Colors!
| Color | RGB | Hex |
| --- | --- | --- |
| Aqua | 133, 220, 252 | 85DCFC | 
| Black | 8, 8, 8 | 080808 |
| Blue | 0, 35, 253 | 0023FD |
| Brown | 131, 66, 2 | 834202 |
| Chartreuse | 171, 206, 114 | ABCE72 |
| Green | 95, 163, 54 | 5FA336 |
| Grey | 205, 205, 205 | CDCDCD |
| Orange | 250, 136, 10 | FA880A |
| Pink | 242, 183, 208 | F2B7D0 |
| Purple | 156, 0, 236 | 9C00EC |
| Red | 251, 9, 17 | FB0911 |
| Sand | 220, 117, 125 | DCB17D |
| White | 255, 255, 255 | FFFFFF |
| Yellow | 254, 255, 40 | FEFF28 | 