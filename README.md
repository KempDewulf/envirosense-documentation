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
|:heavy_check_mark:| Visualize the data stored in the CMS system
|| **--Edge Computing--** ||
|:heavy_check_mark:| 2 devices
|:heavy_check_mark:| Wifi communication
|:heavy_check_mark:| 2 sensors
|:heavy_check_mark:| Other protocol then HTTPS
|:heavy_check_mark:| One type of data that is continuously sampled
|:heavy_check_mark:| Edge computing use case
|:heavy_check_mark:| Events
|| **--Trending Topics--** ||
|:heavy_check_mark:| Application with an own use case
|:heavy_check_mark:| Different unknown programming language or concept
|:heavy_check_mark:| Heartbeat to Firebase
|| **--Global--** ||
|:heavy_check_mark:| All data in the messagebroker
|:heavy_check_mark:| Autodeployment
|:heavy_check_mark:| Caching

## Overview Project
### ![](ReadmeImages/Screenshot.png) Screenshots
## Screens Included
1. Onboarding Screens
2. Authentication Screens
3. New Resident Screens
4. Add Room Screens
5. Add Device Screens
6. Statistics Screens
7. Settings Screens
8. Room Overview Screens
9. Room Devices Screen
10. Room Actions Screens
11. Device (Device History) Screens
12. Device Controls Screens
13. Device Actions Screens
14. No Connection Screen

If you want individual app screens (raw), see the folder **`app-screens-raw`**.

<details>
  <summary>Click to expand screenshots</summary>

![Onboarding Screens](assets/app-screens-showcased/Onboarding%20Screens.png)

![Authentication Screens](assets/app-screens-showcased/Authentication%20Screens.png)

![New Resident Screens](assets/app-screens-showcased/New%20Resident%20Screens.png)

![Add Room Screens](assets/app-screens-showcased/Add%20Room%20Screens.png)

![Add Device Screens](assets/app-screens-showcased/Add%20Device%20Screens.png)

![Statistics Screens](assets/app-screens-showcased/Statistics%20Screens.png)

![Settings Screens](assets/app-screens-showcased/Settings%20Screens.png)

![Room Overview Screens](assets/app-screens-showcased/Room%20Overview%20Screens.png)

![Room Devices Screen](assets/app-screens-showcased/Room%20Devices%20Screen.png)

![Room Actions Screens](assets/app-screens-showcased/Room%20Actions%20Screens.png)

![Device (Device History) Screens](assets/app-screens-showcased/Device%20(Device%20History)%20Screens.png)

![Device Controls Screens](assets/app-screens-showcased/Device%20Controls%20Screens.png)

![Device Actions Screens](assets/app-screens-showcased/Device%20Actions%20Screens.png)

![No Connection Screen](assets/app-screens-showcased/No%20Connection%20Screen.png)

</details>

### ![](ReadmeImages/Database.png) Messagebroker
A RabbitMQ broker is hosted in a Docker container on our VPS, enabling communication between the IoT device and the Deno.js server.

### ![](ReadmeImages/API.png) API request
Request to server x retrieving JSON in the following format displayed in screen x.

[Check out the OpenAPI & AsyncAPI specification here](http://94.130.75.173:8101/)

### ![](ReadmeImages/Intents.png) Devices
1. ESP32 WROVER uses a temperature, humidity, and gas sensor to monitor environmental conditions while controlling a servo.
2. The end-user's phone uses the EnviroSense (Flutter) app to manage rooms and devices.

### ![](ReadmeImages/SensorData.png) Sensor data
The ESP32 reads temperature, humidity, and CO2 data from the sensors, displays the information on the LED screen, and sends it to the message broker.

We also have a Grafana dashboard that listens on the data topic of our real device to display the data.

A snapshot of the dashboard can be seen via this [link](https://kempdewulf.grafana.net/dashboard/snapshot/45ZnzIk8yMndjr5wXwL91eAeKmzp6QsA?orgId=0&from=2025-01-09T18:48:40.135Z&to=2025-01-09T18:53:44.144Z&timezone=browser).

Due to Grafana limitations, an MQTT dashboard cannot be publicly shared.

### ![](ReadmeImages/Workmanager.png) Edge Computing
The IoT device monitors temperatures and automatically opens windows if they exceed the maximum threshold, maintaining ventilation until the target temperature is restored.

### ![](ReadmeImages/Notifications.png) Events
When the server detects bad air conditions coming from the sensors, a notification is sent to the user device, even if app is closed.

The user can send temperature limits, UI-mode selection and brightness setting to the IoT devices.

### ![](ReadmeImages/Workmanager.png) Trending use case
Our Flutter app serves as the primary interface for end-users to interact with our product. Within the app, users can view, add, remove, and modify specific elements.

Other unknown languages we use are:
  - Deno.js (TypeScript) for our server
  - C++ for our IoT device

### ![](ReadmeImages/Animations.png) Auto deployment
Our Deno server is automatically deployed to a Docker container on our VPS, but only after all tests pass successfully.

### ![](ReadmeImages/Notifications.png) Heartbeat
A heartbeat is continuously sent from the ESP32 to a Google Firebase database.

Our VPS also sends a heartbeat to Firebase every 30 seconds with the status of the following docker containers: PostgreSQL, Strapi, Deno server and MQTT broker.

This data will eventually be displayed on Grafana.

### ![](ReadmeImages/Workmanager.png) Caching
Deno dependencies are cached during auto-deployment.

Air quality data per device is cached on the app and only new data is fetched.

## Repositories

Each repository is individually documented

- Flutter App:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/flutter-app
- IoT ESP32:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/iot-esp32
- Deno Server:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/deno-server
- MQTT (RabbitMQ) Broker:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/rabbitmq-broker
- Strapi CMS:
  - https://gitlab.ti.howest.be/ti/2024-2025/s5/ccett/projects/group-14/strapi-cms
