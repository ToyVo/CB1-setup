# CB1-setup
Steps I take after flashing the btt cb1 os image to an sd card as of [v2.1.2](https://github.com/bigtreetech/CB1/releases/tag/V2.1.2)

1. Flash the OS Image from [here](https://github.com/bigtreetech/CB1/releases)
2. Set the wifi information in /boot/system.cfg
3. Set a new hostname by editing /etc/hostname
4. Change the mirrorlist away from china for faster speeds in /etc/apt/sources.list (I chose deb.debian.org)
5. Rename the default biqu user `usermod -l toyvo biqu`
6. Move the user home directory `usermod -m toyvo -d /home/toyvo`
7. rename the user's group `groupmod -n toyvo biqu`
8. Set a password for the user `passwd toyvo`
9. Disable root login `passwd -l root'
10. Update the system `apt update && apt upgrade -y`
