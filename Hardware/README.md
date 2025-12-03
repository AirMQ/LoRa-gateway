# Gateway hardware
The gateway hardware is built across off-the-shelf Waveshare ESP32-S3 A7670E 4G Development Board and uses Ebyte E220-900T22D module as serial LoRa transceiver. 

<img src="..\images\ESP32-S3-A7670E-4G.jpg"  width="60%">

Minor modification have been made:
- CN3791 solar charger IC swapped with pin-compatible LiFePo4-capable CN3801
- battery capacitance increased to 2x3800 mAh 26650 cells + 1x1300 mAh 18650 cell (total 8900 mAh)
- added reed switch across hardware reset button


E220-900T22D module is connected to ESP32-S3's Serial2 uart as follows:


| Pin description | Pin number |
| :------- | -------: |
| LORA_RX|(7)|
| LORA_TX|(8)|
| LORA_AUX|(9)|
| LORA_M0|(10)|
| LORA_M1|(11)|

All gateway components are housed in 3D-printed enclosure with external 868 MHz LoRa antenna. For better power and coverage efficiency, solar panel is mounted separately from the gateway, each having individual mounting brackets.

<img src="..\images\GW-inner.png"  width="30%">

TODO:
- add external RTC board with backup battery