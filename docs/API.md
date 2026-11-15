
# Smart Transit API Documentation

## Overview

The Smart Transit API connects the Passenger Application,
Operator Application, and vehicle tracking hardware
through a Node.js and Express backend.

## Base URL

https://smart-transit-backend.onrender.com

## API Endpoints

### 1. Get Vehicle Information

- Method: GET
- Endpoint: /api/vehicles
- Purpose: Retrieves vehicle information, location, speed,
  status, and estimated arrival time.

### 2. Submit Vehicle Location

- Method: POST
- Endpoint: /api/locations
- Purpose: Sends vehicle GPS coordinates to the backend.

### 3. Start a Trip

- Method: POST
- Endpoint: /api/trips/start
- Purpose: Starts a vehicle trip.

### 4. Get Passenger Demand Summary

- Method: GET
- Endpoint: /api/demand/summary
- Purpose: Retrieves passenger demand information.

### 5. Get Passenger Demand by Hour

- Method: GET
- Endpoint: /api/demand/by-hour
- Purpose: Retrieves passenger demand grouped by hour.

## Technologies

- Node.js
- Express.js
- MySQL
- REST API
