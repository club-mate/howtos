# HP T620 (not Plus) Bios update

The T620 is a nice little box e.g using it as a low powered home server.

* [Hardware Specs & Pictures](https://www.parkytowers.me.uk/thin/hp/t620/)
* [HP QuickSpecs (pdf)](https://www.bluechipit.com.au/media/product_spec/t620_thin_client.pdf)
* [CPU Benchmark](https://www.cpubenchmark.net/cpu.php?cpu=AMD+GX-415GA+SOC&id=2081) **AVG CPU Mark 1350** (the 4 x 1,5Ghz Version) *<- I recommend this version :-)*
* [CPU Benchmark](https://www.cpubenchmark.net/cpu.php?cpu=AMD+GX-217GA+SOC&id=2138) **AVG CPU Mark 707** (the 2 x 1,65Ghz Version)


## Bios update

### Download Bios update to your win pc
* [HP T620 Driver Downloads](https://support.hp.com/in-en/drivers/selfservice/hp-t620-flexible-thin-client/5404706)

### extract and start the program 
### choose usb methode
### put usb stick in your win pc and choose this usb stick
### put usb stick into usb port of your T620
### start T620 and press F10
### choose FLASH ROM Option in the first dropdown menu
### follow the instructions

### WARNING: Virtualization Option is hidden (not available anymore) in BIOS v.2.19
### before you install a system that needs AMD-V virtualisation e.g. proxmox, you have to check it with [HP BCU](https://ftp.hp.com/pub/caps-softpaq/cmit/HP_BCU.html) if its activitated and if not, activate it
### see also 
* [HP Troubleshooting Guide - Changing BIOS Settings from the HP BIOS ConfigureUtility (HPBCU) on page 48(40)](http://h10032.www1.hp.com/ctg/Manual/c04034585)
* [HP Forum discussion about deploying BIOS settings on T620 remotely with HPDM](https://h30434.www3.hp.com/t5/Business-PCs-Workstations-and-Point-of-Sale-Systems/BIOS-settings-configuration-via-HPDM/m-p/6674713)
