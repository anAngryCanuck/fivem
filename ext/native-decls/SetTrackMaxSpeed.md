---
ns: CFX
apiset: client
game: gta5
---
## SET_TRACK_MAX_SPEED

```c
void SET_TRACK_MAX_SPEED(int track, int newSpeed);
```

Sets the max speed for the train tracks. Used by ambient trains and for station calculations

## Parameters
* **track**: The track id (between 0 - 27)
* **newSpeed**: The tracks new speed

## Issues
When ran to set all track ids' to a certain speed, track ids' 12-27 appear to be invalid and create a warning. 0-11 do not return errors but appear to have no effect on station calculations. Trains attempt to brake at the normal pre-designated point, but when cannot stop in time, train bypasses station.
