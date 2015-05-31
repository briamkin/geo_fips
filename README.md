# FIPS Code Getter
### How to use:
```from geo import find_county```<br>
```find_county([40.533548, -97.290977])```

### How it works:
This module simply uses a KD Tree to approximate the 5 closest counties (by county mid point) to the given point. Then it checks if the point exists within any of those 5 counties. If it does then it return that county's FIPS code. If not, it return the closest county. If the closest county is more than a distance of 6 long/lat away, then it returns None.

To return it with corresponding County Name and State Name use this:<br>
```find_county([40.533548, -97.290977],1)```
