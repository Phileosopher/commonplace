
[Keyboards](/keyboard/) were absolutely revolutionary for interfacing with a computer, but lacked finesse.

For one, keyboards are unruly because they can't easily identify things on a map. Though the arrow keys can be useful, they don't detect analog input.

Joysticks had been around for a while, but weren't always reliable or precise. A joystick goes back to a center after using it, or will sit at an odd angle without a spring. Either way is awkward for fine-tuned actions. [Games](/game-dev/) demonstrate this evidence: first-person shooters are easier to play with a keyboard and mouse than with a game pad.

The original "mouse" was a trackball, with the user operating a ball connected to rollers that corresponded with X and Y coordinates. Those numbers could then map to a location on a [screen](/screen/). One of the first trackballs was a top-secret Canadian military project in the 1940s that used a standard Canadian-style 5-pin bowling ball.

A trackball's most frequent drawback is bumping the ball when moving your hand to make a selection. There were many workarounds for the problem, but someone [hacked](/hacking/) a solution in the 1960s by inverting the X and Y rollers to roll on a surface instead. It was called a "mouse" because the cabling from the bottom of the early machines looked a *lot* like one.

Once the [graphical user interface](/ux-ui/) started adapting to the mouse, it became the standard, and [operating systems](/os/) started making the mouse a default peripheral with the presumption of a cursor. By the time [Microsoft Windows](/windows/) came around, operating systems *expected* the computer to have a mouse.

The cursor always sits at an angle because [it has copied from the old conventions of the first cursors](https://ux.stackexchange.com/questions/52336/why-is-the-mouse-cursor-slightly-tilted-and-not-straight). At the time, the screens were so low-resolution that it was easier to identify an arrow at a vertical angle and 45-degree diagonal line than two diagonal lines.

## Absolute vs. relative

A mouse measures relative motion, so it doesn't actually measure where it is in space, but it precisely measures the *difference* in starting/ending locations.

Very often, the software adapts the movement between distances. Generally, most operating systems use pointer acceleration, where moving the mouse across the screen faster makes it move farther. This subconsciously reproduces how [reality](https://gainedin.site/reality/) tends to work, where pushing something harder makes it move farther.

Relative motion means that you can move the mouse, pick it up to somewhere more convenient, and it won't register *that* change. It can typically be convenient if the cursor is in a bad location.

Of course, if you have the means, absolute motion is a more precise measurement. It'll measure the *exact* place you're at relative to the edges of the device. However, if you were using absolute motion for a relative object (such as a laptop touchpad), it would quickly become frustrating because of how much precision you'd need to have.

Plus, most operating systems that use absolute motion tend to get rid of their cursor, so you wouldn't have an easy time knowing where you're interacting unless the input was *directly* over the screen.

## Buttons

There was once a left, middle, and right click button. The left click naturally became the dominant selection button because we tend to point with our index finger, with the other two as context buttons with special features depending on the program.

However, the middle button was dropped because most interfaces only needed an additional "context menu" to then make a primary selection. For simplicity, Apple even dropped it down to *one* button for a long time, with ⌘+Click serving as the right click.

Of course, navigating many screens of information can be tedious, so the scroll wheel was a neat addition. By scrolling, you can skip having to hold down the arrow keys up or down to skim through information.

On [Linux](/unix/), the scroll wheel's middle-click is even more useful:

- It's a separate copy-paste "clipboard" buffer from the typical CTRL+C, CTRL+V that copies anytime something is selected:
  1. Select (Text A), then copy with CTRL+C.
  2. Select (Text B).
  3. Paste with CTRL+V, then middle-click to paste (Text A)(Text B).
- Middle-clicking an empty tab bar or an address bar opens a new tab in a file manager or browser, and middle-clicking the tab header will close it. The same is true for a dock/taskbar.
- Middle-click on a scroll bar will translate to the "Page Up" or "Page Down" key, context-depending.
- In fact, the Linux middle-click is so useful that a mouse *without* a middle-click can use a simultaneous left/right click instead.

## Latency

The electrical signals which come from a mouse abide by approximately the same standards as [almost every other cabled connected](/motherboard/).

The "polling rate" determines how frequently (measured in second-based Hz) the mouse sends updated information. It can range from 125 Hz (every 8 milliseconds) to 8,000 Hz (every 125 microseconds or 0.125 milliseconds). That information includes a few key pieces of information:

- Each button's status of being clicked or released.
- If absolute, the coordinates of the touchpad.
- If relative, DPI (dots per inch) of movement relative to the last polling.

A long time ago, mice had latencies that were about 1-5 milliseconds. However, error-correcting code means modern mice can often reach 80 milliseconds. Human perception never usually goes below 250 milliseconds (0.25 seconds), so people only intuitively "feel" something amiss when a computer is *really* slowed down, and often *not* directly from the mouse's signal.

## Adaptations

Since laptop computers started becoming popular in the 1980s, they created a touchpad or trackpad to replace the relatively cumbersome mouse. Instead of following a ball against wheels, the trackpad senses tiny pulses of electricity from our hands. It measures electrical pulses because it's *way* more precise than measuring heat or pressure.

One failed technology was to use a TrackPoint-style pointer. Instead of a cursor, it served as a small nub in the center of the keyboard that operated a bit like a [video game joystick](/game-dev/). However, it was unwieldy and awkward to use.

By making a particularly large trackpad that *also* detects pressure, artists can directly use a stylus to input with a pen. This creates an almost same-as-paper feel that makes visual design very effortless.

Further, by placing a variation of trackpad technology over a [screen](/screen/) called a "digitizer", the relative motion can become an absolute mapping to the screen.

Because of the difference in hand use, both touchpads and screens allow for "gestures", which are pre-programmed movements that allow for extra functionality:

- Swiping - reproduce a swiping effect with a specified number of fingers to imitate brushing something aside or scrolling through something (typically horizontally)
- Pinch zoom - two fingers moving closer or farther to zoom in/out, reproduces [function key] & +/-
- 2-finger scrolling - reproduces the scroll wheel effect with 2 fingers
- 3-finger tap/scroll - allows opening specific programs
- Edge swipe - swipe from the edge to open a contextual "dock" menu

However, when a touchpad is designed for accessibility (e.g., [mouth-based](https://news.mit.edu/2024/mouth-based-touchpad-augmental-0605)), the extra features become [bad UX](/ux-ui/).

Naturally, like [everything else about games](/game-dev/), people playing computer games have all sorts of sophisticated needs, so the best computer mice are typically gaming-grade. Many of them have additional customizable buttons, fantastic ergonomics, and often with gimmicks like lights or additional error-checking.

While there are many elaborate alternatives to the mouse, it probably will persist until [VR](/vr/) becomes a more prominent interface device. Even then, the mouse will always have its use, just like the barcode.
