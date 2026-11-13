
# CSS

Everyone in the computers industry who will ever visually design anything that isn't inside [a terminal](cs-cli.md) will have to face GUI issues, and CSS is the standard for working with GUI elements. Therefore, everyone should become at least remotely familiar with CSS code and how it works.

- It's truly not possible to master CSS, since they are *constantly* making new frameworks, constantly updating styles and conventions, and the community is a crowd of [artists](mind-creativity.md) that moves with every new visual concept or trend.

Cascading Style Sheets (CSS) is, essentially, a bunch of boxes. It groups everything into a set of stylesheets, which can then expand into more specific sheets that override those previous rules as things become more specific.

- Many CSS developers use !important as a manual override, but the entire purpose for it was simply to ensure guaranteed government compliance, and any other usage of !important is probably a misuse of it.
- The position can be either absolute or relative to some other reference point (usually as a relationship to its containing box).

Historically, CSS layouts now work with 4 major design systems:

1. Table, which is the oldest one and still used for a few things like email.
2. Float, which is still used for articles that have inline images.
3. Flexbox, which is the most used one today and allows adaptive interfaces based on design needs.
4. Grid, which is an expansion of flexbox as a modern alternative to Table.

Compared to JavaScript, CSS is usually far less resource-intensive, so it's worth research absolutely *anything* that can be done with CSS:

- Parallax effects
- Transitions
- SVG alterations
- Many smaller-use modal windows
- Assigning and working with variables

## Responsive web design

One of the most time-consuming and nitpicky parts of modern [user interface design](engineering-design-cs.md) is that there are many, *many* devices, with various sizes.

- While its great to use absolute references like px/in/cm, CSS has multiple relative units:
  - rem: relative to the root element's font size
  - em: relative to the parent element's font size
  - vh: relative to the viewport height (i.e., the scope of the screen/browser/window that's visible)
  - vw: relative to the viewport width

For that reason, things like Grid (for two-dimensional information flow) and Flexbox (for one-dimensional information flow) are absolutely necessary to avoid your website being inaccessible from the many permutations of designed computer interfaces.

Further, media queries allow for more complexity by providing conditions that make everything work according specific conditions.

- A breakpoint is a key to determine when to change the layout and adapt the new rules inside the media queries.
- There are at least *some* standards on breakpoint device dimensions, though they do move around:
  - 576px and under: Extra small
  - 576-767px: Small
  - 768-991px: Medium
  - 992-1199px: Large
  - 1200-1399px+: XL
  - 1400+px: XXL

To keep things simpler, mobile devices are by far the most constricting with their limited real estate, so most web design is built mobile-first and scales up for larger screens. It also happens to work well for [SEO](marketing-seo.md) reasons. This comes with the downside of making complex features harder to express.

One of the most common standards which has emerged in websites is the Holy Grail layout, which is very easy to accomplish with CSS Grid:

1. There's a header and footer.
2. There are two sidebars, one on the left and right.
3. There's a main content area, which takes priority.
4. All other sections adjust responsibly to the main content area.
5. Altogether, this can basically be a 3x3 grid with variances based on design needs.

It's worth noting that every new feature of CSS is another complexity, and it's wise to avoid anything that gets in the way of good-quality design for everyone.

- Instead of aiming for designing for any specific device, aim instead for approximate sizes, with the assumption that people will be viewing it on the smallest possible screen of that size.
- It also helps to assume the user could be nearsighted, color-blind, deaf, and have a severely limited attention span.
- This gives constraints that essentially mean most visual embellishments should never affect the core functionality of the visual presentation.

## Specificity

It's called *Cascading* Style Sheets because the styles cascade into specificity.

- When there is a conflict in styles, it picks the most specific style.

Style distinction runs through an [algorithm](cs-langs-algorithms.md):

1. relevance: filters only the rules that apply to the element in question
2. origin and importance: examines user-agent (i.e., [browser](cs-browser.md)), user styles, and author styles
3. specificity: chooses the most specific one
4. order of appearance: does the last one if the specificity value is the same for multiple things

There are four classes of specificity:

1. inline styles (boolean 0/1)
2. ID selectors (the count of them that apply)
3. class and attribute selectors, as well as pseudo-classes like :hover (count)
4. universal selectors, type selectors, and pseudo-elements like ::before (count)

all of these add to whatever is highest, and then it picks the class above that is most applicable:

- e.g., 1 inline style and 1 ID selector becomes (1,1,0,0), so it chooses the inline styles that apply

Sometimes there's inheritance:

- Properties like font and color are inherited.
  - Properties like margin, padding, border, and background are NOT inherited.
  - (property):inherit on the child element allows mandatory inheritance.

Overriding styles makes sense sometimes.

- You can simply use !important to brute-force the style all the way to the top
- If you want a general rule to *always* apply with exceptions, stick it under the * style.

## Pseudo-scripting

One fun addition to CSS that makes it more like a programming language is that you can set variables that can be reused in more specific domains (a bit like global vs. local variables):

- e.g., :root{--maincolor:#fff}, then .text{color:var(--maincolor)}
- This makes life *much* easier in making themes, especially since you can redefine them within the context of media breakpoints (e.g., --cardwidth:90%, but under 500px --cardwidth:70%).

Defining a property can also create many conditions at once piled into a variable:

- e.g.:
  - @property --propertyname {
      syntax: (<color/number/length/percentage/whatever>);
      inherits: true|false;
      initial value: (something);
    }
  - then call --propertyname

Variables can also have fallbacks just in case other variables fail (e.g., var(--maincolor,#fff)).

## Code snips

```css
/* LOOKS GOOD ANYWHERE */
main {
  max-width: 38rem;
  padding: 2rem;
  margin: auto;
}
```

```css
/* HIDE FROM SCREEN READERS */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
```
