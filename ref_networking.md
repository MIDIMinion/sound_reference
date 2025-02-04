# Networking - Reference Notes

Here is a quick guide to switch configuration for each switch model. Networking is complex, and there are a lot of caveats to each particular setup.
Please use this as a checklist to help get the essential things complete, and not as the only way to configure a switch. Proceed with caution.


## Shorthand
* IPv4 Address
  * IPv4 Addresses are composed of 4 octets, separated by decimals for a total of 32 bits. Each octet can contain up to 255 values from 0-254.
* Subnet Masks
  * It's common to see subnet masks referred to as a number like /16 or /24. This refers to how many bits are masked
      */16 would be equivalent to 255.255.0.0
      */24 would be equivalent to 255.255.255.0


## Cisco SG350
This information is pooled from my(Ryan Cooper's) discoveries, guides from friends, and online resources [Shure's guide to SG350 setup for dante](https://service.shure.com/s/article/configuring-sg350-switch-for-shure-devices-and-dante?language=en_US&region=en-US)

* Before we begin
  * This guide assumes that your switches are managed on the VLAN 1009 with a management IP Range of 192.168.9.0/24.
  * If you have a simple network, it may be best to leave the shop preset file and use that. If you do, consult with the shop's technical department to make sure the base config supports what you're doing.
  * Make sure to SAVE SAVE SAVE. No changes you make will be saved to the startup config unless you hit save in the header or in file management. Sometimes the save won't come up in the header, reloading the page should bring it up.
 
* To Start
  * It's good practice to create a base config that contains IGMP, QOS, and VLAN settings then copy that to all switches and change switch-specific settings like name, and port assignment per switch.
  * First start by defaulting the switch to clear out any shop default settings. Use a paper clip to hold down the reset button for 15ish seconds till all the switch lights flash. The switch will take a few minutes to come back up in factory default state. If the switch is not reachable after reset, it may need a power cycle. 
 
* Making a base config
    * Connect to the switch and change the default UN and PW.
      * Connect to the switch via port 2 and go to the switch IP. The Default Cisco SG series IP is 192.168.1.254/24.
      * Enter the default user name and password, or the shop-assigned one.
        * UN: cisco
        * PW: cisco
      * Enter a new user name and password
    * Change the management IP:
      * In VLAN Management:
        * Make VLAN 1009
        * Make port 1 on the switch untagged on VLAN 1009.
      * In Administration > Management Interface > IPv4 Management and Interfaces Submenu, IPv4 Interface:
        * Add an interface on VLAN 1009, at the desired switch IP within the 192.168.9.0/24 subnet. Once you hit ok you will no longer be connected to the switch.
        * Connect to port 1 and set your computer's interface IP to one compatible with the new switch IP. Connect to the switch at it's new address.
   * Set all ports to management to have a base:
     * Set all switch ports to be VLAN 1009. This means that any port not set to another VLAN will be a management port.
     * NOTE: This is not the most secure way to do this, but allows for ease of setup. This guide is not for network security.
   * Disable Green Ethernet:
     * Navigate to Port Management > Green Ethernet > Properties
     * Disable "802.3 Energy Efficent Ethernet(EEE)"
     * In Port Management > Green Ethernet > Port Settings all ports should show disabled.
   * Disable Smart Port
   * Add VLANs as needed
     * In VLAN Management add VLANs as needed for your show.
   * Multicast
     * In properties enable "Bridge Multicast Filtering Status"
     * Use the drop-down to select each VLAN and change the forwarding method to "IP Group Address"
     * In IPv4 Multicast Configuration > IGMP Snooping
       *  Enable IGMP Snooping and Querier Status.
       *  For Each VLAN using multicast(XDIP, Dante, AES67 etc.)
         *  Select the VLAN and click edit.
         *  In the pop-up enable IGMP Snooping status, immediate leave, IGMP Querier status, IGMP Querier Election.
         *  Set IGMP Querier version to v2.
         *  Set Querier Source IP Address to Auto.
     *  In Multicast > IPv4 Multicast Configuration > IGMP VLAN Settings
       *  Enable IGMP Snooping and Querier Status.
       *  For Each VLAN using multicast(XDIP, Dante, AES67 etc.)
         *  Select the VLAN and click edit.
         *  In the pop-up change Router IGMP Version to v2 and Query interval to 30. Other settings can remain at default.
    * In Multicast > Multicast Router Port
      * Select each VLAN and ensure that all ports are set to none. This causes the switch to auto-detect a Multicast Router Port if you have additional switches.
      * Click apply if you change anything.
    * In Multicast > Forward All
      * Select each vlan and ensure that all ports are set to none. This prevents multicast from flooding all ports.
      * Click apply if you change anything.
    * In Multicast > Unregestered Multicast
     * Set all ports to forwarding. For a network without Video-over-IP devices set all to Forwarding. If you have video over IP devices: for more detail on this visit the Shure doc visited above.
   * QoS
     * Under Quality of Service > General > QoS Properties set the Qos Mode to Basic. Hit Apply.
     * Under Quality of Service > QoS Basic Mode > Global Settings set the Trust Mode to SDCP. Hit Apply.
     * Under Quality of Service > General > DSCP to Que
       * In the Table set DSCP 56 to Queue 8, DSCP46 to Queue 7, DSCP34 to Queue 6, all other values to 1. Hit Apply.
       * You can tab through these fields and use your numbers to set them fast.
   * SAVE.
   * In Administration > File Management save this config to your computer.
 
* Per Switch
  * File Upload 
    * Duplicate the text file on your computer and name it for your switch.
    * Connect to the new switch and change the UN and PW using the instructions above.
    * Open the file in text edit and change the IP address to the desired IP for the switch you will upload to.
    * Connect to the new switch and upload this switch file to the switch.
    * Wait for the switch to load this config up to 5 minutes, then connect to the switch.
    * Log into the switch at it's new IP and hit save.
  * In Configuration Wizards Menu run the "Getting Started Wizard".
    * Set System Location.
    * Set System Contact.
    * Set Host Name.
    * Don't change the switch IP Address or Password.
    * Set the Date and Time from the Local Machine.
  * Set Banners
    * In Administration set Login and Welcome Banners as desired.
  * Set Up Link Aggregation.
    * If you're using link aggregation, now is the time to set them up before you do any other port assignment.
    * Navigate to Port Management > Link Aggregation > LAG Management.
      * Hit Add.
      * Name the LAG and enable LACP.
      * Assign ports to the LAG.
  * Set port settings
    * In Interface Settings Submenu:
      * Set Trunk/Access configuration per LAG.
      * Set Trunk/Access configuration per port. You do not need to set anything per port for ports that are members of a LAG. Those can be left as is.
      * Assign VLANs to desired ports and LAGs as needed.
  * SAVE. It's a good idea to back up this config as well in case you need to swap a switch for a hardware issue.
   
