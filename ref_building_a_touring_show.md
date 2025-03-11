# Building a Touring Show - Reference Notes

## System Components
* FOH
* Mezz Rail
* [Towers & Tower Distros](#towers)
* Center Cluster & Truss
* [Front Fills](#front_fills)
* Onstage Foldback
* Offstage Foldback
* Ampland
* [Dimmer Beach/Dimmer Distro](#dimmer_beach)
* SM Call Desk
* [Fly Rack](#fly_rack)
* Offstage Sing/Chorus Racks
* [XO Rack](#xo_rack)
* [House Ties](#house_ties)
* PD/UPS Rack
* Gondolas
* Com/Vid Rack
* Drive/Amp Racks
* RF Racks
* Band Rack
* Player Boxes
* Player Bundles
* Radios
* Tech Com/Utility


## Common Bundles & Common Lengths
* FOH Bundles & Extensions - 250' + 50' Ext
* Mezz Rail Bundles & Extensions - 250' + 50' Ext
* Tower Bundles Far/Near & Extensions - 
* XO Bundles & Extensions - 
* Pit Bundle & Extension - 
* Player Bundles - 50'
	* typically 50' for most positions to get from the band rack to the players
	* any positions that could get remoted, such as drums or percussion, should have a duplicate "Long" version of the bundle that's 150'
* SM Call - 50' or 100'
* Fly Rack - 150'
* Deck/Auto - 150'
* Offstage Sing/Chorus Far/Near - 25' or 50'
	* should carry video and program (or a special mix) for any offstage singing moments
	* Near should come off of ampland (Com/Vid rack)
	* Far should come off the XO rack
* Dimmer Bundles - 50'
	* ideally, you'd have a dimmer distro that sits on the dimmer racks to service all of your over stage needs
	* this can either run directly to ampland, or through the XO rack/bundles
	* be prepared for dimmer beach to land up on a jump while the XO rack lives on the deck - 100' version of the dimmer bundles
	* plan for DMX or LX network bundles in these, for things like cue light relays, show control gateways, and stand light dimmers that may live in your racks
* House Ties - 50'
* LX Op - 50'
	* this seems long, but sometimes they end up in a booth away from FOH
* Tech Distro Near/Far - 100' and 150'
	* supports any tech table needs
		* Com
		* Timecode/Show Control
		* Video/VOR
		* Program
* SD Tech - 100'
* PSM Tech - 150'
	* there's an argument to be made for using your PSM connections at ampland for PSM Tech connections, because the PSM will never be at both of those positions at the same time
	* however, there's great value in being able to test/troubleshoot your PSM call desk ahead of preview flips




## Common Boxes
* FOH Bundles
	* also contains mezz rail bundles, if they fit
* Mezz Rail Support
	* carries MD Blackout monitors and a mezz rail distro, if one exists


## Lil Tricks
* Mezz Rail - build the mezz rail bundles so that the moving light programmer com/video can come off that bundle
	* makes tech flips for previews really fast
* Front Fills - purchase 2" webbing long enough to span the apron of your stage (50'-60'), and use this to spike out your front fill placements
	* add a center mark to line things up
	* if you want to be nice, you can spike out lighting's foot light positions as well

## Towers & Tower Distros <a name="towers"/>
* typically come in 3 sections; Top, Mid, Bottom
* some will have boat clamp style latches, some will have bolts
* Tower Distros
	* instead of trying to wedge a rack or two into the bottom section of a tower, plan for the distro racks to live upstage of the fire curtain, just offstage of the proscenium
	* Make the tower section bundles longer so they can run offstage to the distro
		* Top Section: 75' - 100' (50' might be just too short if your tower is 20' tall)
		* Mid Section: 50'
		* Bottom Section: 50'
	* this also lets you get to the distro rack without going onstage
	* makes the apron look much cleaner
* Tower Near/Far
	* since ampland can end up on either side of the stage, depending on the venue, using "Near" and "Far" in relation to ampland, is a clear distinction of where a tower bundle (or tower distro) needs to go
	* at the drive/amp rack and towers, you'll still want to distinguish betweekn SL Tower and SR Tower


## Front Fills <a name="front_fills"/>
* ideally, should get fed off the tower distros
	* combo cable/NL4 running out to each speaker is ideal, unless daisy chaining
* if you have a stage deck, then landing the front fills on top of the apron is the fastest/easieest option for placing front fills
* if you don't have a stage deck, then be prepared to hang the speakers off the lip of the apron
	* ask the shop for hangers for your speakers
	* these would get lagged to the deck off the stage, and then the speaker hangs off the edge of the apron, over the pit
	* if the shop doesn't have hangers, look for hardware on mcmaster-carr

## XO (Crossover) Rack <a name="xo_rack"/>
* the XO rack's purpose is to provide a location to patch into/out of your system other than ampland, and is typically located on the opposite side of the stage from ampland
* ideally, each signal type/system within the rig should be represented here:
	* control networks/dante
	* com
	* video
	* utility audio
* for flexibility, the following bundles should be able to patch in either at ampland, or the XO rack:
	* PSM
	* House Ties
	* Fly Rack / Deck Auto
	* Offstage Sing/Chorus

## House Ties <a name="house_ties"/>
* this should carry your com ties, your house PA ties, and your program feeds
	* Com Ties
		* this should carry your com for Spots and House Lx
		* Spots typically get 2 channels (Spot Pvt, Spot SM) + Program
		* House Lx typically gets 1 channel (SM Lx)
	* House PA (House Drive)
		* between 4 and 6 channels of analog audio for tying into house delays, surrounds, clusters, etc.
		* these should already have matrices setup to make for quick and easy routing into those systems
	* House Program
		* Lobby Program
		* ALD Program
		* Dressing Rooms (page/program feed)
	* should be able to be pulled off ampland or XO rack
		* but unlikely both at the same time, so the "House Ties" connections at ampland can be where the XO bundle mult plug in, if your house ties are on the opposite side of the stage from ampland


## Interfacing with Lighting
* Cue Lights
	* lighting may want to put a DMX edison relay in one of your racks to handle FOH and MD cue lights
		* plan for DMX in all of your bundles between dimmer beach and wherever this relay lives (Dimmer Bundles, XO Bundles)
	* powercon for the actual cue lights (Pit Bundle and MD Bundle for MD cue light, FOH Power bundle for FOH cue light)
* MD Blackout
	* lighting will also need a way to toggle your Mezz Rail monitors between MD and a blackout shot
* Show Control
	* it's common for lighting to put show control gateways in sound racks, connected to the Lx network
	* plan for Lx Network cables to be put in bundles between Dimmer Beach and wherever these gateways live
* Mains, Backups, and Spares
	* Lx likes to run with hot backups
	* plan cable accordingly: 3 @ DMX/Ethercon for each run
		* Main
		* Backup
		* Spare
* Stand Lights
	* If you're feeling nice/have the space in your racks/bundles, then building powercon/edison into your player bundles for standlights will save time on a load in/out
	* be sure to *clearly* mark that these are dimmable power and **only** for stand lights
		* using outlet safety caps/childproof caps can help alleviate this
* VOR
	* they're gonna ask for it! might as well build it!
	* you'll need the FOH color shot embedded with program and SM call
		* if you're using timecode, they may also want that in the embedded video
	* if your video system is analog, plan for XLR lines to handle VOR input
	* talk to your production electrician in advance to see where they want to be able to tie into VOR
		* don't forget about preview flips - best to have a VOR tie in near FOH (maybe in the LX op bundle)

## Dimmer Beach / Dimmer Distro <a name="dimmer_beach"/>
* used for getting any signal to/from Lx truss
	* onstage/offstage monitors mounted in ladders or truss
	* cameras mounted in ladders or truss
	* hot power for cameras or IR emitters
* Lx is going to have big cable swags/picks coming off dimmer beach. this is the best place to have your overhead bundles/cable run, so a distro rack keeps things tidy

## Fly Rack <a name="fly_rack"/>
* tyipcally contains video and com, sometimes program
	* a com station with a speaker built in is nice, but not required
* usually sits near, or hangs off a pipe at, the fly rail. so the flypeople can see the stage/hear calls