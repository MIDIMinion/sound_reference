# Networking - Reference Notes

Here is a quick guide to switch configuration for each switch model. Networking is complex, and there are a lot of caveats to each particular setup.
Please use this as a checklist to help get the essential things complete, and not as the only way to configure a switch. Proceed with caution.


## Shorthand
*IPv4 Address
  *IPv4 Addresses are composed of 4 octets, separated by decimals for a total of 32 bits. Each octet can contain up to 255 values from 0-254.
* Subnet Masks
  * It's common to see subnet masks referred to as a number like /16 or /24. This refers to how many bits are masked
      */16 would be equivalent to 255.255.0.0
      */24 would be equivalent to 255.255.255.0


## Cisco SG350
This information is pooled from my(Ryan Cooper's) discoveries, guides from friends, and online resources [Shure's guide to SG350 setup for dante](https://service.shure.com/s/article/configuring-sg350-switch-for-shure-devices-and-dante?language=en_US&region=en-US)

* Before we begin
  * This guide assumes that your switches are managed on the VLAN 1009 with a management IP Range of 192.168.9.0/24.
  * If you have a simple network, it may be best to leave the shop preset file and use that. If you do, consult with the shop's technical department to make sure the base config supports what you're doing.
 
* To Start
  * It's good practice to create a base config that contains IGMP, QOS, and VLAN settings then copy that to all switches and change switch-specific settings like name, and port assignment per switch.
  * First start by defaulting the switch to clear out any shop default settings. Use a paper clip to hold down the reset button for 15ish seconds till all the switch lights flash. The switch will take a few minutes to come back up in factory default state. If the switch is not reachable after reset, it may need a power cycle. 
 
* Making a base config
  * Connect to the switch via port 2 and go to the switch IP. The Default Cisco SG series IP is 192.168.1.254/24.
  * Enter the default user name and password, or the shop-assigned one.
   * UN: cisco
   * PW: cisco
  * Enter a new user name and password
  * Change the management IP: 
   * In VLAN Management:
    * Make VLAN 1009
    * Make port 1 on the switch untagged on VLAN 1009.
   * In Administration>Management Interface>IPv4 Management and Interfaces Submenu, IPv4 Interface:
    * Add an interface on VLAN 1009, at the desired switch IP within the 192.168.9.0/24 subnet. Once you hit ok you will no longer be connected to the switch.
   * Connect to port 1 and set your computer's interface IP to one compatible with the new switch IP. Connect to the switch at it's new address.
   * Set all switch ports to be VLAN 1009. This means that any port not set to another VLAN will be a management port.
    * NOTE: This is not the most secure way to do this, but allows for ease of setup. This guide is not for network security.
  * Disable Green Ethernet
   *  
