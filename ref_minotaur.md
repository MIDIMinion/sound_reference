# Minotaur - Reference Notes

### Shortcuts
* Cmd + E = delete
* Cmd + S = split record (equipment lists)
* Cmd + J = show all
* Cmd + T = omit record from view
* Cmd + up/down = cycle through pages in print preview
* Cmd + I = inspector (color code is the first field)
* Cmd + D = duplicate
* Cmd + Shift + D = duplicate a number of times
* Cmd + Shift + C = cables
* Cmd + Shift + L = lines
* Cmd + Shift + T = tails

### File Structures
* a .mino file needs the following folders to exist in whatever directory it's in, in order to not throw a bunch of error prompts
	* Minotaur CAD Links
	* Minotaur Backup
	* MInotayr Previous Revisions

### Making NL4 A/B Y Cables
* Cable Type Default Values
	* Cable Model: NL4 A/B Y
	* Source End: Male/Pins
	* Destination End: Male/Pins
	* Small Labels: 1
	* Mult Lines: 2
	* Add Lines: checked
	* Branch Cable Type: NL4
* leave all other values empty/unchecked
1. Make a new cable record and set the model to "NL4 A/B Y"
2. Add "destination tails" with a model of "NL4 > x2 NL2"
3. **steps for making sure the labesl print**
4. **renaming 1 & 2 to A & B**

### Category, Method, Grounp
* Category - What is it?
	* amplifiers, cable, roadcases, perishables, etc
* Method - Where do we get it?
	* Rent, rent-major, buy, in house, etc
* Group - Where does it go?
	* Bundled cable, FOH rack 1, SL speaker tower, etc.