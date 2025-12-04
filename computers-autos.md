
# What autonomous vehicles are

"Autonomous vehicles" (AVs) are effectively [robots](computers-robotics.md) designed as cars on the road, which means all the risks of robotics apply, except at a *much* faster speed that can potentially kill people:

- They can be inherently stupid if not programmed correctly.
- Since the programmer must think of *every* "use case", they can't intuitively react.
- While [AI](computers-ai.md) can generate *some* intuition, [debugging](computers-software-redesign.md) it is an absolute nightmare.

This doesn't stop the allure of the narrative, though, that it could replace the tedious experience of [driving](autos.md). The prize is far too significant to *not* be desirable to typical auto owners.

The automation of AVs comes in degrees, and we've already flawlessly attained some of them:

- Level 0 - Completely manual controls. While some things like the parking brake may have an automated component, the driver is in full control.
- Level 1 - There is 1 automated element. The most common version of this is cruise control (or adaptive cruise control that slows from detecting vehicles ahead), where the driver is still in full control of steering and braking. These are as old as governors, and predates the automotive.
- Level 2 - Employs "advanced driver assistance systems" (ADAS) that help the driver. The driver still sits in the driver's seat and can fully control the car at any time, though, so the features are simply for safety.
- Level 3 - The car can do most basic tasks, but a human override is still necessary for various "edge cases" (e.g., rainy weather, steep hills, etc.). The automotive has complete autonomy at this point, so this is a major technological wall.
- Level 4 - The car can do almost everything, but someone can still override the tasks whenever they need. Safety concerns mean it creates very specific and contentious [political issues](power.md) and [moral questions](paradoxes.md).
- Level 5 - The car can do absolutely everything expected of it, and human interaction is gone, which also means a steering wheel and pedals aren't present anymore.

As it stands in 2022, AVs require tons of development and test data until they can legally drive at Level 3 with full responsibility, and still encounter very profound issues in commonplace edge cases like construction zones. The [marketing hype](marketing.md) definitely lies about [how soon it'll happen](trends.md). However, with enough [machine learning](computers-ai-ml.md) and data, it will eventually become commonplace.

Before cars, however, the more likely autonomous vehicle will be with drones. Drones are more lightweight, have a larger margin of error (since they're airborne), and the financial risks from drones crashing are nowhere *near* the scope that comes with cars (meaning less expensive [debugging](computers-software-redesign.md)).

## AV data

AVs require *tons* of input data to operate correctly, and uses at least a few different systems to regulate it:

- Detecting everything around the car with an array of [video cameras](engineering-camera.md) and "light detection and ranging" (LIDAR)
- Detecting [sound-based](computers-speakersmic.md) matters with [microphones](computers-speakersmic.md) from every angle, such as car horns or collision sounds.
- Using incessant [GPS tracking](logistics-navigation.md) to specify the location and feed a [learning model](computers-ai-ml.md) for all the *other* AVs, as well as complying with regulatory geo-fence requirements.

Conveniently, most vehicles manufactured after about 2001 have already added computers to at least *some* of their controls:

1. The control itself is designed to give the same feedback as a direct mechanical control (e.g., brakes giving pressurized resistance).
2. Information from the input travels into a [CPU](computers-cpu.md) as an input number (e.g., accelerator, brake, steering).
3. The computer then directly controls the component (e.g., throttle, brake, rack and pinion).

There are multiple experimental methods for rapidly mapping the environment around the vehicle, with new ones constantly introduced as possible features to make a more reliable automotive.

Further, most cars are also equipped with EDRs (electronic data recorders), so the information is already outputted as a computer-friendly format, and many parts of it are [standardized](standards-computers.md):

- The OBD-II sensor can have that data requested on command with a cheap reader.
- You can gather driving metrics by plugging in an OBD-II device that connects via a [wireless network](networks-cs.md).
- Many vehicles can also send data wirelessly, without an OBD-II port.

It's worth noting that the data on a technologically advanced vehicle is stored until it's erased.

- This exposes a consumer who sells their vehicle to the risk of the next owner seeing what their name is, their taste in music, geographic location of them and everyone they visit, and their daily habits.
- The manufacturers don't tend to care, and the user tends to be unprepared for this circumstance.
- Thus, it's wisest to either not use the built-in vehicle services or to delete the information before selling or scrapping the vehicle.

## EVs

Electric vehicles (EVs) are unrelated to autonomous vehicles, but they're often discussed at the same time because they're [new technology](trends.md).

Unlike ICE (Internal Combustion Engine), EVs are functionally a massive battery with an electric motor. Hybrid vehicles combine the benefits of both ICE *and* [batteries](engineering-electrical.md).

EV motors are almost guaranteed to have less torque than ICEs, so they're manufactured out of aluminum instead of steel (meaning they're less durable). However, they *also* frequently have safety-enhancing Level 2 features to mitigate more severe accidents, and their lighter frame makes dodging or diminishing a severe accident easier.

## Issues

All this extra complexity creates far more code and [computer hardware](computers-hardware.md) inside autos, and more complexity creates more [points of failure](https://adequate.life/fix/), which may be deadly on a highway. If the vehicles are all connected in an interdependent grid [network](networks-cs.md) (e.g., a robotaxi service), they might *all* go offline at once.

For example, when everything is controlled by software with a persistent wireless connection to the internet, the data is fully available to anyone, meaning it's technically available for [hackers](hacking.md), which could cause people to die from faulty software. Beyond bad actors, the owners of the vehicle can make modifications to their vehicles or reprogram the software, and large entities like governments or corporations could shut off the vehicle at their leisure. It's a [legislative](people-rules.md) nightmare.

Laws can also be very difficult to enforce with a vehicle that doesn't have a driver. Technically, the software developer is fully responsible for an AV that kills people, but society is quick to blame and punish, and it's not particularly fair to attack a software developer for an edge case they couldn't have predicted. Plus, there's no way to recruit developers if they know they might be criminally charged with manslaughter later.

Another AV issue comes through [insurance](money-insurance.md) issues. The AV's company is fully responsible for events that happen when the car's auto-drive is on, but the human driver behind the wheel is responsible when they're controlling the vehicle. When a human driver can override the automatic driving feature at any time, a person may panic and assume full responsibility for an otherwise-safe maneuver, leaving the human (and not the company) liable for damages caused by that split-second impulse.

Finally, the existence of AV making decisions creates [situational ethics](morality.md) issues that had once been pure chance. An AV can swerve to prioritize saving the driver, saving the passengers, saving the most vulnerable people (e.g., motorcyclists or pedestrians), or causing the least property damage, so [which should it prioritize](paradoxes.md)?

## More information

Safety features:

- [My Car Does What](https://mycardoeswhat.org/)
