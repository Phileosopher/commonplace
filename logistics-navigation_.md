
GPS is arguably one of the most useful implementations of computers in the 21st century.

At one time, navigating an unknown region required a few things:

1. Maps of that region, which was the easiest method.
2. If anyone was available to provide guidance, asking for directions.
3. Awareness of your environment, which referenced the landmarks given by the map or directions.

"Geolocation" is a modern miracle that effectively removes the need for most of that skill. It involves "geodesy", which is using a [3-dimensional representation](engineering-graphics.md) of geographical elements. It usually uses a "Global Positioning System" (GPS), but often uses other technologies as well (e.g., [cellular towers](engineering-radio.md), sonar), and can more broadly refer to "global navigation satellite systems" (GNSS).

## Coordinates

The GPS coordinate system is *old*, and likely attributable to Eratosthenes in the 3rd century BC.

The system uses the [radial degrees](math-algebra-cs.md) relative along the circular shape of the Earth:

- Latitude ranges from -90 to 90, with 0 being at the equator.
- Longitudes range from -180 to 180, with 0 being along the meridian of [Null Island](https://en.wikipedia.org/wiki/Null_Island) (an imaginary location in the middle of the Atlantic Ocean).
- The numbers cleanly divide into a degree's minutes and seconds (60 minutes, 60 seconds), with decimal points for the rest.
- While Lat/Lon is the definitive answer before computers, [there is no clear standard in software for representing it](https://macwright.com/lonlat/).

Our time zones use this system based in Null Island, with the *approximate* time being offset from that prime meridian:

![](https://trendless.tech/wp-content/uploads/2023/10/time-zones-1024x552.jpg)

The system requires at least *some* specificity beyond the raw degrees:

- 1 degree of latitude is approximately 111.111 km, and 1 degree of longitude is about [111.111 x cosine (latitude)] km.
- When converting from radial measurements to decimal, at least 2 decimal places are necessary for an approximation (e.g., Chicago is 41.88, -87.63).
- Navigation requires at least 5 decimal places.
- Most modern GPS devices use at least 10 decimal places.
- When using computers, which require extreme specificity relative to a mobile device, [it gets *much* more difficult](https://ihatecoordinatesystems.com/).

## Satellite navigation

Since there's no weather to interfere, satellites are typically solar-powered.

Instead of simply using "transceivers" that send pure information, satellites must use "transponders" to accommodate for the "Doppler effect" from how fast they're moving relative to the Earth's surface.

The moon and sun gravitationally pull satellites by up to a degree every year, so satellites require a propulsion system to make occasional corrections, known as "attitude adjustment". Maintaining an orbit trajectory is called "station keeping", and is necessary to prevent orbit decay.

- If a satellite ever experiences too much orbit decay, it effectively becomes space debris.
- The lifespan of a satellite is determined by how long it can maintain its thruster fuel before it runs out.

There are 3 major orbits for a satellite, relative to the Earth:

- Low Earth Orbit (LEO)
  - 160-1600 km above the earth
  - To cover the entire earth, requires at least 20 satellites
  - Every signal takes 0.0005-0.005 seconds to travel at the speed of light, meaning 0.001-0.01 seconds for a successful [SYN-ACK signal](networks-computer.md)
- The range between 1600-10,000 km is dangerous for electronic components because of the Van Allen radiation belt, so no satellites orbit there.
- Medium Earth Orbit (MEO)
  - 10,000-20,000 km above the earth
  - To cover the entire earth, requires at least 30 satellites
  - Every signal takes 0.033-0.066 seconds to travel at the speed of light, meaning 0.066-0.12 seconds per packet
  - Most Earth-observing satellites are *not* MEO
- Geosynchronous Orbit (GEO)
  - 35,786 km above the earth
  - Designed to correspond to a single point on the ground
  - Only requires 3 satellites to cover the entire earth
  - Every signal takes 0.11 seconds to travel at the speed of light, meaning 0.22 seconds per packet
  - Most navigation satellites are GEO

The amount of latency, and relative speed of the satellite, requires a *lot* of calculation and signal management to successfully send and receive information.

- The information travels via [radio waves](engineering-radio.md) somewhere in the 1-50 GHz band, and the bands are identified by letters.
- Lower-range bands (L-band, S-band, C-band) are lower-power, and therefore require larger antennas.
- Higher-end bands (X-band, Ku-band, Ka-band, V-band) have more power, so the dishes can be as small as 45 cm in diameter.
  - High-end bands are ideal for "direct-to-home" (DTH) broadcasting and broadband data/phone.
- The inherent latency, however, means that satellites are *not* ideal for almost any two-way real-time data transfer unless they're LEO.

Each satellite must be *very* reliable, above 99.9%, since [maintenance](fix.md) and hardware upgrades are nearly nonexistent or prohibitively expensive.

## GPS satellites

The infrastructure for geolocation is mostly composed of a constellation of GPS satellites, originally designed by the US military. There are at least 24 active satellites orbiting over 12,000 miles above the Earth.

Each of these satellites has a *very* precise atomic clock, which is constantly broadcasting radio signals towards the Earth.

The satellite positions are arranged so that there are always at least 12 satellites on any given position, though they're *not* in the same location relative to each other:

![](https://trendless.tech/wp-content/uploads/2023/10/satellites.gif)

## Finding location

The GPS satellite system begins the process that devices need to calculate geolocation:

1. The GPS device reads the constant [radio signals](engineering-radio.md) coming from satellites' "transponders".
2. If it can successfully get a "lock" on a GPS satellite, it's able to calculate its distance from that satellite.
3. 3-4 successful locks allow the software to perform "[trilateration](math-geotrig.md)", which uses circles to detect the device's location.

Trilateration is a bit complex. The general idea, though, is that the distance is calculated by offset time between when any particular signal is sent or received, which creates a circle around that fixed point. Multiple signals converging together can determine a precise location through deduction. All the signals use radio waves, which operate at the speed of light (i.e., 299,792.458 km/s).

Further, a device often has the means to draw other information for trilateration:

- Emergency 911 services use cell tower strength to triangulate the position of mobile devices.
- Wi-Fi Positioning Systems (WPS) use Wi-Fi networks to trace location, similarly to E911.

Beyond GPS, other services exist beyond the scope of US control (typically in case of [a war](people-conflicts-war.md)):

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

## Satellite data

Beyond GPS coordinates, satellites can also serve as [network nodes](networks-computer.md) for data.

- Unlike cabling or [cellular towers](engineering-radio.md), the only hardware costs for satellites come from launching the network into space.
- While a satellite connection can be anywhere in the world, the data transfer speeds for satellites are much lower than other technologies, and can be obstructed by cloud cover, aircraft, and foliage.
- It's possible to compensate for the slow network speed and data constraints by using *many* satellites, but it can be prohibitively expensive (especially in replenishing satellites as their orbit decays) and will only work well up to a point.
- Without air, the signals can use [radio waves](engineering-radio.md) or lasers.

For redundancy's sake, satellites tend to have many transponders at once pointing in any given direction.

Since data satellites need to send and receive information, the satellites usually form into a [grid network](networks-computer.md), and typically with redundancies. This grid can connect relatively seamlessly with other data networks, such as [cellular networks](engineering-radio.md).

Since data satellites have a predictable amount of latency, they can be reverse-engineered for trilateration, even when they're not officially designed for the purpose.

## Satellite devices

While GPS devices simply require a receiver, satellite data devices require a "transceiver" to successfully send the information.

- To get enough of a reliable signal, the signal reader typically faces an elliptical dish, which expands the target area for gathering signals from the satellite's transponder.
- The transmitter is typically part of the same dish housing to ensure it sends a signal back to the satellite it received from.

Modern satellite data devices use motorized tracking system that rotate the satellite dish to wherever it needs to aim.

- Motorized tracking makes migrating to another satellite on a network straightforward for the end-user.
- Automated lock can also allow implementations that would otherwise be impossible (e.g., aircraft, maritime).

## Satellite images

Most satellite images are taken in LEO, and usually only on-demand because they can only transmit 10 minutes of data per ground station.

Satellite [cameras](engineering-camera.md) are designed somewhat differently than other cameras. Instead of capturing raw light (which would pick up a *lot* of other interference), it instead uses 3 different optical sensors to track red, green, and blue, which is then post-produced into the final product. They can just as easily, and often do, track [wavelengths](engineering-radio.md) beyond the visible spectrum (e.g., infrared).

There are *many* useful implementations for satellite imagery over other domains, such as drones:

- Firefighting - infrared imaging can detect precise locations of wildfires.
- [Livestock](agriculture.md) - infrared imaging can detect animal movements.
- Pipeline operators - consistent imaging can detect incursions into right-of-way zones.
- [Insurance](insurance.md) - historical imaging can help investigations into fraudulent claims.
- Retail investment - historical imaging can predict future profitability based on parking lot fullness
- [Farm](horticulture.md) investment - historical imaging can predict crop yield before farmers report it
- Government - imaging can track human trafficking, find illegal fishing activities, track criminals, and find insurgent/revolutionary groups
- Not-for-profits - images can address large-scale human rights violations, draw attention to damages caused by [war](people-conflicts-war.md), and monitor oil spills

However, this data is frequently on-demand, so people will either use publicly available satellite imagery or will hire out contractors for the data if the need is severe enough.

## Satellite problems

Satellites aren't *completely* alone in a vacuum, and some problems arise in space, no matter how well the technology develops.

When the orbit is *very* low, a geomagnetic storm may hit some satellites and damage their circuitry.

Like all other spacecraft, satellites are expensive to launch. This would only be remediated if we had an easier way to get into space.

Man-made satellites become space junk when they're done. While they don't individually represent any particular threat, their trajectories may potentially collide with future satellites (especially in LEO), and can [clutter up observation of other celestial objects further out](https://www.caltech.edu/about/news/palomar-survey-instrument-analyzes-impact-of-starlink-satellites).

When LEO satellites re-enter Earth's atmosphere, they'll burn up. The debris [will *typically* burn up completely in a high-velocity cremation](https://www.space.com/6349-satellites-fall.html), but there are other possibilities we haven't experienced yet.

Since satellites can be used proficiently for *both* data and navigation, the people who control those satellites [have a bit more power](networks-computer.md) than cellular carriers, and deactivating GPS systems is a very real part of [wartime tactics](people-conflicts-war.md).

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

* * * * *

## Additional reading

[How Trilateration Works](https://ciechanow.ski/gps/)
