# Howtos

## Hardware
* Hacking the 43" Medion Life 17932 (MD31206) Ultra HD Smart-TV | [see howto >>](./hacking_medion_life_X17032_MD_21206.md)
* HP t620 bios update | [see howto >>](./HP_T620_Bios_update.md)

## Proxmox
* Building a cheap proxmox cluster | [see howto >>](./cheap_proxmox_cluster.md)
* Proxmox hints and tweaks | [see howto >>](./proxmox_hints_tweaks.md)

## Manjaro / Arch
* Manjaro microcode fix | [see howto >>](./manjaro_microcode_fix.md)
* Install Brother HL-L2300D printer on Manjaro / Arch | [see howto >>](./install_brother-hll2300d_printer)

## Data
* Calender dates scraping -> .ics calendar file | [see howto >>](./calender_dates_scraping_to_ics_file.md)

## Java
* Domesticate Eclipse IDE | [see howto >>](./domesticate_Eclipse_IDE.md)

## Shell

### searching files and sort by date
```bash
find path -printf "%T@ %Tc %p\n" | sort -n | grep name
```
