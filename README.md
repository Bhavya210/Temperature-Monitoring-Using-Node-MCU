# IoT Temperature Monitoring and Forest Fire Detection using Node MCU

## Overview
This Arduino code serves a dual purpose: monitoring temperature and humidity with a DHT11 sensor while incorporating a Forest Fire detection system. The data is transmitted to the ThingSpeak cloud platform via an ESP8266 microcontroller, requiring a Wi-Fi connection for seamless communication.

## Requirements
- ESP8266 microcontroller (NodeMCU)
- DHT11 sensor
- Flame sensor for Forest Fire detection
- Wi-Fi network credentials
- ThingSpeak account with an API key

## Setup
1. Install the necessary libraries: ESP8266WiFi.h, dht.h, and additional libraries for the Flame sensor.
2. Configure the Wi-Fi connection by providing the SSID and password in the code.
3. Set up a ThingSpeak account and obtain an API key.
4. Update the TS_API_KEY variable with the obtained ThingSpeak API key.

## Usage
1. The system initializes, displaying the software version on an LCD screen.
2. The NodeMCU connects to the specified Wi-Fi network.
3. The DHT11 sensor reads temperature and humidity data.
4. The Flame sensor monitors for potential forest fires.
5. Collected data is sent to ThingSpeak using HTTP POST requests.
6. The loop repeats every 10 seconds, ensuring real-time monitoring.

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
- Additional libraries for Flame sensor integration.

## Troubleshooting
- Ensure correct wiring of all components.
- Double-check Wi-Fi credentials and ThingSpeak API key.
- Monitor serial output for debugging information.

## Notes
- Adjust the loop delay based on the desired data transmission frequency.
- Customize the LCD display and add features as needed.
- Refer to ThingSpeak documentation for advanced customization and analysis of collected data.
