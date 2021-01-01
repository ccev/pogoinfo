# Pogo Information

Lots of up-to-date data for Pogo. Updated everyday at 9am GMT.

Go through the code and see if you find something useful.
- events/active.json is only good for event spawns. eggs/raids/quests are not really supported


### Pokemon Format:

Each key will only be there, if the script knows about it and its value is > 0.

```js
{
    "id": 1,                            // Pokemon ID
    "form_id": 1028,                    // Form ID (Only if it's Alolan/Costume/whatever, no NORMAL IDs)
    "costume_id": 11,                   // Costume ID
    "evolution_id": 1,                  // Mega ID (1 = normal, 2 = X, 3 = Y)
    "proto_id": "BULBASAUR_NORMAL",     // The in-game/proto ID
    "asset_id": "167"                   // Asset ID used in the default PogoAssets
}
```