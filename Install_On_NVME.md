# Install Retropie on a NVME
Installing on a NVME has numerous advantages, primarily being storage capacity and performance. It is a new feature in Raspberry Pi 5 and as such may require extra steps.

## Update Firmware

There is an issue where the pi may fail to boot with the NVME hat installed. Following the steps in [https://forums.raspberrypi.com/viewtopic.php?t=363401#p2188538](this forum post) the issue appears to be resolved by updating firmware.

```shell
sudo rpi-eeprom-update -a
sudo reboot
```

After rebooting if you no long fail to detect kernel verify the NVME is visible by running

```shell
sudo lspci
```
