# Pogo Information

The goal of this repo is to provide a central source for up-to-date information about events, available shinies and grunttypes.

# Data

## Grunts
All information about grunts currently in rotation.

### Link
https://raw.githubusercontent.com/ccev/pogoinfo/info/grunts.json

### Format
```js
{
    "id": {
        "type": "Bug",
        "grunt": "Female"
    },
    "3": {
        "type": "",             // Required key: the name/pokemon type of that grunt
        "grunt": "",            // Required key: the gender
        "second_reward": true,  // Optional key: Can the second Pokemon of that grunt be a reward?, default: false
        "encounters": {         // Optional key: Possible mons in the grunt's team, default: {}
            "first": [
                "000_00"        // Pokemon format: {mon id padded to 3}_{form id}
            ],
            "second": [
                "000_00"
            ],
            "third": [
                "000_00"
            ]
        }
    }
}
```

## MAD Events
Used for the auto-events MAD Plugin. Every event listed has event-specific Spawnpoints enabled.

### Link
https://raw.githubusercontent.com/ccev/pogoinfo/info/mad-events.json

### Format
```js
[
    {
        "name": "Event Name 1",
        "start": "2020-01-01 00:00",
        "end": "2020-01-01 22:00"
    },
    {
        "name": "Event Name 2",         // Required key
        "start": "2020-07-19 11:00",    // Required key
        "end": "2020-07-19 17:00",      // Required key
        "local_times": true,            // Optional key, defaults to false
        "lure_duration": 180            // Optional key, defaults to 30 (value is in minutes)
    }
]
```
