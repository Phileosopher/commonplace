
# Useful HTML code

This is a quick reference for HTML.

Note: everything can be nested under endless ```<div></div>```

- It gets to be a pain, but divides out the idea

Meta tags are *huge* for [SEO](marketing-seo.md)

- They define what the web search indexer is looking for.
- In the age of [machine learning](computers-ai-ml.md), this is even more the case with contextual synonyms.

## Comments

<!--say what you want,
and nobody notices-->

## Headings and basic paragraph formats

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
<p>paragraph/body text</p>

<ul>
    <li>bullet point of unordered list<li>
    <li>another bullet point</li>
</ul>
<ol>
    <li>bullet point of ordered list<li>
    <li>another bullet point</li>
    <li>the list can have the handle "start=(number)" as well</li>
</ol>

```

## Expandable details/summary pane

```html
<details><summary></summary>
<!--body text here-->
</details>
```

## Tables

```html
<table>
    <thead>
        <th>Heading label 1</th>
        <th>Heading label 2</th>
    </thead>
    <tbody>
        <tr>
            <td>table row 1, table data 1</td>
            <td>table row 1, table data 2</td>
        </tr>
        <tr>
            <td>table row 2, table data 1</td>
            <td>table row 2, table data 2</td>
        </tr>
    </tbody>
</table>
```

## Input forms

The data is passed through to another site (the "action" handle alongside the "form" handle), which goes fully beyond the scope of HTML unless you're a hacker.

```html
<form>
    <label for="label">Label</label>
    <input type="text" id="input">
    <label for="select">Drop-down Selection</label>
    <select>
        <option>1</option>
        <option>2</option>
        <option>3</option>
    </select>
</form>
<button>Button</button>
```

NOTE: the "type" is optional and defaults to "text":

- plaintext (type=text)
  - type=email (validates)
  - type=url (validates)
  - type=number (validates)
  - type=tel (validates phone number)
  - type=password (obscures text visually)
- multiple-choice selection
  - type=checkbox
  - type=radio
  - type=range (slider)
- chronological selection
  - type=date (for hardkey/dropdown)
  - type=time (for hardkey)
  - type=datetime-local (for hardkey/dropdown with time as well)
- file selection (type=file)
  - type=image (doesn't always work)
- redundant button redundancies (since there is a "button" HTML handle)
  - type=button
  - type=submit (is simply a button that submits query)
- other weird ones
  - type=hidden
  - type=color
  - type=search (submits a search query)
  - type=reset (probably supposed to reset the form)
  - type=week (doesn't work?)
  - type=month (doesn't work?)

Input handles:

- readonly (makes the information read-only)
- disabled (similar to readonly but can't be focused by user selection)
- required (must be entered to submit query)
- value=(default value you want to place in it)
