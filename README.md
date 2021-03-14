# Pogo Information

Lots of up-to-date data for Pogo. Updated automatically.

Go through the files and see if you find something useful. Most of the structures are self-explainatory (except for Grunts maybe, but that format is explained in active/README.md)

### Pokemon Format:

Each key will only be there, if the bot knows about it and its value is > 0. All possible keys:

```js
{
    "id": 1,                            // Pokemon ID
    "form": 1028,                       // Form ID (Only if it's Alolan/Costume/whatever, no NORMAL IDs)
    "costume": 11,                      // Costume ID
    "evolution": 1,                     // Mega ID (1 = normal, 2 = X, 3 = Y)
    "template": "BULBASAUR_NORMAL",     // The in-game/proto ID
    "asset": "167"                      // Asset ID used in the default PogoAssets
}
```
