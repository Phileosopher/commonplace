
# Universal standards for specific designed computer elements

There are *many* elements to consider for interacting with a computer. Most of them are automatically designed into most [operating systems](computers-os.md) or [web browsers](computers-sofware-webdev.md), but anyone with patience to learn can often tweak, add, or remove them.

Many elements abide by the [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/), which set standards that allow *anyone*, even colorblind or visually impaired, to easily use the computer.

The visual flow in an interface must allow the eyes to travel along a line. That line should be as short as reasonably possible.

## The object's structure

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

## Colors

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

## Object selections

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
- Be careful with toggle switches (i.e., sliding checkboxes), since they give poor feedback compared to checkboxes (since they're pulling from [network](networks-cs.md) information instead of sending that information *after* the user submits it).

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

## Conveying media

Media (especially visual media) in computers must be managed carefully:

- Present most typical media in as downsampled a format as possible to save on [bandwidth](networks-cs.md) and loading.
- "Media queries" that resize elements appropriately relative to the [screen size](engineering-screen.md) or other elements.
- Clear text or other types of media as a fallback if that media can't present itself (e.g., [sound](computers-speakersmic.md) has been muted, poor internet connection).
- Maintain standard requirements for common user disability use cases (the most obvious being deaf, blind, and amputee).

Keep icons consistent across the medium or page:

- Don't mix-and-match icons.
- Label the icons, especially if there's *any* chance a user won't understand.

## Typography

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

## Text content

Since we still often must use words, the text *itself* must also concretely connect to the use of the product:

- Keep the text's case consistent (e.g., "Your Order is Ready for Purchase" shouldn't lead to "Congratulations, your order is complete!").
- Stay practical to what the thing actually does, or give concrete examples.
- Stay consistent with the first-person (e.g., "My Favorites"), second-person (e.g., "Your Inbox"), or strip it out altogether (e.g., "Inbox").
- Use the same choice of words for specific commands (e.g., "Continue" vs. "Next", "Back" vs. "Previous", "Home" vs. "Main").

Avoid using redundant text (e.g., "Enter your email and password" heading with "Your email address" above the entry).

Accessibility via text-to-speech is possible on all the major operating systems:

- macOS/iOS has VoiceOver (CMD+F5 or in the settings)
- Windows has Narrator (WIN+CTRL+ENTER)
- Linux has Orca for desktop and Speakup for the terminal
- Android has TalkBack (under Accessibility>TalkBack)

## Icons

For icons, use SVGs instead of icon fonts.

- They're easier and quicker to express, though they're harder to setup and take more memory on the host server.

## More information

[growth.design](https://growth.design/case-studies/)

Icons:

- [Icon Fonts are Awesome](https://css-tricks.com/examples/IconFont/)
- [Stop Using Icon Fonts](https://www.irigoyen.dev/blog/2021/02/17/stop-using-icon-fonts/)
