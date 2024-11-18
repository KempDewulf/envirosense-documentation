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
|:hourglass:| Headless CMS system STRAPI to store all the cloud data
|:hourglass:| Visualize the data stored in the CMS system
|:hourglass:| Use TensorFlow that consumes the data stored in the CMS
|| **--Edge Computing--** ||
|:hourglass:| 2 devices
|:hourglass:| Wifi communication
|:heavy_check_mark:| 2 sensors
|:heavy_check_mark:| Other protocol then HTTPS
|:hourglass:| One type of data that is continuously sampled
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

## Overview app
### ![](ReadmeImages/Screenshot.png) Screenshots
Give screenshots for every screen in the application. Give each screen an unique name.

### ![](ReadmeImages/Database.png) Messagebroker
Type of data stored in the messagebroker used in screen x and displayed in screen y.

### ![](ReadmeImages/API.png) API request
Request to server x retrieving JSON in the following format displayed in screen x.

### ![](ReadmeImages/Intents.png) Devices
1. Detail device 1
2. Detail device 2

### ![](ReadmeImages/SensorData.png) Sensor data
Implementation of sensor data.

### ![](ReadmeImages/Workmanager.png) Edge Computing
Implementation of the Edge Computing use case

### ![](ReadmeImages/Notifications.png) Events
Implementation of notifications & events.

### ![](ReadmeImages/Workmanager.png) Trending use case
Implementation of the application with an unknown programming language or concept.

### ![](ReadmeImages/MLkit.png) Tensorflow
Implementation of Tensorflow.

### ![](ReadmeImages/Animations.png) Auto deployment
Implementation of auto deployment.

### ![](ReadmeImages/Notifications.png) Heartbeat
Implementation of the 2 weeks heartbeat.

### ![](ReadmeImages/Workmanager.png) Caching
Implementation of caching.


## Repositories
- Code
  - https://gitlab.ti.howest.be/ti/
