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

# Events

## Active Event
Had all useful information about the event currently running. Note that if there's no event going on (lol as if), the list will have the last event. So when caling the list, make sure that the end date is in the future.

Data is taken from the [u/SilphScience Reddit Account](https://www.reddit.com/user/SilphScience) and [LeekDuck](https://leekduck.com/events/)

### Link
https://raw.githubusercontent.com/ccev/pogoinfo/info/events/active.json

### Format
The format is self-explanatory. Each key will always be there. If there's no data, the list will be empty.
```js
{
    "name": "Event Name",
    "start": "2020-01-01 08:00", // If the date is unknown: null
    "end": "2020-01-08 22:00",
    "details": {
        "bonuses": [
            "Release of shiny Mew",
            "Debut of Kacleon"
        ],
        "eggs": [
            "001_00"
        ],
        "spawns": [
            "001_00",
            "002_00"
        ],
        "raids": { // If there's missing Raid data, the would be no level keys.
            "1": [
                "001_00"
            ],
            "2": [
                "001_00"
            ],
            "3": [
                "001_00"
            ],
            "4": [
                "001_80"
            ],
            "5": [
                "001_00"
            ]
        },
        "quests": {
            "Land 2 Great Throws": [
                "001_00"
            ],
            "Land 3 Great Throws": [
                "001_00"
            ]
        }
    }
}
```

## All Events
All important events coming up. This includes regular events, Raid and Spotlight Hours and GoFests.

Data is taken from [LeekDuck](https://leekduck.com/events/)

### Link
https://raw.githubusercontent.com/ccev/pogoinfo/info/events/all.json

### Format
There will always be the keys. Name and type should always be known, dates might be null.
```js
[
    {
        "name": "The Event name",
        "type": "Event",
        "start": "2020-07-21 08:00",
        "end": "2020-07-21 22:00"
    }
]
```

## MAD Events
Used for the auto-events MAD Plugin. Every event listed has event-specific Spawnpoints enabled.

Data is taken from [LeekDuck](https://leekduck.com/events/)

### Link
https://raw.githubusercontent.com/ccev/pogoinfo/info/events/mad.json

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
        "local_times": true,            // Optional key, defaults to false (If false, the times are in UTC+0)
        "lure_duration": 180            // Optional key, defaults to 30 (value is in minutes)
    }
]
```
