
# Smart Transit System - Testing Documentation

## 1. Overview

This document describes the testing procedures
for the Smart Transit System, including its
mobile applications, backend API, GPS tracking,
ETA calculation, and passenger demand monitoring.

## 2. Testing Environment

| Component | Technology |
|---|---|
| Passenger Application | Flutter |
| Operator Application | Flutter |
| Backend | Node.js / Express |
| Database | MySQL |
| Vehicle Controller | ESP32 |
| GPS Module | GPS Module |
| Backend Hosting | Render |
| API Testing | Browser / Postman |

## 3. Functional Testing

| Test ID | Feature | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TC-01 | Backend Connection | Backend responds successfully | To be tested | Pending |
| TC-02 | Vehicle API | Returns vehicle JSON data | Verified | Passed |
| TC-03 | GPS Tracking | Updates vehicle coordinates | To be tested | Pending |
| TC-04 | ETA Calculation | Calculates estimated arrival time | To be tested | Pending |
| TC-05 | Passenger Location Sharing | Sends passenger location | To be tested | Pending |
| TC-06 | Operator Dashboard | Displays vehicle information | To be tested | Pending |
| TC-07 | Demand Monitoring | Displays passenger demand | To be tested | Pending |

## 4. API Testing

### Endpoint: GET /api/vehicles

Production URL:

https://smart-transit-backend.onrender.com/api/vehicles

Expected Result:
- HTTP 200 OK
- JSON response
- Vehicle information is returned

Observed Result:
- JSON vehicle information successfully returned.

Test Status: PASSED

## 5. GPS Tracking Testing

Testing Procedure:
1. Power on the vehicle tracking hardware.
2. Wait for the GPS module to acquire a location.
3. Send the coordinates to the backend.
4. Check the vehicle location through the API.
5. Verify that the coordinates update.

Result: Pending actual vehicle testing.

## 6. ETA Testing

Testing Procedure:
1. Record the vehicle's current location.
2. Calculate the remaining distance.
3. Record the vehicle speed.
4. Compare the predicted ETA with the actual travel duration.

Result: Pending actual trip testing.

## 7. Conclusion

Testing is conducted to evaluate the functionality,
reliability, and performance of the Smart Transit System.

Final results will be updated after completing
the actual system tests.
