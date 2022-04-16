# Solax X3 inverter monitor

The monitor reads data via TCP modbus from Solax X3. It shows the current free power to consumption. And provides data for the PowerCube (https://github.com/xventus/PowerCube-http). In addition, it calculates the possible power plant profit for the day ahead using the service from www.pvforecast.cz. 

Nodered was chosen for its easy implementation and the need to have only one client to read the data from the inverter. In the case of multiple wedges, the inverter is not able to serve multiple TCP clients in a reasonable time. Therefore nodered serves as a source for other services, e.g. mqtt etc. 

The data is read from FC 4 (Read Input Register) and for reading it is necessary to install: node-red-contrib-modbus

For storing predictions: node-red-contrib-persist

# Flow
![flow](/img/flow.png)

# Dashboard
![dashboard](/img/ui.png)


