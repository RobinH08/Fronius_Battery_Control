# Fronius_Battery_Control
With the files in this repository are able to control your battry (ie. BYD) connected with your Fronius inverter

The code is optimized for slowly changes in a Fronius Gen24 10kW inverter connected with a BYD HVM 22.1

Changes you need to do:

Modbus.yaml
* enter IP-adress of your Fronius inverter

set charging power script:
* change maximum charging/discharging power of your battery

both scripts:
* adopt scaling factor in all registry-write calls (standard value in code is 2.05) depending on the behavior of your system

