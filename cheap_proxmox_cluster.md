# howto build a cheap proxmox VE 6.x cluster (work in progress)

## Hardware Nodes
as mentioned in this [Howto](./HP_T620_Bios_update.md), the **HP t620 thin client** is a smart little box with enough power to make a virtualized homelab reality.
### inside
* 4 x 1,5Ghz AMD APU 
* up to 32GB DDR3 RAM with 1600Mhz (mostly comes with 4GB)
* 2 x internal USB 2.0 Ports (which I use to power the SSD Sata drives)
* 1 x Mini PCI-expres Slot for e.g. an 2-Port Sata-Adapter (in this example) or wifi card (normally)
* some t620s come with an extra mSATA slot but not in the newer versions
### on the front side
* 2 x USB 3.0 Port
* 2 x USB 2.0 Port
* Audio in/out
### on the back side
* 2 x USB 2.0 Port
* 1 x 1 GBit onboard Network 
* 2 x DisplayPort 
* 1 x VGA
* Audio in/out ???
* PS/2 ports for oldschool keyboard/mouse
### price
* **55€** ~ **65€** on eBay

## peripherals
my recommended peripheral parts list for one node:

* 1 x M.2 SSD for the proxmox node system (mostly they are sold with M.2 16GB SSD), I have 128GB installed | around **13-18€** (eBay)
* 2 x 8GB DDR3 RAM 1600Mhz SO-DIMM | around **25€** each (eBay) = **50€** per node
* 1 x Mini PCI-E to 2-port Sata Adapter for e.g the CEPH shared filesystem | around **8$** (aliexpress)
* 2 x enterprise SSD with power loss protection, e.g Samsung 160GB around **28€** each (eBay) = **56€** per node
* 2 x USB 2 SATA Power Cable | around **4€** each (eBay) = **8€**
* 2 x 1GBit USB3.0 LAN Adapter | around **7$** each (aliexpress) = **14$** per node

## cluster
* for learning and testing purposes, just install 2 virtual nodes on one physical node
* if you want to try building a HA Cluster with dedicated network for CEPH, you need 3 x HP t620 thin clients connected in a circle with 2 x 1GBe USB3.0 Adapters (the t620 has 2 USB3.0 Ports on the front) on each node

## price
* alltogether this projekt cost me around 200€ per node

## contributing
if you want to share your expierience or thoughts, feel free to pull a request

## more details coming soon ...

## [<< go back to HOWTO'S](./README.md)
