
# CSS

Style distinction:

- it runs through an [algorithm](computers-programming-algorithms.md):
  1. relevance: filters only the rules that apply to the element in question
  2. origin and importance: examines user-agent (i.e., [browser](computers-browser.md)), user styles, and author styles
  3. specificity: chooses the most specific one
  4. order of appearance: does the last one if the specificity value is the same for multiple
- The reason it's called *Cascading* Style Sheets is because the styles cascade into specificity.
- When there is a conflict in styles, it picks the most specific style.
- There are four classes of specificity:
  1. inline styles (boolean 0/1)
  2. ID selectors (the count of them that apply)
  3. class and attribute selectors, as well as pseudo-classes like :hover (count)
  4. universal selectors, type selectors, and pseudo-elements like ::before (count)
- all of these add to whatever is highest, and then it picks the class above that is most applicable:
  - e.g., 1 inline style and 1 ID selector becomes (1,1,0,0), so it chooses the inline styles that apply
- inheritance sometimes happens:
  - properties like font and color are inherited.
  - properties like margin, padding, border, and background are NOT inherited.
  - (property):inherit on the child element allows mandatory inheritance.
- overriding styles makes sense sometimes.
  - you can simply use !important to brute-force the style all the way to the top
  - If you want a general rule to ALWAYS apply with exceptions, stick it under the * style.

```css
/* LOOKS GOOD ANYWHERE */
main {
  max-width: 38rem;
  padding: 2rem;
  margin: auto;
}
```
