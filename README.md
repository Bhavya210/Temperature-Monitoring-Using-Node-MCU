# Temperature-Monitoring-Using-Node-MCU
# IoT Temperature and Humidity Monitoring System

## Overview
This Arduino code is designed for an Internet of Things (IoT) project that monitors temperature and humidity using a DHT11 sensor and sends the data to the ThingSpeak cloud platform. The system is implemented on an ESP8266 microcontroller and requires a Wi-Fi connection for data transmission.

## Requirements
- ESP8266 microcontroller
- DHT11 sensor
- Wi-Fi network credentials
- ThingSpeak account with an API key

## Setup
1. Install the required libraries: ESP8266WiFi.h and dht.h.
2. Configure the Wi-Fi connection by providing the SSID and password in the code.
3. Set up a ThingSpeak account and obtain an API key.
4. Update the TS_API_KEY variable with the obtained ThingSpeak API key.

## Usage
1. The system initializes with an LCD display showing the software version.
2. The ESP8266 connects to the specified Wi-Fi network.
3. The DHT11 sensor reads temperature and humidity data.
4. The data is sent to ThingSpeak using HTTP POST requests.
5. The loop repeats every 10 seconds, providing real-time monitoring.

## Code Structure
- **SW_VERSION:** Software version displayed at startup.
- **DHT11_PIN:** Pin configuration for the DHT11 sensor.
- **WiFi and ThingSpeak Configuration:** Variables for Wi-Fi credentials and ThingSpeak server details.
- **connectWifi():** Function to establish a Wi-Fi connection.
- **sendDataTS():** Function to read sensor data and send it to ThingSpeak.
- **setup():** Initialization function, including Serial communication and Wi-Fi connection.
- **loop():** Main loop for continuous data monitoring and transmission.

## Dependencies
- ESP8266WiFi library for Wi-Fi communication.
- dht library for interfacing with the DHT11 sensor.

## Troubleshooting
- Ensure the correct wiring of components.
- Double-check Wi-Fi credentials and ThingSpeak API key.
- Monitor serial output for debugging information.

## Notes
- Adjust the delay in the loop function according to the desired data transmission frequency.
- Customize the LCD display and additional features as needed.
- Refer to ThingSpeak documentation for further customization and analysis of collected data.
