
# What the computer keyboard is

Converting the keyboard used for [typewriting](language-writing.md) into a useful computer input may probably be the most convenient thing that has ever happened to computers.

Before keyboards, people had to send information to a computer with holes in punch cards or paper tape. If you've ever taken a standardized test where you fill in the numbers with a pencil (sometimes called a scantron), imagine having to [code](cs-langs.md) a computer that way.

We still use barcodes (e.g., homogenous retail products) and magnetic ink (e.g., bank checks) that use the [older technology](people-trends.md).

- As an aside, barcodes read the *light* spots on the code, not the dark spots like your intuition would have you believe.

Almost everything else has either moved to keyboard-based input or is supplemented with it. Even completely screen-based interfaces (e.g., mobile devices) often use an on-screen keyboard.

## Long-term health

Anyone who sits at a computer all day has a [major health risk](body-health.md), and keyboards are a huge contributor to that.

The ideal ergonomic placement of a keyboard is for the person's hands to be at rest. Therefore, counter to many keyboard configurations, the best place for the keyboard to be is sloped *downward* from the user.

## Closing circuits

When you press a key on a keyboard, you're closing a circuit. That circuit sends an electrical pulse to the [CPU](cs-cpu.md) with a binary code representing a number. This is reproduced digitally if the keyboard is on a screen.

Interestingly, musical synthesizer keyboards operate similarly. [The only difference](engineering-audio.md) is that they usually output the signal to a perceptible sound, along with (possibly) sending MIDI information out to a computer.

However, the *actual* design of a keyboard itself isn't so simple. Keyboards use an elaborate "keyboard matrix" to map the keys to the signals they're supposed to send.

The keys themselves are designed to maximize ergonomic convenience and [conform to user habit](engineering-design.md). The conventions were drawn from typewriters, with a vast variety of other strange designs throughout the 1980s.

However, the keyboard convention has settled itself into a predictable layout since the 1990s:

- A QWERTY layout of 26 characters, plus 8 keys used for punctuation. This was pulled straight from how typewriters worked (which was configured to prevent the hammers of nearby keys from sticking to each other when typing correctly).
- A few keys to navigate text: a large Space key at the bottom to advance a space, a Tab key to insert a gap of about 5 spaces, Enter/Return to move to the next line, and Backspace to remove a character.
- A row of number keys along the top, with a few mathematical keys next to it, with an alternate configuration of other more specific punctuation symbols.
- A panel of 6 keys, with 4 of them being navigation (Home, End, Page Up, Page Down), an Insert key that changes the text mode between insertion and overwriting, and a Delete key that serves as the forward deletion (i.e., the reverse of Backspace).
- Navigation/cursor/arrow keys arranged in an inverted-T arrangement that allow directional navigation.
- To allow the user to send more information, keyboards have multiple "modes" that allow for capitalized letters (SHIFT key), along with [alternate and control key combinations](cs-keyboard-shortcuts.md) (ALT and CTRL key). To make it convenient, they're on both sides of the keyboard.
- A Print Screen key. At one time, it would *actually* send the screen's display to the printer when everything was [terminal-based](cs-cli.md), but now serves to send a screenshot to the clipboard.
- A Pause Break key. At one time, it would break a telegraph circuit, and is most reliable to stop a [console command](cs-cli.md). However, it doesn't have a well-defined purpose anymore.
- A proprietary "super" key (Win and CTRL, or ⌘) that adds even *more* functionality and features.
- Specific locks to make the user more efficient:
  - CAPS LOCK keeps SHIFT key pressed for entering letters.
  - SCROLL LOCK is a bit more software-specific (e.g., spreadsheets), but permits the arrow keys to either navigate the screen or their selection.

Further, multiple other features are *often* on a keyboard, though they're not required:

- Function keys labeled F1 through F12, designed for additional software-based features.
- A number pad with all the numbers and mathematical symbols in a 10-key configuration. It can be *very* useful for [math-related](math.md) needs (e.g., [accounting](money-accounting.md)).
  - NUM LOCK is a mode that uses the number pad only for entering numbers (rather than navigation).
- Other proprietary buttons for features like media playback or task-switching. Many of them can be remapped.
- To save space, smaller keyboards may use function keys to make multi-function buttons, often with the alternate function also labeled on the keyboard (e.g., volume controls, brightness controls, calculator shortcut).

There are other keyboards, such as for stenography, and there are plenty of weird designs, but the QWERTY model seems to have stuck in the public mind as good enough.

- There are other keyboards that run similarly (DVORAK and AZERTY), but the added value they provide is so negligible, if any, compared to [convention](habits.md), that they haven't caught on anywhere. And, the dominant issue will be someone adapting to *two* [standards](cs-standards.md).

It's worth noting that *all* keys can be re-mapped.

- One of the first things worth mapping to another location is the Caps Lock, since it's in a very convenient place but is rarely used.

There are two major ways that keys connect with their electrical contact:

- Membrane keyboards have a bendable rubber dome that pushes down when pressed to activate the connection. This makes a softer-feeling press, but is much cheaper and often more quiet than a mechanical keyboard. Some older membrane keyboards were flat, meaning you couldn't easily use touch typing with them (instead of sight typing, which is *much* slower).
- Mechanical keyboards have a piece of plastic obstructing a bent piece of memory metal when it's raised. When depressed, the plastic moves out of the way and makes the connection. That connection can be linear (slides down smoothly), tactile (a small bump it has to go over before it connects), or clicky (a separate piece with a bump that bounces down to make an audible click).

As far as feel and responsiveness, mechanical keyboards are superior. However, their design comes with some downsides:

- Mechanical keyboards are more expensive to manufacture than membrane keyboards.
- The form factor of mechanical keyboards is almost always much larger and heavier than membrane keyboards.
- Mechanical keyboards are typically MUCH LOUDER than membrane keyboards. In some situations, they can keep people up at night.
- Mechanical keyboard signals have a higher chance of mapping extra keys (also called "ghosting") when 3 or more keys are pressed, so it often stops those keys (also called "blocking"). Thus, there's an "n-key rollover" that sets a maximum number of keys registered as pressed. This usually doesn't cause issues for most people, but hardcore [software developers](cs-software.md) and [gamers](cs-software-gamedev.md) will notice anything below 6-key-rollover.

Occasionally, a keyboard may register multiple inputs with one keyboard press, known as a "key bounce". There are several "debounce" [break-fix](https://adequate.life/fix/) methods:

1. Software debouncing, which involves adding response delays to the controller after the first press.
2. Dusting out the keys with compressed air, or running it through the dishwasher if the keyboard doesn't have many expanded features.
3. Replacing the switch directly, which is typically not worth the cost or trouble on a cheaper keyboard.

## Moving information

The keyboard signal sends over to the "keyboard memory map", a specific spot in [memory](cs-memory.md) that shows what keys are pressed.

Since the keyboard memory map is an abstraction, it doesn't necessarily *need* a physical keyboard:

- Add a keyboard display to a [touchscreen user interface](engineering-design.md).
- Use hand or body gestures with a programmed [camera](engineering-camera.md) to capture letters or words.
- Use electrodes attached to the brain to let someone "think" the letters or words.

## Not simple

In general, a keyboard press has many stopping points between the moment that it's pressed and the moment the [CPU](cs-cpu.md) registers it. While it's not really processed at all during that wait, the signal is often locked-off or added to a queue to allow other time-sensitive [operating system](cs-os.md) processes to complete first.

However, computers still run as fast as necessary irrespective of this delay. The only time this ever presents itself as an issue is with specific uses (such as playing high-reflex [games](cs-software-gamedev.md)). But, if [screens](engineering-screen.md) draw frames faster than 60 Hz, this may change.

This, of course, doesn't address the fact that sending the characters accurately into the screen is the first challenge. The second is to [correctly express the characters to a screen or printer](cs-keyboard-characters.md).

## The future

While [some futurists](https://trendless.tech/trends/) imagine that we may migrate away from text (such as a society that exclusively communicates via voice or videoconferencing), this has proven itself false. Text is *very* low-data to [transfer](cs-networks.md) compared to audio or video, and is easy to [search and index](cs-langs-algorithms.md). For that reason, text (and by association, keyboards) will always be around in some fashion.

Keyboard interfaces migrated naturally from hardware to software, mostly because [habits and rituals](habits.md) are difficult to change. The future of keyboards will be much of the same.

Keyboard interfaces have become more advanced. As of this writing (June 2022), neural implants are now permitting near-accurate typing using thoughts with at least 94% accuracy. It allows people with paralysis and cerebral palsy to communicate, and paves the way for further developments.

However, keyboards must conform to healthy [UX standards](engineering-design.md). Pushing too many [trendy changes](people-trends.md) will invariably alienate most of the users, so it's likely keyboard conventions will stick around *long* after nearly everything uses a software-only digital keyboard.

## More information

[Computer latency: 1977-2017](https://danluu.com/input-lag/)

[N-Key Rollover explained](https://www.mechanical-keyboard.org/n-key-rollover-explained/)

[U+237C ⍼ &angzarr;](https://ionathan.ch/2023/06/06/angzarr.html)

The Absolute Minimum Every Software Developer Must Know About Unicode - ([One Guy](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/)) or ([Another Guy](https://tonsky.me/blog/unicode/))
