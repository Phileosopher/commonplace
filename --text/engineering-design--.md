
### Example blueish palette

Monotone:

- White-ish Card background: #FCFCFC
- Blueish-Black icons: #1C1E20
- Lighter text on white: #485963
- Bluish background: #202D34

Multicolor:

- Black: #1d1d1d.
- purple: #b066ff;
- blue: #203447;
- lightblue: #1f4662;
- blue2: #1C2F40;
- yellow: #ffc600;
- pink: #EB4471;
- white: #d7d7d7;

You may or may not want to use generic names if you want it swappable for dark mode:

### Yellow palette

Example [yellowish palette](https://codepen.io/oliviale/full/XyqQYL):

- primary-light: #FFD151 mustard
- primary-dark: #FFAE03 UCLA gold
- secondary-success: #20A39E light sea green
- secondary-warning: #EF5B5B sunset orange
- secondary-info: #08D377 dark cerulean
- grays: #E8E9E9, #D1D3D4, #BABDBF, #808488, #666A6D, #4D5052, #333537, #1C1D1E

Note - THIS IS DISPUTED!!! Even Slack's impl has separate light and dark theming.

> The problem is "primary" isn't a color, it's a measure of contrast in the current context. On the same page you might have a white panel with a black button and a black panel with a white button, and both of those buttons are "primary" even though they are different colors. - Adam Wathan

One liner dark mode (careful about perf!)

## centering

Easy way to make your text look balanced

Previously, I remember there were libraries calculating that stuff, for example, [React Wrap Balancer](https://react-wrap-balancer.vercel.app/).

But now, it's possible to do with pure CSS.
​
It's probably been around for years, but I learned about it a year ago.
​
Two options that save my life:

text-wrap: balance and text-wrap: pretty.
​
The first one makes your text balanced (not too lengthy, not too short, sustaining optimal line length).

The second ensures you don't have orphans (single words at the end of a line).

## ux

[Apple vs. Meta: The Illusion of Privacy | Hacker News](https://news.ycombinator.com/item?id=37433495)
[Apple vs Meta: The Illusion of Privacy](https://growth.design/case-studies/apple-privacy-policy)

- clarify the TI ratio, since that is VERY important
- Transparency/Intrusiveness ratio
	- i.e., be transparent proportionally to being intrusive
- (also, roach motel dark pattern)
	- https://blog.mobiversal.com/dark-patterns-or-how-ux-exploits-the-user-roach-motel-and-sneak-into-basket.html
- Clarify "privacy washing"
