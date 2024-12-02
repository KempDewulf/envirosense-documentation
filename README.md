# EnviroSense CCETT documentation

## Groupmembers
### Group 14
1. Kemp Dewulf
2. Layton Berth

## Project summary
This system monitors the air quality within university classrooms using multi-sensor integration. It continuously tracks pollutants (e.g., CO2, VOCs, particulate matter), temperature, and humidity to ensure a healthy environment. When unsafe levels of pollutants or fire risks are detected, the system will trigger alarms and interact with smart devices to take appropriate actions—such as opening windows, activating air conditioning, or unlocking doors to improve ventilation and ensure safety.

## Requirements
### ℹ️ Legend
- :heavy_check_mark: = Implemented
- :x: = Not implemented
- :hourglass: = Work in progress

 
|Status|Description|Details|
|---|---|---|
|| **--CMS--** ||
|:heavy_check_mark:| Headless CMS system STRAPI to store all the cloud data
|:hourglass:| Visualize the data stored in the CMS system
|:hourglass:| Use TensorFlow that consumes the data stored in the CMS
|| **--Edge Computing--** ||
|:heavy_check_mark:| 2 devices
|:heavy_check_mark:| Wifi communication
|:heavy_check_mark:| 2 sensors
|:heavy_check_mark:| Other protocol then HTTPS
|:heavy_check_mark:| One type of data that is continuously sampled
|:heavy_check_mark:| Edge computing use case
|| Events
|| **--Trending Topics--** ||
|:hourglass:| Application with an own use case
|:heavy_check_mark:| Different unknown programming language or concept
|:heavy_check_mark:| Heartbeat to Firebase
|| **--Global--** ||
|:hourglass:| All data in the messagebroker
|:hourglass:| Autodeployment
|:hourglass:| Caching

## Overview Project
### ![](ReadmeImages/Screenshot.png) Screenshots
Give screenshots for every screen in the application. Give each screen an unique name.

### ![](ReadmeImages/Database.png) Messagebroker
Type of data stored in the messagebroker used in screen x and displayed in screen y.

### ![](ReadmeImages/API.png) API request
Request to server x retrieving JSON in the following format displayed in screen x.

### ![](ReadmeImages/Intents.png) Devices
1. ESP32 WROVER using a temperature, humidity and gas sensor.
2. End-user device (Android Phone) using the EnviroSense (flutter) app to manage the rooms and devices.

### ![](ReadmeImages/SensorData.png) Sensor data
The ESP32 reads the temperature, humidity and gas data from the sensors. This gets displayed on the LED screen and will be sent to the messagebroker.

### ![](ReadmeImages/Workmanager.png) Edge Computing
The ESP32 will activate a servo to simulate the opening of a smart window to reach target temperature.

### ![](ReadmeImages/Notifications.png) Events
Implementation of notifications & events.

### ![](ReadmeImages/Workmanager.png) Trending use case
Implementation of the application with an unknown programming language or concept.

### ![](ReadmeImages/MLkit.png) Tensorflow
Implementation of Tensorflow.

### ![](ReadmeImages/Animations.png) Auto deployment
Implementation of auto deployment.

### ![](ReadmeImages/Notifications.png) Heartbeat
A heartbeat is continuously sent from the ESP32 to a Google Firebase database.

### ![](ReadmeImages/Workmanager.png) Caching
Implementation of caching.


## Repositories
- Flutter App:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/flutter-app
- IoT ESP32:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/iot-esp32
