
# Good computer interface design

Designing a "user interface" (UI) is a subdivision of visual artistry. At one time, the design field was oriented toward "human computer interaction" (HCI) but has since moved to the realm of "user experience" (UX) from the ubiquity of business within technology. UI is what users perceive, while UX/HCI is what users do.

All the [general rules of good design](engineering-design.md) apply, but computers take a divergence in a few key areas.

## Rules

The speed of successful [tech trends](trends.md) mixed with the relatively young age of most [tech innovators](trends.md) tend to see the industry *constantly* break the rules of UX.

No design is *ever* perfect, but computers have taken bad design to a new level:

- Make things invisible.
  - Exploit the tyranny of a blank screen.
  - Don't use hints for effectively operating the system.
- Give no feedback or results of what happened.
  - Have a huge interface gap between different related elements.
  - Make a gap in time between doing and observing anything.
- Be arbitrary.
  - Use non-obvious commands.
  - Be inconsistent and change the rules.
  - Let something get done one way in one mode, then another way in another.
- Make operations difficult to understand.
  - Use idiosyncratic language or abbreviation.
  - Use uninformative error messages or notifications.
  - Make all the information available in [the manual](language-writing-documentation-cs.md), instead of in the interface.
- Be impolite.
  - Treat errors and near-errors as completely invalid.
  - Make errors seem or be very dangerous, as if they're [breaches of contract](people-contracts.md).
  - Permit 1 error to destroy valuable work.

Users can only draw from their [environment](reality.md) (observations) or [memory](imagination.md) (expectations), so [computer design](engineering-design.md) frequently borrows from the world around us:

- Building things to reflect biological form, such as making the case look like a plant or adding earth tones.
- Adding context-sensitive colors, such as shades of gray for industrial tones or a brightly colored palette for children's themes.
- Inputs that match how we interact with nature (e.g., a scroll wheel interacts like rolling a ball on the ground, a steering wheel interacted like pulling the reins of a horse).

We draw [patterns](symbols.md) that connect different aspects of the world around us ("skeuomorphism"), so it's *absolutely* critical that technology reproduce the feedback mechanisms in other existing technology or in nature.

- This can be very difficult if the industry standard has been *bad* design.
- To get new users to understand new concepts, they must migrate from the old through slow adaptations, which are *guaranteed* to move more slowly than the technology itself.

The available information from that technology also allows for more specialized design requirements:

- Computers can only display an astronomically small percentage of all their information at any given moment, so designers must severely consider the users' "attention economy", which makes [good design philosophy](engineering-design.md) (especially regarding visual hierarchy and visual structure) absolutely critical.
- Since a computer is *constantly* working when it's on with an inhuman logical flow, use empty space to articulate silence to the user and personalize it to indicate that a human designed it.
- Make sure the presented information is using any tracked [location data](logistics-navigation.md), and make it location-agnostic if there's a [VPN](computers-cysec.md) or no location. Generally, there's still usually an *approximate* nation or region to derive data from.
- If there is *any* information about the [operating system](computers-os.md), assume the user is using that particular OS. Either way, give a simple selection for *all* available OSes.
- If the user has provided information, use it to tailor all relevant [algorithms](computers-programming-algorithms.md) of the software (e.g., their genre preference should define *all* the content).
- Provide personal information based on the software's usage. Generally, a large-scale enterprise's needs are different from a home user.
- Since people value their privacy, build trust *before* asking for permissions for more information.
- Create designs that direct the user's incentive toward something else that is *not* the computer. We are [wired to need human connection](humanity-universals.md), and computer-assisted [interaction](people-conversation.md) is typically *less* [meaningful](meaning.md) than in-person.

## Communication

Typically, the nature of tech trends means most of the styles communicates from the sci-fi/fantasy of the time to imply the technology is "futuristic" by that decade's [fashions](trends.md).

The domain of technology has *magnitudes* of complexity, so users have a dramatically higher chance of frustration than any other industry:

1. Most people don't understand computers in full.
2. They also often don't communicate that lack of understanding to others, for various reasons.
3. This lack of shared non-understanding creates a conspiracy of silence.

[Software engineers](computers-programming.md), by the nature of their trade, do not need great [communication skills](people-conversation.md) and often have limited [people skills](people-2_image.md), so many computer design elements have been, from their inception, fundamentally obtuse.

This is almost standard in tech, and never seems to [trend](trends.md) otherwise. Most software is either bloated or under-communicates, depending on the psychological idiosyncrasies of the software engineer and design team (if any).

[Cybersecurity](computers-cysec.md) design, by contrast, is simply the *reverse* of good design: instead of communicating what a user can do, the designer is obscuring and *hiding* things instead.

Of course, this means many possibilities for growth within computers. Many more things frustrate users in computers than anywhere else, so there are more possible places where [taking a risk](entrepreneur-1_why.md) may yield a positive result.

## Documentation

The complexity of computers almost *mandate* a manual, and it's about as important as the product itself (since the product won't work without the knowledge contained in that manual). It's a necessary evil from how utterly complex computers are.

With software, it's not difficult to include help files and browser-based [hyperlinks](computers-sofware-webdev.md) to lead the user to what they need. With hardware, it's worth including both simplified and advanced documentation for different levels of users, or to at least maintain a permanent archive hyperlink built onto the package.

The most effective internet-based form of a manual is a Q&A-based forum with the engineers and product designers answering user questions, since it allows a direct conduit for feedback from the users, which gives the designers criteria to develop *future* iterations of the product.

## Forcing functions

Forcing functions within the domain of computers is *way* more dangerous than any other domain. While people may [hack](hacking.md) their fridge or car to do what they want, tech hackers are *very* intelligent and *really* hate forcing functions, especially lock-outs. Many of them will try to break a lock-out on principle alone.

## Human error

Computers work with information at scale, so devote intensive effort to preventing the user from breaking everything with one button-press.

- Ask for confirmation before deleting or moving large amounts of something.
- Hold on to important information before deleting (e.g., "Recycle Bin").
- Require that massive tasks (e.g., deleting 1,896 files) require typing in the exact number shown.

However, it is vital that any error-correcting system *must* work or people will absolutely hate it. And, once it's implemented, people will come to *depend* on it, so be careful removing it if you already have it.

## The design's elements

There are *many* elements to consider for interacting with a computer. Most of them are automatically designed into most [operating systems](computers-os.md) or [web browsers](computers-sofware-webdev.md), but anyone with patience to learn can often tweak, add, or remove them.

Many elements abide by the [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/), which set standards that allow *anyone*, even colorblind or visually impaired, to easily use the computer.

The visual flow in an interface must allow the eyes to travel along a line. That line should be as short as reasonably possible.

### The object's structure

The abstract nature of computer interfaces makes simple and easy interfaces *much* more critical than non-computer design.

- A horizontal element spanning the screen that includes menus and status indicators.
  - On operating systems, it's usually at the bottom, but can also be at the top.
  - It's usually at the top on websites, but might shave down on mobile screens to a "hamburger menu" with a dropdown that spans the vertical range of the screen.
- If using a horizontal grid, use 12 columns (which can be broken into denominations of 1, 2, 3, 4, and 6 as needed).
- A menu that can be selected, or an element that opens up that menu.
  - Can often have sub-menus for drilled-down selections.
  - If it's a visually present menu, it must have labels that make intuitive sense to the user (e.g., File, Edit, View, etc.).
- Scrollbars for consuming information that extends beyond a screen's size, with the bar itself representing the relative size to the bottom and updating as new information expands or contracts the information domain.
- Use "skeleton loaders" to give the form of the objects and their placement *before* the computer has fully loaded the assets.
- Adaptable elements that change depending on the size of the screen or window, becoming simpler and removing columns as the screen space gets smaller. This can also mean making entirely different interfaces for mobile versus desktop sizes.
- Provide clear "exit points" that define when the user can easily and safely leave the experience.
- Align *everything* with other elements optically (the way the eye sees it), and *not* mathematically (the center of the element). It should always be represented as a chain of elements.
- All measurements should be [mathematically](math.md) related to each other.
- Make sure multi-line text never sits with only 1-2 words alone. It can create widows (1-2 words on the next line) or orphans (1-2 words completely separate at the top of another section). The easiest solution is to set the CSS property called text-wrap to balanced.

As much as possible, separate out the information with a clear demarcation and structure:

- Borders and boxes are elements *themselves*, while empty negative/white space conveys enough silence to assist the user.
- Never place two hard divides next to each other.
- Keep the outer padding as much or more than the inner padding.
- For lots of information, lists of features (typically with bullet points) help the reader skim it more easily.
- Keep headings at least somewhat closer to the body of text they summarize than other content.
- Use striped tables when they have lots of data.
- Make hyperlinks *very* distinctive to identify.

### Colors

Since most interaction with a computer is [screen-based](engineering-screen.md), color is *vitally* important for communicating information on the [front-end](engineering-graphics.md) and [across the internet](computers-sofware-webdev.md), more than most other non-computer design:

- Use the colors from the source images to define the color theme and "gradients" of the site
- Contrast the colors between the text and the background to make it as readable as possible, which may include adding color overlays or gradations over the photo before imposing text.
- Saturate neutral colors to draw more visual attention, but only use *either* warm or cool colors.
- To make colors distinctive, vary both the hue and brightness values to non-standard numbers.
- Use colors to distinguish various sections of the site, but keep the colors at least *somewhat* consistent to avoid any incoherence.
- Include several color themes that allow for a "dark mode".
  - Keep the brightness values between the background and container within 12% for dark themes, and within 7% for light themes.

One tiny and important detail is to never use straight black (i.e., #000000), which is often standard for Regular weight typefaces:

- We tend to see dark things and imagine them to be black, but even *shadows* are more gray/blue/brown than black.
- Even in innocuous elements (e.g., table borders), black completely overpowers all the other colors and draws all attention to it.
- To use black, saturate it with other colors relative to its environment (e.g., saturate the black with blue if it's a blue interface).
- The entire interface should use sustained colors, typically gray, with (usually) black text and important elements using distinctive palette colors.
  - Make the elements distinctively contrasted in color from each other.

Shadows are dark edges around the element to make the interface feel three-dimensional. They tend to vacillate with [social fashions](trends.md) with an attempt to make everything look three-dimensional:

- Sometimes they're "drop shadows" that fade, in the past they were "gradients", and are defined by a blur value. Generally, heighten the blur to give the illusion that it's nearer.
- Light implies nearer, and dark implies farther.
- The only requirement is to stay consistent with them and avoid using them with heavy colors.
- Generally, minimalism is timeless.

### Object selections

A user needs *much* more information from computers than most products to make their [decisions](people-decisions.md):

- The user's social feedback systems should reflect habitual prompts we perform in our daily life ("like" buttons, comment boxes, "share" buttons).
- Use one primary button per page (e.g., "Next"), with secondary buttons have a more subdued presence.
- "Autofocus" on the first form field to make it more convenient for the user.

The farther the distance the user has to travel, the less reliable their selection, and the larger you should make the elements (Fitt's Law).

- Make sure the buttons are large relative to where the user last was on the screen.
- Keep the buttons fixed-width because any changes to the button text (e.g., content loading, font formatting) can make the button shrink.
- However, the farthest edges of [screens](engineering-screen.md) adds additional accessibility. The *very* edge of the screen is effortless to navigate to because it captures *all* distances where the selection goes beyond the screen (e.g., thumb touching the edge of a tablet). Those regions are called "magic pixels" from how convenient they are.

The buttons and selections should be seamless on *all* varieties of input peripherals the user may use:

- [Mouse-only](computers-mouse.md) interfaces don't work well with swipe-based interaction, touchscreens don't have any sort of mouse-over function, and [audio-only](computers-speakersmic.md) can be *very* challenging to give prompt feedback without the user interrupting.
- Keep the most frequently selected options as easy to access as possible.
- The length of time the user has been using the software should reflect with the selections, and more frequently used *advanced* options should move to an easily accessible portion of the interface as the user keeps interacting with it.
- Do *not* move things the user may potentially select, especially if the content is partially loaded.
- If the user will be on a mobile device, provide a "copy to clipboard" button next to an important piece of information.
- The button's padding height should be half the padding for its width.

A dropdown takes multiple selections by the user, so *only* use them if the users aren't on a mobile device, there are hardly any options, and the users rarely need to change the default value:

- If it's 2-5 buttons, use vertical segmented buttons or radio buttons.
- If it's many options, use a "typeahead" control.
- For a date, use a calendar control for a nearby date (e.g., an appointment) and a text input for a wide range of dates (e.g., birthdate).
- For a number, use a "stepper" for small numbers and a text entry for large ones.
- If it's 2 options, use buttons instead.
- If you use a dropdown, communicate there are more by either making an explicitly obvious scrollbar or making the dropdown height a weird 1.5-sized distance to show further selections.

Try to keep all fill-in forms brief and clear:

- Always have a heading to indicate what to enter, and do *not* use the "placeholder" text field for it.
- Unless the software can grab most of the information or the user can enter all the information into 1 screen, have an "onboarding" process that gathers all relevant information, preferably without the user consulting their email first (since it's a distraction).
- Have the most frequently used selection be the "default" or most prominent selection.
- Use a clearly defined button that can jump ahead with default information.
- Provide positive feedback as well as negative (e.g., a checkbox icon for completed, an X icon for incomplete).
- Have a percentage indicator, progress bar, or ## of Total ## to show how much required input is left.
- Less effort from the user is better, and the user can often skip *many* elements (names, phone numbers, email confirmations). Some can even be auto-generated (e.g., temporary passwords emailed to the user) or pulled from a social network API.
- Provide "input masks" that inhibit incorrect entry and use the input box's size to give clear implications.
- "Autocomplete" the information if it's frequent enough.
- If an input has any rules, explicitly communicate them nearby without any extra required input before the user enters the information (e.g., [password](computers-cysec-authentication.md) rules, character limits).
- If the input is a fixed-width verification code (e.g., 4 digits), validate as soon as the final number was entered instead of giving a "Submit" button.
- Frequently use a "none" or "other" selection, since a 0.01% edge case becomes substantial with many users, or simply have a yes/no question that opens up the selection options.

A computer also must communicate *back* much more than most other products:

- As the user enters input, remove other logically unnecessary elements (e.g., remove the social media login buttons as the user enters their username).
- When relevant, give visual examples of what the selection would look like (e.g., a simple map of each country as it's selected).
- For critical information that needs more than 1 selection, use a "modal window" that locks out other input.
  - When using a modal window, *never* use scrollbars and make it several pages instead.
  - Be cautious with modals, since mobile device browsers often don't work well with them.
  - Avoid confirmation modals (e.g., "Do you want to continue?"), since users have a habit of quickly clicking through them.
- "Customer assurance widgets" give a visual indicator the computer is doing something (e.g., percentage indicators, progress bars, animated loading screen), but *only* if it's more than about 0.5-1 seconds. If it takes longer (~5-10 seconds), indicate further information to the user.
- The software must ask for [permissions](computers-cysec-authentication.md) relative to both when it is absolutely necessary *and* proportional to the user's trust of the software.
- Clearly indicate any algorithmic results that work in the interests of the user, and hide the rest.
- However, if the software keeps over-communicating (e.g., too many notifications, too many emails) it should reflect *less* communication from under-interaction.
- Indicate a download button very distinctly and clearly with color, and with a percentage indicator for anything above a few kilobytes to show progress.

Any feedback systems should be *very* well-articulated (error messages, further selections about those errors):

- Clearly demarcate *where* the user is in the software system.
- If there are any "empty states", indicate clearly that there's no additional information (e.g., "you have no credit cards on file").
- The user should *always* know what they should do next.
- Be careful with toggle switches (i.e., sliding checkboxes), since they give poor feedback compared to checkboxes (since they're pulling from [network](networks-computer.md) information instead of sending that information *after* the user submits it).

"Validation error" messages should give their response *very* near where the user made their selection.

- "Autoscroll" the window to that error.
- If there were a few failed login attempts, give a link to the password reset page.
- If the error message is at the bottom, the messages might pile up and be difficult to read.
- That error message shouldn't disappear with further user input (such as a "toast" notification).

Other selection features ought to be industry-standard, but often aren't:

- Avoid the browser's default file upload feature, since it varies wildly on the [browser](computers-sofware-webdev.md).
- For physical things with a relatively analog control scheme (e.g., 1 to 100), physical knobs and dials are almost universally superior to buttons on a screen. This, however, does add extra work for [project management](mgmt-2_projects.md).
- Have settings available for advanced and experienced users, with all the options available the most advanced user would ever need. If a setting might break something, prompt the user.
- Instead of directing permission requests directly to the operating system's prompt when the software needs it, have the user make an opt-in selection within the software with a lock-out if it's *absolutely* necessary.
- Give a posted date for content that isn't designed to be completely time-insensitive.

### Conveying media

Media (especially visual media) in computers must be managed carefully:

- Present most typical media in as downsampled a format as possible to save on [bandwidth](networks-computer.md) and loading.
- "Media queries" that resize elements appropriately relative to the [screen size](engineering-screen.md) or other elements.
- Clear text or other types of media as a fallback if that media can't present itself (e.g., [sound](computers-speakersmic.md) has been muted, poor internet connection).
- Maintain standard requirements for common user disability use cases (the most obvious being deaf, blind, and amputee).

Keep icons consistent across the medium or page:

- Don't mix-and-match icons.
- Label the icons, especially if there's *any* chance a user won't understand.

### Typography

The dynamic nature of screens give *much* more control for designers over fonts:

- Proportional font scaling that distinguishes headings, subheadings, and body text from each other.
- Because of the varying sizes of screens, most interfaces incorporate "liquid layouts", where the size of the interface is defined by a percentage in a box rather than pixel size.
- Keep the body text font over 16 points.

Many good ideas in typography aren't common, but should be:

- Uniwidth/equal-width/duplexed/multiplexed typefaces, where it's the same width even when it's boldened/italicized/underlined.
- [Standards for font sizes and line heights](https://tonsky.me/blog/font-size/). Windows vs. Mac fonts have different font sizes, line height is arbitrarily set and messes up the flow of lines, and nobody has really made an accepted standard yet.
- Keep headings and small passages of text aligned to the center, but larger bodies of text should be left-aligned. If they're "justified", the "kerning" creates an uneven flow.
- To keep text legible, increase the line height as the font size decreases.

Most UX design revolves around [web development](computers-sofware-webdev.md), so make sure the hyperlink is accessible:

- Make links that directly point to the content you want the users to access.
- If the hyperlinks are designed to be easily accessible, use a user-friendly URL: `https://site.com/content` instead of `https://site.com/page?page_id=730/u/ycur`.

### Text content

Since we still often must use words, the text *itself* must also concretely connect to the use of the product:

- Keep the text's case consistent (e.g., "Your Order is Ready for Purchase" shouldn't lead to "Congratulations, your order is complete!").
- Stay practical to what the thing actually does, or give concrete examples.
- Stay consistent with the first-person (e.g., "My Favorites"), second-person (e.g., "Your Inbox"), or strip it out altogether (e.g., "Inbox").
- Use the same choice of words for specific commands (e.g., "Continue" vs. "Next", "Back" vs. "Previous", "Home" vs. "Main").

Avoid using redundant text (e.g., "Enter your email and password" heading with "Your email address" above the entry).

## Design at scale

[Software development](computers-software.md) has a unique, nasty problem:

1. First, the software must be designed, then [tested a *lot*](computers-software-redesign.md) to ensure it actually works.
2. Then, the software must be tested to ensure that people *beyond* the designer are capable to use it.

The implication of this is that the [project management lifecycle](mgmt-2_projects.md) in a large organization will likely be *twice* what the manager is probably thinking.

Further, on top of making design changes, the revolving nature of version control requires a few elements at the end of the process:

1. Use paced updates and small version control updates on *each* element, to avoid complicating things with a large-scale update all at once.
2. Have automation that tests each of the dependencies, to track for any failings in the interfaces.
3. Automate *all* updates for each element, meaning nobody has to manually change elements as they update.

Fixing bad software/hardware design isn't as easy as it sounds. The technology experience can suffer for multiple reasons:

- It takes 5-6 ideas to get a design right, and startups often only get 1-2 shots at good design before they run out of money, so their design often becomes industry-standard even if it's not that great.
- Most design rules in tech create *many* contradictions which arise across a plethora of edge cases.
- The people who design software are human beings who [may not want the users' best interests](faang.md), and have reason to employ "dark patterns" to make some elements difficult to access (e.g., unsubscribe, delete account, remove connection).
- [Social trends](trends.md) can redefine elements, so most websites are *constantly* changing. Some elements become archaic, new elements become the standard, and some elements can become purely offensive.

Good software design starts with a rudimentary structure, then works outward. Unfortunately, the feature/complexity paradox dramatically expresses itself within computers:

- Watching a rapid update of files can be scary to watch for a non-tech-savvy person, but a spinning wheel often won't indicate an error.
- Every new version of the software adds features, but often clutters up the menu or makes the experience more inaccessible.
- Without discretion, every software eventually becomes an okay multi-use product instead of a great single-use one.
- The only way to keep an inherently complex product like software or a computer simple is to *constantly* investigate how to merge or remove obsolete features. Just make sure you explicitly document those changes, and allow people to roll back [those updates](computers-software-redesign.md) if they need.
- If the features become difficult to work with, reorganize the features and give the user the full option between the new and old way.

Generally, large-scale changes can force an immobilized design experience. Back when [Windows 95](computers-os-windows.md) dominated the OS market, people could tweak their wallpaper, colors, and sound effects, but most granular control is constrained in most mainstream [OS's](computers-os.md). Having the freedom to keep a customizable interface would require exponentially more work, or the quality would suffer.

At least, theoretically. Customizable elements heavily contribute to a user's feeling that the interface is "theirs", and gives the users a more [meaningful](meaning.md) experience, even while it's more awkward.

### Big issues at scale

Some UI ideas are terrible, for various reasons:

- Hidden elements (e.g., scrollbars, buttons) can often work fine on mobile devices, but are unwieldy if someone has a desktop computer.
- Moving elements around with every update will perpetually disorient the user, especially if they don't communicate the changes publicly beforehand or in an "Updates" prompt when they open the program.
- Not instructing the user via tooltips when hovering over an element. This often leads to confusion and, sometimes, tremendously large mistakes.
- Failing to clarify the difference between input locations, such as placing "Projected Budget" and "Estimated Budget" on two input boxes next to each other.
- Saving information when the user presses "Submit", but not communicating a response.
- Saving information that the user volunteered, but not using that information for inherently obvious future tailoring of the experience.
- Excessive JavaScript or elements that interfere with the user experience instead of help direct their attention.
- Modal windows (windows that pop out information inside the page) can't easily have a hyperlink to it, can't be opened in a new tab, can't be bookmarked or shared as a link, make the back button confusing, and can't compensate for slow page load.
- Making the "Sign In" selection difficult to find, or making it indistinguishable from the "Sign Up" one.
- QR codes without an alternative URL to key in, since not all devices reliably read them.
- Creating an infinite scroll feature on a product that doesn't need it.
- Only having a "like" button for feedback, but without extra clarifications or using the numerical "likes" as a simple means of prioritization.
- Requiring the user install extra software or accept extra [permissions](computers-cysec-authentication.md) that are convenient for the developer, but often involve [tracking data that the user may not want tracked](faang.md).
- Removing any features that the users had become familiar with.
- Messages and prompts with excessive wording and explanation, instead of providing [documentation](language-writing-documentation-cs.md) for people who wish to read more.

Most tech designers are *way* more fickle than the average non-tech comparison, which makes tech design even *more* volatile:

- They'll get bored way more quickly, and their creative tendencies will provoke them to reinvent the wheel by designing [a better volume control](https://uxdesign.cc/the-worst-volume-control-ui-in-the-world-60713dc86950?gi=64381f3bdf3b), menu system, mouse pointer, or whatever.
- They'll be *much* quicker to adopt trends, and the speed of adoption determines how fast it'll get abused. It can lead to absolutely absurd interfaces until it's [patched later](computers-software-maintenance.md).
- Sometimes, they'll stumble across a stunningly *brilliant* design, but it'll take too much work to maintain, and a future update will replace it with a simpler (and more boring) one.
- Asking for [permissions](computers-cysec-authentication.md) or for the user to download software is highly convenient for the developer, even while it's annoying for the user, and that selfishness bleeds into the software experience.
- Giving icons or elements users may find interesting in focus groups, but don't plainly articulate the information the user may need.
- Moving things around on the user, but without giving any warning or communication of the old ways of doing things.

Generally, the context of UX determines which direction it'll fail.

- If it's consumer-facing (e.g., [web design](computers-sofware-webdev.md)), the push for simplicity and ease-of-use will make arcane systems hiding behind deceptively simple visual elements.
- If it's more technical or organizationally facing, the constant [feature bloat](computers-software-maintenance.md) will make the interface cluttered with all the extra edge cases present for the user.
- The solution is to find ways to make it accessible for the first-time user, in such a way that a technical user won't feel hampered by the experience. This is difficult to do.

While it may be useful to catch most glaring issues, A/B testing can absolutely *ruin* the longevity of a design in lieu of short-term gains.

- Harassing users will maximize short-term results, but will drive away long-term growth.
- Over time, UX driven by A/B testing will generate a lingering unpleasantness with anyone who *didn't* want to perform precisely according to the metrics.

Computers have a unique paradox:

1. We must abide by [existing convention](habits.md) to learn how to operate something new.
2. Simplicity is critical for people to easily, quickly [understand](understanding.md) information that helps them make [decisions](people-decisions.md).
3. For the convenience of the hardware and software engineer, *all* the complexities are laid out when they first design the object.

Those 3 elements combine to mean that computers *can't* please all the users unless there are *many* dropdown menus and extra hidden elements for more complex features.

In technology, the "slow" element is the user's understanding. More than anything else, the slowest part of any designed computer that isn't a [large-scale distributed system](computers-distsys.md) is the user.

As society keeps moving more toward browser/app-based computer interaction, proportionally fewer designers can create increasingly more misery for users. In high-stakes information transfer, such as large-scale banking and government websites, dark patterns and incompetence are almost guaranteed.

One of the most significant forms of dark pattern comes through default settings. Most users don't think to reconfigure settings, so they'll often automatically opt-in to whatever settings are provided, and *possibly* change them later.

### Addiction

Computers can magnify [addiction](addiction.md) more than just about anything else, mostly because a computer's design permits room for *many* dark patterns without the user's awareness:

- Forcing users to opt-out of things instead of letting them opt in.
- Email lists divided into many groups, which require the user to manually select *all* of them individually to fully remove their subscription.
- Swapping out UI elements to provoke users to make a mistaken selection.
- Hiding a [contractual agreement](people-contracts.md) behind a checkbox that has terms the user would certainly *not* agree to if they read it.
- A "download" button that's near the *actual* download button that typically contains [a virus](computers-cysec.md).
- Providing an inadequate experience *outside* the "paywall", then not permitting multiple payment options depending on the users' needs.

Shame is a [manipulation tactic](power-types.md) that tries to coerce users to do something. In software, this can be magnified because the software was *designed* that way, meaning it's scaled with the number of users:

- Confirm-shaming by making the "no" selection something terrible (e.g., "no, I hate outstanding content and freedom").
- Manipulinks that provoke people to select hyperlinks.
- Provoking users to accidentally select something.

Sometimes, in the interests of [marketing numbers](marketing.md), some UI decisions will be *terrible*:

- Email popups that confront the user 3 seconds into opening the website, since [A/B testing](engineering-design.md) showed it gained 10% more subscribers (while not really considering the lead-to-sales ratio).
- Moving around highly established design elements, since marketing [fashions](trends.md) dictated it was trendy and the key demographic would like it.

To get more money, online shopping has a few specific dark patterns:

- Hiding or subduing the presence of the free version to imply it's inferior or doesn't exist.
- Sneaking items to someone's shopping cart without their permission before they purchase an item.
- Copious [advertising](marketing.md) that promotes an unrelated product as part of the software experience.
- Making default selections that pre-select a price the user would likely not want to pay.

The incentive of a social media organization is for more people to use it more frequently, so some dark patterns are exclusive to them with the intent of people spending more time on the service or selecting advertisements:

- Requirements to share content to fully consume media (e.g., an article, free music).
- Adding [advertisements](marketing.md) in between users' content, with [algorithms](computers-programming-algorithms.md) that tailor those ads to be as associated as possible to what the user may want to have.
- The software requesting consent by the user to send messages to that user's contacts (typically email), then abusing that permission and messaging *everyone* in their contacts without their knowledge.
- Artificial notifications with no relevance that still provoke the [habit](habits.md) of checking and removing them.
- Sending fake requests to connect to the user as if they were initiated by another person, but the user's *reply* is the request to connect.
- Making the default message for connection requests sound desperate or urgent.

Except for casinos, [game development](computers-software-gamedev.md) contains some of the most addiction-inducing design possible. Games use goals and rewards to create an [operant conditioning chamber](https://en.wikipedia.org/wiki/Operant_conditioning_chamber) that leaves people *constantly* emulating the sense of reward that comes from [succeeding at life](success-1_why.md), but within their small ecosystem:

- Time the delay of rewards to be frequent enough to prevent boredom.
- Let off on rewards for a little bit to offset diminishing return and overload.
- Provide *just* enough incentive to keep playing the "free" game, while constantly [advertising](marketing.md) the paid game.
- Force scarcity over certain collectible items that would dramatically improve a player's performance.
- Create "loot boxes" to incentivize more purchasing with only a *chance* of granting an incentive.
- "Shaping" behavior to curate habits (e.g., spending free money at the beginning, starting a time-intensive task).
- Creating symbolic distance between the user and their money with a token/currency system.
- Using patterns to imply real people are using the game, with their status implying that they're more financially invested than the player.
- Constraining the progress a player is capable of performing on any given day without paying more money.
- If there's a social component to it, all the dark patterns specific to social media may apply as well.

At its most sinister, social media can provoke people to "doomscroll" (consume a large amount of bad news at once) to keep people constantly engaged with that platform.

## Additional reading

Delivering Impact

- [Juice](https://garden.bradwoods.io/notes/design/juice)

Colors

- [Building Your Color Palette](https://www.refactoringui.com/previews/building-your-color-palette)
- [Why are hyperlinks blue?](https://blog.mozilla.org/en/internet-culture/deep-dives/why-are-hyperlinks-blue/)
- [Contrast Rebellion](https://contrastrebellion.com/)

Specific Elements

- [You don't need a modal window](https://youdontneedamodalwindow.dev/)

Generating Addiction

- [Dark Patterns](https://neal.fun/dark-patterns/)
