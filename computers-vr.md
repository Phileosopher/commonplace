
# What VR is

As a concept, "virtual reality" (VR) is highly contextual to the culture that interprets it, and it can be interpreted through a few points of view:

- Augmented reality is essentially reality, but with adaptations to it (e.g., an overlay on top of what you see).
- Mixed reality is still reality, but a hybrid of reality and simulation (e.g., a sculpture that has virtual elements).
- Spatial computing is the domain of computing, but with *much* more space involved (i.e., the functions of a 3-dimensional [screen](engineering-screen.md)).
- Virtual worlds are built around the idea of *completely* removing someone entirely from reality.

VR depends on multiple other technologies to reproduce reality:

1. A [screen](engineering-screen.md) to clearly display something that looks like reality.
   - This has been reproduced fully and precisely, and the [graphics](engineering-graphics.md) will always keep improving.
2. Binaural [audio](computers-speakersmic.md) that clearly and accurately indicates direction.
   - This is pitch-perfect to reality, and there's not much necessary to develop in this domain.
3. A means for the user to smell what they're experiencing.
   - This *has* been created, but hasn't become popular enough to justify in most VR configurations.
4. A mechanism that allows the user to touch the world around them.
   - This hasn't been created, but it's *very* difficult to perform. The closest we can get right now is to use hand gestures and control pads.
5. Other sensory immersion (e.g., wind, heat, electromagnetic interference, proprioception).
   - While some of it has been part of VR in the past, everyone is so preoccupied with the other parts that they're not paying attention to it.

VR systems have the most promising practical use, and have degrees of immersion:

1. Non-immersive VR - a realistic virtual environment, but with limited involvement, and is ubiquitous for most [modern games](computers-software-gamedev.md).
2. Semi-immersive VR - aka "augmented reality" (AR), still the full experience of reality but with an overlay of assets and elements that provides additional information.
3. Fully immersive VR - a complete interaction with a hyperrealistic computer-generated environment.
4. Collaborative VR - essentially, fully immersive VR but with other users *also* using VR.

## History

VR development is always a slower [trend](trends.md) than many other tech trends because it's the convergence of other supporting technologies:

1. 1835 - Sir Charles Wheatstone created a stereoscope that used a mirror to show two pictures, one for each eye.
2. 1956 - a cinematographer named Morton Heilig created Sensorama, which combined full-color 3D video, audio, vibrations, smell, and atmospheric effects like wind. Later, in 1960, he created a "head-mounted display" (HMD) version of it, though it didn't have any motion tracking.
3. 1961 - two Philco Corporation engineers created Headsight for the military, which tracked head motion.
4. 1965 - Ivan Sutherland [created a paper describing the ultimate display](http://worrydream.com/refs/Sutherland%20-%20The%20Ultimate%20Display.pdf), which would reproduce reality so well that the user wouldn't be able to differentiate from actual reality. Later, in 1968, he created a NHD that used wire-frame shapes.
5. 1966 - Thomas Furness created the first flight simulator for the US Air Force.
6. 1969 - an artist named Myron Krueger created multiple virtual reality experiences with computers and video systems. Later, he'd make VIDEOPLACE in 1975, which didn't use goggles or gloves but used an entire room and tracked the users' silhouettes on a flat screen. It also allowed people to interact across different rooms (i.e., the precursor to a [social network](computers-sofware-webdev.md)).
7. 1972 - General Electric Corporation expanded the flight simulator to a 180-degree field of view with 3 screens around the cockpit.
8. 1977 - MIT created Aspen Movie Map, which allowed users to drive through Aspen City, Colorado using photos from a car that drove through the city.
9. 1979 - McDonnell-Douglas Corporation created the VITAL helmet for military use. The HMD's head tracker followed the pilot's eye movements to match computer-generated images.
10. 1982 - Two people created Sayre gloves, which monitored hand movements with light emitters and photocells, which converted finger movements into electrical signals.
11. 1985 - VPL Research Inc. was the first company to commercially sell VR goggles and gloves, including products like the DataGlove, EyePhone HMD, and Audio Sphere.
12. 1986-1989 - Later, Thomas Furness created a flight simulator called the Super Cockpit that used computer-generated 3D maps, advanced infrared/radar imagery, and the pilot could see and hear in real-time. At the same time, British Aerospace created the Virtual Cockpit to include [speech recognition](computers-speakersmic.md).
13. 1989 - Crystal River Engineering Inc. developed the audio-based component of NASA'S VIEW project (a training simulator for astronauts), and developed the first binaural 3D audio processing.
14. 1990 - the first line of VR arcade [games](computers-software-gamedev.md) was called Virtuality.
15. 1994 - SEGA released a motion simulator arcade machine called the VR-1, and VictorMaxx released a headset called CyberMaxx.
16. 1995 - Nintendo released the Virtual Boy console to represent 3D graphics in monochrome. It failed within a year miserably because it was in red-and-black (and gave eye strain), the software was [poorly maintained](computers-software-redesign.md), and it was uncomfortable to use. At the same time, Virtual IO released the I-Glasses and Forte released the VFX1 Headgear.
17. 1997 - Georgia Tech and Emory University researchers used VR for [war zone](people-conflicts-war-why.md) scenarios to treat soldiers with PTSD via exposure therapy.
18. 2001 - The first PC-based room was SAS Cube, which led to the Virtools VR Pack.
19. 2007 - Google introduced Street View, which eventually included photos of most roads across the world. In 2010, they added a stereoscopic 3D mode.
20. 2012 - The Oculus Rift was released by Luckey through a Kickstarter campaign, which was subsequently bought by Facebook in 2014.
21. 2014 - VR became a consumer trend: Sony released Project Morpheus for the PlayStation 4, Google released Cardboard as a low-cost smartphone stereoscopic viewer, and Samsung released Samsung Gear VR.
22. 2016 - Nintendo released Pokémon GO as an AR experience, with Pokémon being overlaid over a phone's [camera](engineering-camera.md). This created some issues because some people were being *very* unsafe with auto traffic with the intent to play the game.
23. 2016-present - the public had complete access to VR headsets with binaural audio, a screen, and control pads for each hand, and they've been becoming more affordable over time.

## Uses

There are several major reasons people create VR:

1. Military training - it's a conceptually effective solution to train soldiers without them seeing combat.
2. Military enhancement - it can theoretically assist in helping soldiers become more effective at war.
3. Military support - [robotics](computers-robotics.md) and drones can allow soldiers to remotely control the experience, thereby protecting them as assets.
4. Business training - it's a conceptually effective solution to train people how to interact with something.
5. Business enhancement - it can theoretically assist in workers becoming more efficient.
6. Consumer enjoyment - people are willing to pay for the product because it's fun (e.g., [games](computers-software-gamedev.md)).

## AR

AR uses several approaches to track reality:

- Marker-based AR - recognizes an image, then displays the augmented reality content on top of it, which requires the image to have distinctive-enough features and enough contrast for the computer to detect it.
- Markerless AR - more advanced, and allows *no* context for displaying digital content, and only requires a preferred surface or floating in midair.
- Location-based AR - requires specific location information to present information.

## VR uses

One of the most common uses of VR is "virtual try-ON" (VTON), which allows someone to test how a product will look before purchasing it.

One very interesting reality about VR is that it triggers the same space-based theta waves [in the brain](science-neurology.md) as if the person were actually present somewhere. Someone who [becomes familiarized](understanding.md) with the technology can effectively [imagine](imagination.md) the experience so heavily that their mind creates the illusion that they're actually there. This can have tremendous implications for [therapeutic healthcare](body-health.md) and [education](education.md).

VR also can serve as an effective [exercise aide](body-exercise.md), especially for people who otherwise would *not* exercise.

## Downsides

As close as we've come to imitating reality, there are issues with VR.

Firstly, the hardware has issues:

- The screen on a standard HMD is 120 FPS, and it's right in the person's face. This can create *awful* consequences for anyone susceptible to motion sickness from high-frame rate [screens](engineering-screen.md).
- For people who wear glasses, VR headsets are awkward and uncomfortable to work with, though you can get prescription glasses *for* the headset directly.
- The hardware is often very finicky, and all the cameras and screen lenses *must* be regularly wiped to prevent dust and oil interfering with the inputs.
- HMDs can get very heavy after keeping it on your face for a few hours, and it can cause chronic strain.

The software is often poorly designed as well:

- Most VR designers have competing ideas on how to approach the concept, and each variation of the product requires a new [learning curve](understanding.md) to adapt to it.
- Since they're frequently accompanied by new input devices as well, most of them haven't adopted decent-quality [UX](engineering-design.md) for navigation.
- Many of them don't have critical features like built-in focus-adjustment or the means to use a [keyboard](computers-keyboard.md) and [mouse](computers-mouse.md).
- Most of the software is *not* backwards-compatible with a [conventional screen](engineering-screen.md), which can severely limit the user's options if they wish to display something.

The hype around VR is overblown as well. Like other [trendy tech things](trends.md), it may be really *neat*, but it doesn't necessarily fulfill a clear *need*. It doesn't help that the market is small enough that the [marketing](marketing.md) never distinguishes clear product lines that focus on specific needs:

- Gamers want *extremely* reliable feedback and *complete* immersion, which means the experiences should rival or overshadow what reality can provide.
- Business professionals don't care much about immersion, but want it to be *very* reliable, since they need to know it'll work for their collaborative needs.
- Artists and creatives want something that can make them more efficient, don't care as much about reliability, and would prefer high-quality [UX](engineering-design.md).
- Engineers and programmers want feedback *much* more than immersion, since they're designing highly technical things and want to know if something goes wrong. Most of them, as well, aren't as obsessed with reliability.

Given that VR headsets collect a *lot* more data than a typical computer, any [data collection abuse](faang.md) issues by large organizations can be exponentially worse.

When you include audio into the experience, HMDs are *very* exclusionary. You'll be working or playing by yourself, and will *not* detect any other people around you.

Another issue comes from specifically *AR* systems. While it may seem useful, *any* aberration from reality (such as a targeting reticle that bounces around) can make the user about as disoriented as if there was a fly present or smudge on the glasses.

Currently, as of the early 2020s, VR is a fine-enough upgrade to your screen experience, but has arcane failings that won't be resolved until much later. A lot of the surrounding hype (e.g., Facebook's Metaverse) has largely collapsed, and it's likely the OS development in that area won't yield much in the short term either.

## More information

[Working From Orbit. VR Productivity in (or Above) a WFA...](https://medium.com/immersedteam/working-from-orbit-39bf95a6d385)
