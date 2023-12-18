# ESP32 Multifunctional Firmware

This firmware is designed for the ESP32 developer board and includes functionalities for BLE, mDNS, and MQTT communication protocols.

## Getting Started

### Prerequisites

- ESP-IDF based on FreeRTOS
- ESP-WROOM-32 development board
- nRF Connect Android app
- MQTT Broker

### Installing

1. Clone the GitHub repository to your local machine.
2. Open the project in the ESP-IDF development environment.
3. Configure the Wi-Fi credentials in the code.
4. Build and flash the firmware onto the ESP-WROOM-32 development board.

### Usage

1. Connect to the BLE server using the nRF Connect Android app.
2. Send the Wi-Fi SSID and Password to the device via BLE.
3. The device will connect to the Wi-Fi network using the received credentials.
4. The device will publish an mDNS service of type _http._tcp.
5. Connect to the MQTT broker to monitor the device.
6. Send a message string via BLE to publish it in a topic that can be monitored in a 3rd party client.

## MQTT Broker URL

The MQTT broker URL is "mqtt://192.168.1.100" with the default port 1883.

## UUID Details

- BLE Service UUID: 0x00FF
- WiFi SSID Characteristic UUID: 0xFF01
- WiFi Password Characteristic UUID: 0xFF02

## Special Instructions

- Ensure that the ESP32 developer board is properly connected to the development environment before flashing the firmware.
- For MQTT communication, ensure that the ESP32 is connected to the same network as the MQTT broker.
- If using the mDNS service, ensure that the network environment supports mDNS and that the MQTT service is advertised via mDNS.

## Authors

- Charan ganesh S
