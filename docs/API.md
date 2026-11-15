
# Smart Transit API Documentation

## Overview

The Smart Transit API connects the Passenger Application,
Operator Application, and vehicle tracking hardware
through a Node.js and Express backend.

## Base URL

https://smart-transit-backend.onrender.com

## API Endpoints

### 1. Get Vehicle Information

- **Method:** GET
- **Endpoint:** `/api/vehicles`
- **Full URL:** `https://smart-transit-backend.onrender.com/api/vehicles`
- **Purpose:** Retrieves vehicle information, GPS coordinates, speed, route, capacity status, and ETA.

#### Example Response

```json
[
  {
    "vehicleId": "VAN-001",
    "route": "Silago Terminal → Sogod Terminal",
    "latitude": 10.3910,
    "longitude": 124.9811,
    "speed": 2.15,
    "status": "On Route",
    "capacityStatus": "available",
    "distanceRemaining": 25.02,
    "eta": null,
    "lastUpdated": "2026-11-09T04:24:27.000Z",
    "direction": "Silago Terminal → Sogod Terminal"
  }
]
```

*Note: This is an illustrative example. Coordinates and timestamps are sample values, not guaranteed current vehicle data.*

#### Response Fields

| Field | Data Type |
|---|---|
| vehicleId | String |
| route | String |
| latitude | Number |
| longitude | Number |
| speed | Number |
| status | String |
| capacityStatus | String |
| distanceRemaining | Number |
| eta | Number or null |
| lastUpdated | ISO 8601 timestamp |
| direction | String |


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

## Testing the API

You can test the vehicle endpoint using a browser or API testing tool.

### Get Vehicle Information

**GET**
```text
https://smart-transit-backend.onrender.com/api/vehicles
```

Expected result:
- HTTP Status: 200 OK
- Content-Type: application/json
- Response: JSON array containing vehicle information.

### Testing Tools

- Browser
- Postman
- Thunder Client (VS Code Extension)
