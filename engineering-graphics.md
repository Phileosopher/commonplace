
# How graphics work

Getting computers to display information on a [screen](engineering-screen.md) isn't necessarily easy, and most computers before the 1970's represented information as raw language outputted to a [printer](engineering-printers.md).

The first graphical interface was called Sketchpad, and [was created by Ivan Sutherland in 1963 as part of his PhD thesis](https://www.youtube.com/watch?v=6orsmFndx_o). It essentially involved pressing a pad with a wired stylus while pressing buttons on the side of the screen, which indicated what form the device would draw.

## Vector vs. raster

There are two major approaches to displaying graphics on a screen:

- "Vector graphics" - running an electron horizontally across a screen using [algebra](math-algebra-cs.md) to leave a line (like with oscilloscopes), which is how the old [Atari arcade games](computers-software-gamedev.md) worked, and is very effective even with low-powered computers to create 3D effects.
- "Raster graphics" - making a grid matrix of pixels, which is how screens have been rendered ever since.

When rastering to different sizes of pixel (e.g., 1024x768 resized to 1920x1080), the resolution can create weird feedback called "aliasing" that forms jagged edges (informally called jaggies). To prevent jaggies, graphics software often has "anti-aliasing", which comes in a few forms:

- Spatial anti-aliasing "supersamples" by taking a higher resolution's image, then samples the extra pixels that wouldn't show up on the lower-resolution, then shrinks the image down to the original resolution with the averaged-out colors.
  - SSAA (super-sampling anti-aliasing) was the first form of anti-aliasing, and tends to adversely soften sharp horizontal and vertical lines. It also requires tons of computing power because the *entire* image must be processed before the jaggies are smoothed ("full-scene").
  - MSAA (multisample anti-aliasing) draws and smooths out the edges of polygons, but it doesn't smooth out the textures, which can cut down on processing power a little bit at the expense of the poor-looking textures.
  - CSAA (coverage sampling anti-aliasing) was made by NVIDIA, and detects whether a polygon is present in the image, then only supersamples the pixels that have polygons that might have jaggies.
  - EQAA (enhanced quality anti-aliasing) is pretty much AMD's version of NVIDIA's CSAA.
- Post-process anti-aliasing will slightly blur each pixel after it's rendered, then the GPU will determine the edge of the polygon by comparing whether the colors contrast between the pixels. This one is very fast, but can also make the image blurry in the process.
  - MLAA (morphological anti-aliasing) was made by AMD, and is the standard post-process anti-aliasing feature.
  - FXAA (fast approximate anti-aliasing) is NVIDIA's version of AMD's MLAA.
  - TXAA (temporal anti-aliasing) uses a complex hybrid of supersampling and blurring to create a graceful feeling of motion, but uses a lot of graphics power to do it.
  - SMAA (enhanced subpixel morphological anti-aliasing) smooths pixels with the same blurring method as MLAA/FXAA, but also uses supersampling to sharpen the entire image. It's popular because it uses less computing power than MLAA/FXAA.

## Rastered pixels

Pixelated screens have been the standard since the 1980's because of their versatility. By using a grid, absolutely anything can render without too much trouble. It also happens to be how the data expresses on [printers](engineering-printers.md), so it's easy to migrate from one to the other.

The [screen](engineering-screen.md) pulls information from a "screen [memory](computers-memory.md) map", which is a designated part of the RAM set aside for screen information.

Each pixel color is contained in memory. This is a *lot* of information compared to other peripherals like the [keyboard](computers-keyboard.md) or [mouse](computers-mouse.md). A 1024x768 screen (the standard screen size c. 2005) requires 786,432 pixels.

For a synchronized experience, each screen is maintained on an "aspect ratio", which allows screens to give a comparable image even when different screens have differing amounts of pixels:

- 4:3 - common size originated from televisions moving up from 640x480, 800x600, and 1024x768.
  - The standard TV of the past was 352x288 for PAL (the international standard), and 352x240 for NTSC (the USA standard).
- 16:9 - widescreen, moving up from 1280x720, 1365x768, and 1920x1080.
  - There's an off-kilter standard of 16:10, which adds a little more height.
- 5:4 - a squared-off format that didn't last long, at 1280x1024.
- 1.85x1 and 2.35x1 - the standard for digital cinema with non-square pixels, moving up from 1920x1440, 2048x1536, and 4096x3112.

Computer screens are constantly getting better, but the pixel density of mobile devices typically lag behind larger screens.

Some standard sizes are described by encoded jargon:

- 960x540 - 540p or qHD
- 1280x720 - 720p or HD
- 1920x1080 - 1080p, Full HD, or FHD
- 1920x1440 - DataCine native
- 2048x1080 - 2K, though it may also refer to 2048x1536
- 2560x1440 - 1440p, QHD, QuadHD, WQ
- 3840x2160 - 2160p or UHD
- 4096x2160 - 4K, though it may also refer to 4096x3112
- 5120x2880 - 5K
- 7680x4320 - 8K or 8K UHD

## Video quality

A video in its purest form, is a stream of a *lot* of raw data. Compressor/decompressors ("codecs") permit storing that information without as much memory:

- They'll remove information that's redundant (e.g., groups of pixels that are the same color).
- They may condense patterns of pixels that frequently represent in videos.
- Some codecs like H.264 and H.265 can *dramatically* compress data, upwards of over 50% less.

Codecs are either "lossy" or "lossless", proportional to how much data is lost during compression.

To keep video files together, they're played synchronously in a container, often alongside [audio codecs](computers-speakersmic.md). It works a bit like a virtual machine, but with *extremely* specific specifications. Some of the most popular containers are MP4, MKV, AVI, FLV, and WEBM.

The pixellation of the [camera](engineering-camera.md) represents the upper threshold of a recording, though post-processing software can fill in pixels to give a smoother image.

Some containers, such as WMV, can include built-in [DRM](legal-ip.md).

## Color

In a black-and-white screen, each pixel is represented simply by one bit, with 0 being white and 1 being black (or the other way around). It's relatively simple.

To give the illusion of color, some clever designers used colored or artistically designed panels to give a colored backdrop. It was cheating, though, since the computer was still non-colored.

Legitimate computed color gets far more complex, and is far more relative than most people realize.

The actual numbers used to represent colors have no inherent meaning, and it goes back to the physics of light.

- Our eyes perceive brightness on an exponential, not incremental, scale. This means that we doubling the number of photons would *not* feel like the brightness doubled.
- There are a variety of [standards](standards-computers.md) available to represent this: linear progression, exponential progression, or a hybrid of both.
- The numerical barriers for these colors are defined as "color spaces". Computers do *not* represent the full range of colors, and simply create constraints for the sake of what's most convenient.
- "Unbounded" color values are free to be more precise compared to bounded values, but they're a little more fiddly to work with [memory](computers-memory.md) constraints.
- The "color temperature" is a tweak that allows colors to represent more toward red-leaning (warm) or blue-leaning (cool).

Each colored pixel has 3 lights (red, blue, green) that shine at varying intensities, which can combine via additive light to form any color.

- These varieties of color are based on the number of bits stored in [memory](computers-memory.md) for that purpose: more variations require more memory.

The 3 most popular color configurations right now are 16-bit, 24-bit, and 32-bit.

- 16-bit color is fine enough for any normal use, though games and high-resolution movies may suffer a little. By using 16 bits, there are 65,536 ranges of color.
- 24-bit color covers every common visual need for seeing the entire range of color. Each of the 3 lights gets 8 bits (effectively 256 intensities), which combined together can make 16,777,216 possible colors. This represents as a 6-digit hexadecimal (e.g., #ff7452), though it can sometimes convert to an RGB format (e.g., rgb(255, 116, 82)).
- 32-bit color adds a layer of complexity. By incorporating an alpha channel that blends pixels, each pixel receives an additional 8 bits, bringing the total to 4,294,967,296 possible configurations per pixel.

The memory required for pixelated color becomes daunting to imagine:

- At 32-bit color, each of those 3 colors in each pixel has 32 bits, making 96 bits per pixel and 75,497,472 bits total.
- With a 64-bit word width in [memory](computers-memory.md), that means the computer needs 1,179,648 registers to store 1 screen.
- The average refresh rate of a computer is about 60 Hz, which means 70,778,880 registers *per second* of use.
- A faster refresh rate means even *more* memory use.

To fine-tune [design](engineering-design.md) needs, there is another way to work with color from a different point of view called HSL or HSLA:

- Hue - a degree on the color wheel from 0 to 360, with 0 representing red, 120 representing green, and 240 representing blue. Colors can generally lean into either a red or blue gradation as well.
- Saturation - the color's intensity, represented as 0% up to 100%, with shades of gray incorporated into the raw color.
- Lightness - the brightness of the color represented as 0% up to 100%, typically expressed on a [screen](engineering-screen.md) through the light settings.
- Alpha - Represents as how opaque the color is ("opacity"), with 0.0 being fully transparent and 1.0 being not transparent at all.

Thankfully, even though the colors have no precise numerical basis, Grassmann's laws indicate that mathematically adding 2 colors together will yield a resulting color that's the same as if you combined both those colors. It means, plainly, that they can be converted back-and-forth numerically if you know the standards.

## Render needs

Memory management is a big deal with high-intensity graphics needs.

Many large-scale [enterprise](computers-distsys-enterprise.md) endeavors require pre-rendering (e.g., Pixar animations). In this case, the rendering is dropped into a queue that many computers in a [distributed system](computers-distsys.md) pull from, and the computers run nonstop for many, many days.

But, the largest consumer-grade need, by far, is for playing [games](computers-software-gamedev.md), with "computer-aided design (CAD) software lagging behind by a significant margin from not needing a half-second update for absolutely everything. These often need "dedicated graphics cards" that plug into the motherboard, since an integrated graphics controller inside a CPU's chipset won't cut it.

Thus, there are many tricks to maximize the hardware. Many of them were [hacks](hacking.md) designed with the constraints of the time, and have often become dated as a result.

## Hardware hacks

On older games, the hardware was severely limited, so it wasn't able to update everything all at once. So, the developers built out a divide:

- A static background that either didn't change, or it simply scrolled by moving color information over line-by-line.
- A dynamic foreground comprised of "sprites" that moved and updated frame-by-frame, which most importantly included the player's character and enemies.
- Later, as technology improved, even the *background* could have moving sprites to give an additional level of immersion.

Once the technology improved enough, the scrolling effects could be offset on different layers, known as "parallax scrolling". The clouds, mountains, and a nearby-looking background near the ground could all scroll at different intervals, for example. This gives a tremendous illusion of movement.

For a long time, "wireframe" models were the only way to capture a 3-dimensional view, which mostly used the above-mentioned vector graphics technology imposed onto a pixellated screen. Once the technology became advanced enough, the graphical designers were able to fill in the shapes to create polygon-based art. Flight simulators were the first to embrace the idea fully, but many games at first would use polygon-based rendering for the characters with paneled or static backgrounds. Polygons for *everything*, though, became industry standard by the early 2000's, though it has generally not aged well.

One of the short-lived divergences from wireframe modeling involved using "voxels" (volumetric pixels) to use a 3-dimensional grid of blocks to capture a game world. It looked awkward, but about as effective as the polygons of the time. However, increasing polygon counts was less CPU-intensive compared to shrinking voxel size, so the trend died quickly.

To compensate for the increased load in graphics, one clever workaround was to use "raycasting", which draws lines out from the 3D-modeled perspective of the user, then only renders the portion of the world that the user actually sees. This can also be coupled with the illusion of "motion blur" caused by [cameras](engineering-camera.md) to further cut down on graphics processing requirements.

All this additional 3D modeling became labor-intensive for the CPU. So, instead of rendering the graphics inside the software, it became critical to have the rendering handed off to another source. That extra source is either through a separate graphics chip or through an [emulated](computers-distsys-vm.md) graphics chip that pulled from the same CPU.

Instead of outright rendering largely chaotic things that would be hard to render (like fire or a bomb explosion), most of those use a "particle system" to create "particle effects", which reproduce the experience with predefined random 3D movement instead of having a fixed appearance frame-to-frame.

## Developer hacks

Graphics rendering is time-consuming as well as GPU-consuming, and the time required for developers to create is now more of a constraint than hardware capacity. So, developers use tricks to cut down on their required work.

"Procedural generation" requires setting a series of rules for the environment, then telling the computer to start rending. As a simple example, a matte two-dimensional blade of grass may only be a certain range of pixels wide and high, and may only be curved a certain amount, so the rules can create an indefinite procedurally-generated field of grass at a fraction of the time to render each blade of grass.

## Animation styles

To capture real-life motion into older games, one of the most tedious forms of animation required "rotoscoping", which involved graphically reproducing a real-life video, frame-by-frame (e.g., Prince of Persia).

One short-lived technique that embodied the 1990's involved dropping digitized sprites into a game directly. It looked a bit odd because there was no way to reliably capture shadows, so it always felt surreal to look at. Adding real-life video into games started getting particularly dumb once the technology allowed complete videos.

Later, 3D games have largely replaced rotoscoping with "green screen" technology used in movies to capture motion, where people have brightly colored indicators on a colored background, which makes it easier for computers to note movement between frames.

After games became effective enough at creating realistic-looking 3D models, it became important to add lighting effects to improve the feeling of realism.

- Flat shading requires relatively lightweight processing power, and adds gray proportional to each primitive (in effect, every triangle). It looks awkward.
- Gouraud shading is the first effort to introduce gradations of light without calculating it per-pixel. The lighting is calculated from a source, then uses "interpolation" to diminish the shading as the object is angled farther away from the light source. It gives a very artificial-looking but believable appearance.
- "Variable lighting" adds a granular layer of referencing a light source, then "ray tracing" the light and adding gradations of gray to the simulated shadows. This is done per-pixel.

To hide the graphical limits of older games, many games introduced a fog element, where further distance was grayed-out, mostly by adding more gray relative to the player's distance.

For the most part, 3D models have simply beefed up the above to increasingly aim for photo-realism:

- More polygons
- Creating curvature with the polygons instead of straight lines (especially with many "Bézier curves")
- More lighting and shading elements
- More things on the screen at once

However, it's become very difficult to aim for complete photo-realism because reality is *vastly* complicated compared to a digital representation or simulation.

"Cel shading" takes a shift away from realism by stripping down the color palette to create a solid effect that contrasts where shadows begin. While the appearance looks a little cartoon-like, it represents a striking visual style and is *highly* time-resistant; Jet Set Radio and The Legend of Zelda: The Wind Waker don't feel like dated products of their technological time.

To give the impression of motion and interaction, a static image can give a wobble effect, where every pixel wobbles on its own. It can give a cartoon-like effect while feeling interactive. One of the earlier implementations of this was Super Mario World 2: Yoshi's Island.

### Web development styles

To give an impression of movement or fill in an otherwise bland view, backgrounds can be "gradients" or have dynamically updated content on them.

## Additional reading

[LCD monitor technology and tests](https://www.techmind.org/lcd/index.html)

[Color Spaces](https://ciechanow.ski/color-spaces/)
