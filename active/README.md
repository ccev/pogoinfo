# active/

## grunts.json

This file holds information about the Team Rocket grunts with the ID of 1 to 50 and 53/54.

```js
{
    "1": {                              // The ID of the grunt
        "active": true                  // Whether or not the grunt is currenty being available to battle
        "character": {                  // General info about the grunt character
            "template": "CHARACTER...", // The templateId used in PoGo
            "gender": 0,                // 0 = female, 1 = male
            "boss": true,               // True if the grunt is Giovanni/Sierra/Arlo/Cliff
            "type:" {                   // null if the grunt has no specific pokemon type
                "id": 1,                // If  the grunt has a specific type, ID and templateID are available
                "template": "GRASS"
            }
        },                              // the "character" field and all its keys will always be there
        "lineup": {                     // only exists if active = true
            "rewards": [
                0                       // Which index of the "team" list is available as a reward
            ],
            "team": [                   // All possible mons a grunt can have in its 3 team slots
                [
                    Mon,                // Mon = A Pokemon field
                    Mon
                ],
                [
                    Mon
                ],
                [
                    Mon
                ]
            ]
        }
    }
}
```
