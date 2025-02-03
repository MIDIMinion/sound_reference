# Networking - Reference Notes

Here is a quick guide to switch configuration for each switch model. Networking is complex, and there are a lot of caveats to each particular setup.
Please use this as a checklist to help get the essential things complete, and not as the only way to configure a switch. Proceed with caution.


## Shorthand
*IPv4 Address
  *IPv4 Addresses are composed of 4 Octets for a total of 32 bits. Each octet can contain up to 255 values from 0-254.
* Subnet Masks
  * It's common to see subnet masks referred to as a number like /16 or /24. This refers to how many bits are masked
      */16 would be equivalent to 255.255.0.0
      */24 would be equivalent to 255.255.255.0


## Cisco SG350
This information is pooled from my(Ryan Cooper's) discoveries, guides from friends, and online resources [Shure's guide to SG350 setup for dante](https://service.shure.com/s/article/configuring-sg350-switch-for-shure-devices-and-dante?language=en_US&region=en-US)

* Before we begin
  * This guide assumes that your switches are managed on the VLAN 1009 with a management IP Range of 192.168.9.0/24.
 
* Making a base config.
  * It's good practice to create a base config which contains
