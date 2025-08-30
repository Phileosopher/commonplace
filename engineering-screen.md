
# The computer screen explained

Ever since the computer screen became affordable, we've been prioritizing it over the [printer](computers-printers.md) to visually see most output on a computer. It's now *way* cheaper and faster, so it's a core peripheral of most computers.

Unlike the printer, screens use visible light instead of reflected light. So, instead of using subtractive primary colors of cyan/magenta/yellow to reflect the wavelengths, screens combine emitted wavelengths with additive colors. They found out that 3 colors (red, green, blue) can combine to make *all* other visible light.

## Implementations

Most computer screens use the abstraction of [pixel-based rendering](engineering-graphics.md), which allows them to operate side-by-side on the same computer without any issues in portraying the information.

Most pixel-based screens are relatively straightforward:

1. Each pixel has a controller for each of the 3 primary colors of red, blue, and green, activated by electricity.
2. Optionally, if the pixel isn't self-lit, a backlight feeds light through the pixel from behind.

Cathode ray tube (CRT) screens were more popular at one time.

- The implementation involved a gigantic bulb that shot electrons through a vacuum onto a semi-rounded phosphor plating. From there, filters on the front of the bulb would then fine-tune the intensities of each pixel.
- The electrical connections would often accrue dust or wiggle loose, which meant slapping the side of the screen often resolved signal issues.
- They're largely outmoded now because they're bulky and have a bad tendency to burn an image onto the glass if the image stays the same for too long ("screen burn-in").

Plasma screens use tiny pockets of mercury gas, which turn to plasma when ionized by electricity and emit ultraviolet rays, which run through 3 different colors of phosphor cells to create an image. Each pixel in a plasma screen is emitting its own light, so it doesn't need a backlight.

"Liquid crystal display" (LCD) screens uses long horizontal fluorescent tubes as a "backlight". The voltage for each pixel rotated it to allow light to pass through. It became reliable enough that it surpassed CRT sales by 2007.

"Light-emitting diode" (LED) displays are precisely the same as LCD screens, except that they use many small LEDs instead of fluorescent lamps. LEDs themselves are essentially semiconductors. The term is mostly a [marketing](marketing.md) term, since it's mostly the same technology as LCDs, though the LEDs can be coated in plastic and used in arrays separately (such as sports stadium or bus station signs).

Historically, plasma was a better screen than LED, but LEDs have improved:

- Plasma has a more stark contrast for the color black, since the light can be turned off. LED always has a backlight, but has improved in blocking light to where it's competitively the same or better.
- LEDs are significantly brighter displays than plasma, though plasma was much better for viewing in a dark room.
- Screens are often difficult to see from the side, but the fact that plasma emits light from each pixel means it has a wider viewing angle than LED.
- Plasma screens have a higher refresh rate (see below) than LED screens.
- While plasma screens manage each pixel, LED screens have a host of issues that come from a backlit panel (e.g., darker edges, uneven color).
- Plasma is more susceptible to burn-in than LED, though they've gotten dramatically better over the years.
- Plasma screens are typically thicker and heavier than LED screens, and tend to burn lots more electricity and get very hot.

The next evolution of plasma is "organic light-emitting diode" (OLED), which effectively does the same thing but better. However, different sub-pixels may age at different rates, and it's still sensitive to direct sunlight and can be prohibitively expensive.

To compensate for OLED, LED now uses "quantum dots" (small pixels only a few nanometers long) over the pixels to create an even more granular image with "quantum light-emitting diodes" (QLED).

Many limited-use computers, like clock radios or air conditioner controllers, don't need much for a visual display, so engineers settle for cheap, large panels shaped for simple character expression (typically LCD) and illuminated by a backlight.

Since about 2010, computer screens and televisions have been functionally the same. The only difference, beyond the television having its own fully functioning proprietary [computer](computers-hardware.md) inside it, is that the television [tracks more user data and may advertise products for users to purchase](faang.md).

One relatively newer technology with tons of promise is e-ink. It uses negatively charged black pigment and positively charged white pigment on a type of paper, which will jump to the top of the screen based on the charge. This is easier on the eyes because someone is viewing pigmentation (like with [printed](computers-printers.md) paper) instead of visible light. Most of its screen implementations also *feel* like paper. The only downside is that paper is relatively cheap, while these paper-like devices would cost at least 100x the price of a notepad even if it was made as cheaply as possible.

## Illusion of motion

A computer screen outputs a sequence of very rapid images, and most of the technology on a computer screen is borrowing directly from televisions.

We interpret everything on the screen as if it were moving because of the "Phi phenomenon", where our brains fill in the gaps between similar images when they run together really fast.

People will often feel nauseous if the FPS (frames per second) falls below 24 FPS, especially below 16. Television ran at 30 FPS for a long time.

At around 10-12 FPS, the frames feel like a slideshow.

Typically, computers run at 59-60 FPS (frames per second) because most people wouldn't notice any performance difference above that number.

The "sampling" of images (or "frames") typically stays at about 60 per second (Hz) in most modern computers, though the internal refresh rate of plasma TVs can go up to 600 Hz.

120 FPS is a preferable rate for high-intensity activities (e.g., [VR headsets](computers-vr.md)). However, it has the tendency to give people headaches and nausea if they're conditioned to 60 FPS devices and are perceptive enough.

## Reusable

Since the screen is an array, and modern ones typically have a backlight, computer screens can easily be repurposed:

- As long as there's a controller, laptop screens can be converted into standard computer monitors.
- By removing the backlight and other unnecessary layers, a screen can be laid on top of an overhead projector to create a projection video screen.
- Smaller LCD screens (such as on old cellphones or landline telephones) can be reused to make small readout displays and smart watches.
  - Placing them behind a mirror can create a smart mirror.
