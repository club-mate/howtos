# Proxmox hints and tweaks

# 1. allow more than 1 backup of VMs

I just ran into a problem with my Proxmox installation. I wanted to create a new backup of a VM, but Proxmox refused with
```bash
ERROR: Backup of VM 102 failed - only 1 backup(s) allowed - please consider to remove old backup files.
```
* solution: Datacenter/Storage - option is called 'Max backups'
