
# What computer geolocation is is

[Navigation](logistics-navigation.md) via computers is arguably one of the most useful implementations of technology in the 21st century.

"Geolocation" is a modern miracle that effectively removes the need for most direct navigation skill. It involves "geodesy", which is using a [3-dimensional representation](engineering-graphics.md) of geographical elements. It usually uses a "Global Positioning System" (GPS), but often uses other technologies as well (e.g., [cellular towers](engineering-radio.md), sonar), and can more broadly refer to "global navigation satellite systems" (GNSS).

## GPS satellites

The infrastructure for geolocation is mostly composed of a constellation of GPS [satellites](engineering-vehicles-spacecraft.md), originally designed by the US military. There are at least 24 active satellites orbiting over 12,000 miles above the Earth.

Each of these satellites has a *very* precise atomic clock, which is constantly broadcasting radio signals towards the Earth.

The satellite positions are arranged so that there are always at least 12 satellites on any given position, though [they're *not* in the same location relative to each other](logistics-navigation-gps.gif).

## Finding location

The GPS satellite system begins the process that devices use to calculate geolocation:

1. The GPS device reads the constant [radio signals](engineering-radio.md) coming from satellites' "transponders".
2. If it can successfully get a "lock" on a GPS satellite, it's able to calculate its distance from that satellite.
3. 3-4 successful locks allow the software to perform "[trilateration](math-geotrig.md)", which uses circles to detect the device's location.

Trilateration is a bit complex. The general idea, though, is that the distance is calculated by offset time between when any particular signal is sent or received, which creates a circle around that fixed point. Multiple signals converging together can determine a precise location through deduction. All the signals use radio waves, which operate at the speed of light (i.e., 299,792.458 km/s).

Further, a device often has the means to draw other information for trilateration:

- Emergency 911 services use cell tower strength to triangulate the position of mobile devices.
- Wi-Fi Positioning Systems (WPS) use Wi-Fi networks to trace location, similarly to E911.

Beyond GPS, other services exist beyond the scope of US control (typically in case of [a war](people-conflicts-war-why.md)):

- Russia has GLONASS.
- India has IRNSS.
- China has BDS, or BeiDou.
- Europe has Galileo.

While GPS signals generally work fine on open terrain, urban environments can create major problems:

1. Direct line-of-sight signals are blocked by buildings.
2. Large, flat surfaces on *other* buildings can reflect the signals off them, giving a false read for a different location on the other side of the street.

The solution is to use multiple satellites and surrounding data to determine which side of the street someone is on:

1. The blocked satellites determine what side of the street the device is on.
2. Signal strength can determine whether the signal was reflected or directly sent.
3. Use a "heat map" to determine where a device is *likely* to be.
4. The information can be cross-referenced with Wi-Fi signal strength.

## Presentation/apps

However, geolocation by itself isn't necessarily useful, and needs to express on a map.

Unless it's a direct 3-dimensional [graphical representation](engineering-graphics.md) of the Earth itself, maps must reduce something down for the sake of simplicity.

- Maps represent a 3-dimensional sphere as a 2-dimensional projection. There are [many approaches to making a world map](https://en.wikipedia.org/wiki/List_of_map_projections), but the easiest *software* solution is to simply use a flat plane. This, however, [will distort our perspective of geographical relationships](https://unchartedterritories.tomaspueyo.com/p/maps-distort-how-we-see-the-world).

Map applications vary *wildly* by design and need:

- If a map were to display *all* available information about everything it had, it'd be too cluttered to view.
- Maps for navigation are typically designed to be minimalist, to make viewing it convenient while operating a vehicle.
- Maps for research are typically filled with data corresponding to need.

The minimalism of maps, however, means there are *major* technicalities about seemingly simple matters:

- How wide a road ought to be represented (e.g., non-driving lanes, service lanes).
- The best way to represent unique roads (e.g., one-way roads, service roads).
- How to represent intersections, especially when they're at strange angles.

As "geographic information systems" (GIS) include more layers (e.g., hotels, restaurants, traffic data), the [UX](engineering-design.md) for maps becomes more difficult:

- When there is plenty of *potentially* useful information, the map must have layers that can be toggles, which adds extra complexities, especially if some of that data requires constant updating.
- When a map expresses information, sometimes that information won't arrive in a timely manner, which may cause issues for the user as they start to interpret information before it updates to its final form.
- At scale, the map information will be spread across a [distributed system](computers-distsys.md), meaning the developers have to think ahead about bandwidth and processor load relative to users' use of the software.
- Most of the time, a map must permit the user to interact with it and move it around, which magnifies *all* of the above.
- By implementing a Street View feature, photographic data (often as panoramic tiles) can be added to specific coordinates, which even *further* complicates the system.
- If a map system ever integrates with [autonomous vehicles](computers-autos.md), the complexities become almost inhumanly difficult to fully codify in a single essay.

And, social requirements can make the UX even more complex:

- Monetizing the app with [advertisements](marketing.md) can *dramatically* alter the quality of the map, to the point that it may remove important information for navigation, such as street names.
- Political issues, specifically [territorial disputes](https://en.wikipedia.org/wiki/List_of_territorial_disputes), may create *severe* conflicts over the colored shading of a region or its given name. Ironically, most software developers were simply pulling from other maps and didn't think about it.
- For military reasons, satellite imagery may be removed or redefined, especially in a [conflict zone](https://gainedn.site/war/).

## Additional reading

[How Trilateration Works](https://ciechanow.ski/gps/)
