# CMake
Check if cmake was run as Debug or Release build type

cmake -L . | grep CMAKE_BUILD_TYPE

or add to CMakeLists.txt

add_custom_target(
    print_build_type 
    COMMAND ${CMAKE_COMMAND} -E echo $<$<CONFIG:>:Undefined>$<$<NOT:$<CONFIG:>>:$<CONFIG>>
)


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

### Change swap file size
sudo dphys-swapfile swapoff

As root, edit the file /etc/dphys-swapfile and modify the variable CONF_SWAPSIZE=1024

sudo dphys-swapfile setup

sudo dphys-swapfile swapon

## Raspberry Pi
### VideoCore monitoring
vcgencmd measure_clock arm

vcgencmd get_throttled

Bit field

0: under-voltage

1: arm frequency capped

2: currently throttled 

16: under-voltage has occurred

17: arm frequency capped has occurred

18: throttling has occurred

### Get back to cmd line only
ctrl+alt+F1

sudo /etc/init.d/lightdm stop

### Useful links
https://blog.vpetkov.net/2020/03/30/raspberry-pi-netflix-one-line-easy-install-along-with-hulu-amazon-prime-disney-plus-hbo-spotify-pandora-and-many-others/
https://debugger.medium.com/my-impressions-on-using-a-raspberry-pi-4-as-a-desktop-replacement-ff677c885149

