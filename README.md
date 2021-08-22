# Linux

# Debian

## Temperature sensors
sudo apt install lm-sensors
sudo sensors-detect
sensors
watch sensors

sudo apt install hddtemp
hddtemp
sudo hddtemp SATA:/dev/sda

# Raspberry Pi
vcgencmd get_throttled
Bit field
0: under-voltage
1: arm frequency capped
2: currently throttled 
16: under-voltage has occurred
17: arm frequency capped has occurred
18: throttling has occurred
