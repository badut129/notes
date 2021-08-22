# Linux

## Debian

### Temperature sensors
sudo apt install lm-sensors

sudo sensors-detect

sensors

watch sensors


sudo apt install hddtemp

hddtemp

sudo hddtemp SATA:/dev/sda


cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_cur_freq

sudo cat /sys/devices/system/cpu/cpufreq/policy0/cpuinfo_cur_freq

## Raspberry Pi
vcgencmd measure_clock arm

vcgencmd get_throttled

Bit field

0: under-voltage

1: arm frequency capped

2: currently throttled 

16: under-voltage has occurred

17: arm frequency capped has occurred

18: throttling has occurred


ctrl+alt+F1

sudo /etc/init.d/lightdm stop

