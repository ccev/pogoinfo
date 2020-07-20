# Pogo Information

The goal of this repo is to provide a central source for up-to-date information about events, available shinies and grunttypes.

# Data

## MAD Events
Used for the auto-events MAD Plugin. Every event listed has event-specific Spawnpoints enabled.

### Link
https://raw.githubusercontent.com/ccev/pogoinfo/info/mad-events.json

### Format
```java
[
    {
        "name": "Event Name 1",
        "start": "2020-01-01 00:00",
        "end": "2020-01-01 22:00"
    },
    {
        "name": "Event Name 2", // Required key
        "start": "2020-07-19 11:00", // Required key
        "end": "2020-07-19 17:00", // Required key
        "local_times": true, // Optional key, defaults to false
        "lure_duration": 180 // Optional key, defaults to 30 (value is in minutes)
    }
]
```
