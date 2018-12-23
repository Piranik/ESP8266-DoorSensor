# ESP8266-DoorSensor
ESP8266 Tasmota Door Sensor System

## Set OLED Display for SSD1306 on tasmota on the console
Check if Display available:
```
CMD: I2Cscan
MQT: stat/door_office/RESULT = {"I2CScan":"Device(s) found at 0x3c"}
```
Check if DisplayAddress is 60 if not set it:
```
CMD: DisplayAddress
MQT: stat/door_office/RESULT = {"DisplayAddress1":60}

CMD: DisplayAddress 60
MQT: stat/door_office/RESULT = {"DisplayAddress1":60}
```
Check DisplayMode is 0 if not set it:
```
CMD: DisplayMode
MQT: stat/door_office/RESULT = {"DisplayMode":1}

CMD: DisplayMode 0
MQT: stat/door_office/RESULT = {"DisplayMode":0}
```
Check if DisplayDimmer is 100(15) if not set it:
```
CMD: DisplayDimmer
MQT: stat/door_office/RESULT = {"DisplayDimmer":1}

CMD: DisplayDimmer 100
MQT: stat/door_office/RESULT = {"DisplayDimmer":15}
```
Check if Display is working:
```
DisplayText [s1l1c1]Hello how are you?
```
Clean Display:
```
DisplayText [z]
```
## Configure the Switch (Reed Sensor)
```
CMD: SwitchMode2 1
MQT: stat/door_office/RESULT = {"SwitchMode2":1}

CMD: SwitchTopic 1
MQT: stat/door_office/RESULT = {"SwitchTopic":"door_office"}
```
