# Fronius_Battery_Control
With the files in this repository are able to control your battry (ie. BYD) connected with your Fronius inverter

The code is optimized for slowly changes in a Fronius Gen24 10kW inverter connected with a BYD HVM 22.1

Changes you need to do:

Fronius inverter:
* Activate Modbus TCP Slave mode in technician mode of your inverter with standard configuration

Add the following line to your cofiguration.yaml
* modbus: !include modbus.yaml
  
modbus.yaml
* enter IP-adress of your Fronius inverter

set charging power script:
* change maximum charging/discharging power of your battery
* adopt scaling factor in all registry-write calls (standard value in code is 2.05) depending on the behavior of your system
* * if your Scaling Factor entity is not 0, you have to multiply all value by 10^x

Disclamer:
* there could be errors in the code
* scaling factor provided by fronius will not be used - if there are changes in a future software update of your inverter, the provided code may not work
