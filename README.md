# Notes
- This can be used with the Void Linux uConsole image (https://github.com/paigeadelethompson/void-uconsole?tab=readme-ov-file) to install a more comprehensive OS. 
- This is still a WIP, if you know and understand Ansible please help out with testing and contribute so that this can be improved =)


# Quickstart
- Write the Void Linux uConsole image to an SDcard (instructions and image releases are here: https://github.com/paigeadelethompson/void-uconsole?tab=readme-ov-file)
- With the SDCard inserted into the computer, mount the second partition of the SDCard to a mountpoint (ex `mount -t exfat /dev/mmcblk0p2 /mnt`)
- git clone to the second partition on the Void Linux image (ex: `cd /mnt ; git clone git@github.com:paigeadelethompson/paige-ansible-uconsole.git`
- Edit the `wpa_supplicant.conf` file (WiFi configuration for post-boot installation)
- unmount the sideload partition, eject the SDCard and insert into the uConsole
- boot on uconsole
- login as `pi`
- `sudo ansible-playbook -vvvvvv /mnt/sideload/install.yml`
- `reboot`

## Start KDE
- login as `pi` then run: `dbus-run-session startplasma-wayland`. Refer to Github issues in this repository for more info on the status of things that are not working or to report problems. 
