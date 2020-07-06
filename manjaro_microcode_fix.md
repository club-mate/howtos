# manjaro microcode fix (spectre-meltdown)

## check if microcode is installed
```bash
sudo dmesg | grep microcode
```
## install spectre-meltdown-checker
```bash
sudo pacman -S spectre-meltdown-checker
```
## check if you have vulnerabilitys
```bash
sudo spectre-meltdown-checker
```
## install intel microcode
```bash
sudo pacman -S intel-ucode
```
## configure grub with microcode
```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
## restart
```bash
sudo shutdown -r 0
```
## check again if microcode is installed
```bash
sudo dmesg | grep microcode
```
## check if you still have vulnerabilitys
```bash
sudo spectre-meltdown-checker
```

## [<< go back to HOWTO'S](./README.md)






