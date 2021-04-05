# HAN-to-WLAN interface module
This is a combined hardware- and embedded software-project where the readings of electrical power-meters will be interfaced for logging and display without further interaction with external servers and third-party vendors.

## Hardware
The hardware-module will be developed with the Aidon-meters in mind, which is the most used power-meter in eastern Norway.
The hardware-module will be a standalone module powered by the HAN-port of the AMS-meter. For Aidon, there is a maximum current delivery of 30 mA, which is the highest ammount among the AMS-vendors used in Norway.

External power supply will not be neccessary, and the module will be developed for low power consumption without losing the data rate of new data every 2.5 seconds.

## Data parsing
Data from the AMS-meter will be processed on the embedded microcontroller and published through wifi. The plan is to publish every incomming message with MQTT.

## Other specifications
* When the MQTT-broker is unreachable, the incoming AMS-data will be stored in the microcontrollers buffer.