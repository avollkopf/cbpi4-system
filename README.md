# CraftBeerPi4 System Functions Plugin

### Functions:

- Plugin has capability to reboot Pi every day at a time that can be specified in the settings.

![Auto Reboot](https://github.com/avollkopf/cbpi4-system/blob/main/AutoReboot.png?raw=true)

### Sensors	

Plugin will add system 'sensors' to monitor some system parameters. The psutil package is currently used for that purpose:
	
- CPU Load: 		CPU load in % (psutil: cpu_perc)
- Available Memory:	Available system memory in Mb (psutil: vitrual_memory -> available)
- Used memory:		Used memory in percent (psutil: vitrual_memory -> percent)
- CPU Temp:		CPU temperature (psutil: sensors_temperatures -> cpu_thermal)

Each parameter has to be added as individual sensor.
	
![Sensor Config](https://github.com/avollkopf/cbpi4-system/blob/main/SystemSensor.png?raw=true)

### Installation: 
- sudo pip3 install cbpi4-system
- or install from repo: sudo pip3 install https://github.com/avollkopf/cbpi4-system/archive/main.zip
	
### Usage:

- Add Hardware under Sensor and choose SystemSensor as Type
- Configure Autoreboot in settings (Default is 'No') and specify time of day (0-23 -> Full hour)

### Changelog:

- 16.01.22: (0.0.5) Adaption for cbpi 4.0.1.2
- 12.01.22: (0.0.4) Reduced amount of mqtt traffic
- 27.11.21: (0.0.3) New Readme file and link to plugin included in setup.py
- 02.09.21: (0.0.2) Remove Actor to reboot / shutdown system. Add automatic reboot and add system sensors
- 18.06.21: (0.0.1) Initial commit with Actor to shutdown/reboot system
