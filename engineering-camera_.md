
The camera's history and development is *much* older than computers, though at this point the technologies have mostly converged.

For several thousand years, people figured out light could travel through a small hole (officially called an aperture) and produce an upside-down image on a flat surface (camera obscura). This was because the light waves were traveling in a straight line, so the hole created a cone of light on one side that mirrored the other. People could trace the visual image and reproduce it.

By combining the aperture concept with something that darkens when exposed to sunlight (such as silver salts), they were able to create a photographic plate. Putting that plate inside a closed box, then opening it for a fixed amount of time, creates a color-negative of the image you wanted, which you could make a color-accurate image if you reversed the colors. The original photos took *hours* to capture, which is why nobody smiled in old photos.

Instant-exposure film was invented in the 20th century, meaning you only had to open the aperture for a split-second and could capture motion. The 20th century saw cameras become more portable (and eventually fit the film on a reel) and cameras could be made so cheaply that they could be *disposable*!

Digital cameras were first used by Russell Kirch in 1957 to take a 176-pixel photo of a baby, and operate on a different concept. Though the aperture opens up the same as a film camera, the technology where the light hits is effectively the reverse of a [computer screen](engineering-screen.md).

There are different patterns to capture the light. One of the simplest is a Bayer filter, which has 2×2 squares of a red, blue, and two greens. There are two greens in this setup because the [luminous efficiency function](https://en.wikipedia.org/wiki/Luminous_efficiency_function) means green most heavily correlates with perceived brightness.

Digital panels either use a CCD (charge-coupled device) or CIS (CMOS image sensor) to represent each pixel, then fill in the gaps between the color sensors to convert the information into pixels ("demosaicing"). When light hits each pixel, the photons convert into electrical impulses using the [Nyquist sampling rate](https://web.archive.org/web/20210619082520/https://microscopy.berkeley.edu/courses/dib/sections/02images/sampling.html) for each of the primary colors, which can then be stored, transferred, or retrieved at will.

The concept is easy to understand beyond the visible spectrum, which is effectively how infrared cameras work as well, though they're *much* harder to create because the output must be modulated downward to visible light.

## Configuration

Generally, for high-quality camera work, you'll want to purchase a camera body as a standalone unit, then buy the lenses separately. You can buy cameras with kit lenses, but they're not usually as good.

The focal length determines how zoomed-in or zoomed-out something looks, with longer zooming in farther. People look thinner with long focal lengths, but they're impractical for short-range. Very short focal length can distort images.

Exposure determines how much the camera lets light in, which is determined by 3 factors:

1. Shutter speed, which is the amount of time light can hit the sensor, measured in seconds. This can range from 1/1000 s to 1 s.
2. Aperture, which is the size of a circular hole that lets light in, measured in f-stops (which is the ratio of the lens focal length divided by the lens diameter). This ranges from f/16 all the way to f/2. Wider apertures make the images feel softer, while narrower apertures sharpen the image at the risk of being darker.
3. In digital cameras, cameras use an [ISO standard](standards-computers.md) that represents a light sensor sensitivity scale that ranges from 100 to 25,600. There's a base ISO that conforms to the specification the camera came with, but it can be configured upward to gather more light, at the risk of generating noise in the image.

- Doubling any of them adds a "stop" of light (e.g., 1/500 s to 1/250 s is a stop, and 1/250 s to 1/125 s is another stop).

Manual focus lenses require tuning by the photographer, but autofocus adapts the focus to the objects in the frame. The [algorithms](computers-programming-algorithms.md) in most modern cameras are good enough that autofocus is almost always better for anything but still photography.

## Artifacts

There are a few types of "artifacts" from how cameras capture images. They're errors between the actual representation of the image as someone would perceive it compared to the image represented on a screen.

"Hot spots" come when one part of the image is more exposed to light than another, washing out that area compared to the rest.

"Diffusion" is an artifact from bright sources that spreads out from the light source to wash out other parts of the image. "Bloom" is from *very* bright sources.

The shape of the lens will distort light and create "chromatic aberration", where the focus of the lens will change the hue of a color.

A lens can only focus on certain things at once while blurring out other elements in an image, which creates a "depth of field" as the range between the nearest and farthest it can create a crystal-clear focus at the same time.

An object will create "motion blur" if something is moving particularly fast or the aperture timing was open for too long.

## Post-processing

Most artifacts can be at least partially compensated by software after the initial capture, but many artists intentionally disable those features (such as for movies), and even many [graphics developers](engineering-graphics.md) (especially for [games](computers-software-gamedev.md)) try to *recreate* those artifacts!

In fact, post-processing has been how smartphones utterly *destroyed* the dedicated camera market. It's logistically impossible for a millimeter-deep lens distance to compete with several inches of space, and smartphone cameras have had to compensate by making weird-looking non-spherical lenses to refract the light. But, post-processing can effectively remove many of the issues which may potentially present in non-spherical lens photos.

"White balance", or color temperature, determines how much the color leans blue or red.

While most post-processing features can be helpful, digital zoom is nothing more than a dynamic cropping feature, which would be better performed on a desktop computer later. However, it allows for more zoom in the [marketing](marketing.md).

## Imperfect

While post-processing can be very useful, it can become ineffective as well. If the operating system does *too* much to raw photos, the result will look inauthentic or strange, especially with human photos.

Post-processing isn't exempt from [politics](power-types.md), either. Film industry experts, for example, have made deals with [television](engineering-screen.md) companies to dampen high-resolution pixelation for skin tones.

Further, perspective in our eyes works differently than perspective in a photograph. Photos capture the raw information evenly across a panel, while we capture *more* information at the center of our eye's focus than on the edge. This makes the center of something look somewhat larger by comparison to everything else, and photos are incapable of capturing that distinction.

Among the [market](economics.md), webcams in particular are very shoddy. They possess low-quality post-processing software, *very* cheap components, and are small enough to fit snugly on the side of a [computer screen](engineering-screen.md). Professional-grade cameras or phone cameras networked to a computer are generally a better choice if you want a more presentable image for video streaming and online meetings.

* * * * *

## Additional reading

[The Ultimate Guide to Lens Design Forms](https://www.pencilofrays.com/lens-design-forms/)

[How Does Perspective Work in Pictures?](https://aaronhertzmann.com/2022/02/28/how-does-perspective-work.html)

[Photography for geeks](https://lcamtuf.coredump.cx/photo_basics/)

[Cameras and Lenses](https://ciechanow.ski/cameras-and-lenses/)
