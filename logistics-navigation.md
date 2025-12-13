
# Navigation explained

Ever since we wanted to explore things, [own land](hom-homestead.md), and [conquer land](people-conflicts-war-why.md), we have have been trying various methods to navigate for a long time.

At one time, navigating an unknown region required a few things:

1. Maps of that region, which was the easiest method but required someone to draw on.
2. If anyone was available to provide guidance, asking for directions.
3. Awareness of your environment, which referenced the landmarks given by the map or directions.

Pretty soon, the specificity of using the sun's guidance was replaced by [the compass](logistics.compass.jpg). This permitted travel in adverse weather, at night, and more precision over long distances.

Our modern methods are [vastly better](logistics-navigation-gps.md), but it has taken many centuries of trial-and-error to get here.

Before we handed off the work to computers, most of the effort involved using reference points in the environment.

Naval navigation beyond the shorelines couldn't use any direct landmarks, so they used the sun and stars.

- The sun rises in the east and sets in the west, so it wasn't difficult to measure where it went.
- At night, they used the north star (Polaris) because it stayed at a fixed location in the night sky.

## Global coordinates

The [GPS](logistics-navigation-gps.md) coordinate system is *old*, and likely attributable to Eratosthenes in the 3rd century BC.

The system uses the [radial degrees](math-algebra-cs.md) relative along the circular shape of the Earth:

- Latitude ranges from -90 to 90, with 0 being at the equator.
- Longitudes range from -180 to 180, with 0 being along the meridian of [Null Island](https://en.wikipedia.org/wiki/Null_Island) (an imaginary location in the middle of the Atlantic Ocean).
- The numbers cleanly divide into a degree's minutes and seconds (60 minutes, 60 seconds), with decimal points for the rest.
- While Lat/Lon is the definitive answer before computers, [there is no clear standard in software for representing it](https://macwright.com/lonlat/).

[Our time zones](logistics-navigation.jpg) use this system based in Null Island, with the *approximate* time being offset from that prime meridian.

The system requires at least *some* specificity beyond the raw degrees:

- 1 degree of latitude is approximately 111.111 km, and 1 degree of longitude is about [111.111 x cosine (latitude)] km.
- When converting from radial measurements to decimal, at least 2 decimal places are necessary for an approximation (e.g., Chicago is 41.88, -87.63).
- Navigation requires at least 5 decimal places.
- Most modern GPS devices use at least 10 decimal places.
- When using computers, which require extreme specificity relative to a mobile device, [it gets *much* more difficult](https://ihatecoordinatesystems.com/).
