# CB1-setup
Steps I take after flashing the btt cb1 os image to an sd card as of Sep 13 2022

1. Flash the OS Image from [here](https://github.com/bigtreetech/CB1/releases)
2. Set the wifi information in /boot/system.cfg
3. Expand the ext4 root partition to take up the rest of the SD card
4. Set a new hostname by editing /etc/hostname
5. Change the mirrorlist away from china for faster speeds in /etc/apt/sources.list (I chose deb.debian.org)
6. Rename the default biqu user `usermod -l toyvo biqu`
7. Move the user home directory `usermod -m toyvo -d /home/toyvo`
8. rename the user's group `groupmod -n toyvo biqu`
9. Set a password for the user `passwd toyvo`
10. Disable root login `passwd -l root'
11. Update the system `apt update && apt upgrade -y`
