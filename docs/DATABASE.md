
# Smart Transit Database Design

## Entity Relationship Diagram

```mermaid
erDiagram
    TRIPS ||--o{ DEMAND_RECORDS : contains
    TRIPS ||--o{ ETA_TRAINING_DATA : contains
    TRIPS ||--o{ ETA_TRAINING_SAMPLES : contains

    VEHICLES {
        int id PK
        varchar vehicle_id UK
        varchar route
        varchar status
    }

    TRIPS {
        int id PK
        varchar vehicle_id
        datetime start_time
        datetime end_time
        int estimated_eta
        int actual_duration
        varchar status
        varchar direction
    }

    VEHICLE_LOCATIONS {
        int id PK
        varchar vehicle_id
        decimal latitude
        decimal longitude
        decimal speed
        datetime timestamp
        int trip_id
    }

    DEMAND_RECORDS {
        int id PK
        int trip_id FK
        varchar vehicle_id
        int passenger_count
        datetime recorded_at
    }

    ETA_TRAINING_DATA {
        int id PK
        int trip_id FK
        varchar vehicle_id
        decimal latitude
        decimal longitude
        decimal speed
        decimal distance_remaining
        int passenger_count
        datetime recorded_at
        decimal actual_remaining_minutes
    }

    ETA_TRAINING_SAMPLES {
        int id PK
        int trip_id FK
        varchar vehicle_id
        int estimated_eta
        int actual_duration
        decimal average_speed
        decimal max_speed
        decimal distance_km
        int passenger_count
        datetime recorded_at
    }
```

## Foreign Key Constraints

- `demand_records.trip_id` references `trips.id`.
- `eta_training_data.trip_id` references `trips.id`.
- `eta_training_samples.trip_id` references `trips.id`.

Note: Other matching columns are not shown as
confirmed foreign-key relationships.
```
