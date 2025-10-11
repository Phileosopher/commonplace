
# How spacecraft are designed

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

Each satellite must be *very* reliable, above 99.9%, since [maintenance](https://adequate.life/fix/) and hardware upgrades are nearly nonexistent or prohibitively expensive.

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

While [GPS devices](logistics-navigation-gps.md) simply require a receiver, satellite data devices require a "transceiver" to successfully send the information.

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
- [Insurance](money-insurance.md) - historical imaging can help investigations into fraudulent claims.
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
