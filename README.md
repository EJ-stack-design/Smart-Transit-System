# Smart Transit System

### GPS-Based Commuter Vehicle Tracking and ETA Monitoring System

A mobile-based transportation monitoring system designed to improve commuter experience through real-time vehicle tracking, estimated time of arrival (ETA) monitoring, and passenger demand analysis.

The system consists of separate passenger and operator mobile applications, a backend server, a database, and GPS-enabled vehicle tracking hardware.

---

## Project Overview

The Smart Transit System aims to provide commuters with accessible vehicle tracking information while helping transport operators monitor vehicle locations and passenger demand.

Passengers can view vehicle locations and estimated arrival times, while operators can monitor fleet activity and passenger demand through a dedicated dashboard.

**Project Status:** Under Development

**Project Type:** Computer Engineering / Mobile Application / IoT

**Developers:** EJ Godpray Doquila and Team

---

## Technologies Used

### Mobile Development
- Flutter
- Dart

### Backend Development
- Node.js
- Express.js
- REST API

### Database
- MySQL

### Hardware and IoT
- ESP32
- GPS Module
- Cellular Communication Module

### Development Tools
- Visual Studio Code
- Git and GitHub
- Android Studio

---

## Key Features

### Passenger Application
- View available commuter vehicles.
- Monitor vehicle locations on a map.
- Check estimated time of arrival (ETA).
- Share passenger location when permitted.
- Receive vehicle capacity information.

### Operator Application
- Operator authentication.
- Monitor vehicle locations.
- View passenger locations who enabled location sharing.
- Monitor passenger demand.
- View demand summaries and hourly statistics.

### Backend System
- REST API for mobile applications.
- Vehicle location management.
- Trip management.
- Passenger session management.
- ETA calculation.
- Demand data collection and processing.

---

## Application Screenshots

### Passenger Application

**Passenger Home Screen**

![Passenger Home](screenshots/passenger-home.jpg)

**Vehicle Tracking Map**

![Passenger Map](screenshots/passenger-map.jpg)

**Passenger Location Sharing**

![Passenger Sharing](screenshots/passenger-sharing.jpg)

---

### Operator Application

**Operator Login**

![Operator Login](screenshots/operator-login.jpg)

**Operator Dashboard**

![Operator Dashboard](screenshots/operator-dashboard.jpg)

---

## System Architecture

The Smart Transit System uses a client-server architecture
to connect passengers, vehicle operators, and vehicle hardware.

```mermaid
flowchart TD
    A[ESP32 + GPS Module] -->|Vehicle location data| B[Node.js / Express Backend]

    B <--> C[(MySQL Database)]

    B -->|Vehicle location and ETA| D[Passenger Flutter App]
    B -->|Fleet and passenger demand data| E[Operator Flutter App]

    D -->|Passenger location sharing| B
    E -->|Operator monitoring| B
```
--- 

## System Architecture

The Smart Transit System connects the passenger
application, operator application, vehicle hardware,
backend server, and MySQL database.

![Smart Transit System Architecture](docs/images/Smart_Transit_System_Architecture.png)
