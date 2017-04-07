# SIMCOM-TO-IOT-HUB

## This page share commands for Simcom (GPS module) to send data to Azure IOT hub. If you encounter any error then one of the root cause could be firmware is not updated on the device. Please try to update it and then try. 

AT+HTTPPARA="CID",1

AT+HTTPPARA="URL","https://IOTHUBNAME.azure-devices.net/devices/DEVICENAME/messages/events?api-version=2016-02-03"

AT+HTTPPARA="USERDATA","SharedAccessSignature sr=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

AT+HTTPPARA="CONTENT","application/json"

AT+HTTPDATA=62,12000{"deviceId":"azuretestdevice1","windSpeed":9.9044241690563144}

AT+HTTPACTION=1//POST

