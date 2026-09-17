
# The JavaScript programming language

JavaScript is the language of the [internet](cs-software-webdev.md), though the internet-based version of it is technically ECMAScript. HTML is the skeleton and CSS is the appearance of the internet, and JavaScript are the muscles.

In that sense, because of the internet's ubiquity, just about everything that *can* be written in JavaScript will eventually be written in it (Atwood's Law), and JavaScript will stick around as long as [the internet](cs-sofware-webdev.md) exists.

Further, JavaScript runs a huge chunk of [game development](cs-software-gamedev.md) and most front-end content for phones.

JavaScript's only connection to Java is that it was a marketing move. Java was hot at the time, so calling something JavaScript might get some programmers interested. It obviously worked, and has now outpaced Java in popularity.

JavaScript itself functions very simply as a .js [file](cs-files.md).

## Specific commands

Var is global, while let is far more specific. For this reason, use let unless you have a good reason not to.

Even with const, arrays can be mutable (i.e., push, pop, shift, unshift).

## Libraries

[The Rule of Least Power](technology-lawsaxioms.md) indicates that weaker programming languages are easier to secure and reuse. For this reason, [Atwood's Law](technology-lawsaxioms.md) indicates that everything will eventually be written in JavaScript.

Since JavaScript has basically had an implementation for everything, there are libraries for just about everything. It's rarely well-optimized, but it usually works fine.

Within the domain of visual development, two major libraries have arisen to create [visual expression](art-design-visual.md) when [CSS](art-design-visual-css.md) isn't sufficient:

- Vue has strictly HTML-based template syntax and directives, so it's more of a template-based methodology than an actual library.
- React relies on JSX, which is HTML-like markup *within* JS files.
- They both use "state management", which diredts how the interface changes.
- Svelte was designed for a specific problem in web optimization. Since React has a runtime virtual DOM, it ships with ~42KB, so Svelte compiles the components to direct DOM updates at build time, which makes bundles that are 2-5KB with almost no DOM overhead.
