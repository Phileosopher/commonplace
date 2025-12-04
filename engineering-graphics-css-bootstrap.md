
# Bootstrap specifics

Bootstrap is a straightforward CSS framework, similar to Tailwind. It standardizes lots of the CSS fiddling that normally would have to happen by writing CSS from scratch.

While it's not necessary to work with, Bootstrap also has JavaScript baked into it.

To start with, drop a link and the script into the header of the file.

## Basic structure

It's composed of 3 major elements:

1. Containers - wraps the grid system, big boxes to hold stuff
   - `<div class="container">`
   - The containers also have templates: container-fluid, container-lg, etc
2. Rows - vertically parses the containers, nested inside "container"
   - `<div class="row">`
3. Columns - horizontally parses the rows, nested inside "row"
   - `<div class="col">`

- Rows and columns can be recursively nested inside each other, but all columns should sit directly inside rows and all rows should sit directly inside containers

The sizes are based on viewport breakpoints:

- <576px XS
- 576-767px SM
- 768-991px MD
- 992-1199 Large
- 1200-1399 XL
- >1400 XXL

It uses the CSS flexbox standard (W3C compliant)

The columns can be configured

- uses 12 hardcoded column sizes
  - the elements can span that length:
    - "col-2" = 1/6 of the row
    - "col-6" = 1/2 of the row
  - if there isn't enough space, the columns will just fill whatever space remaining possible
- "col-auto" will take up the space necessary for the elements inside it
- can specify hard limits, such as "col-lg-3 col-4" to make it 4 columns normally except 3 when on the large or higher viewport
  - without a hardcoded default, it'll default to col-12
- can offset columns, such as "col offset-2" to shift it over by 2 columns
- anything surpassing the 12th column returns to the next line

The rows have conditions that can make columns easier to work with

- Rows can be specified to give a different number of columns per row than 12
  - "row row-cols-2" = 2 columns per row
- There can be conditions for specific breakpoints
  - "row row-cols-2 row-cols-lg-4" = 2 columns per row, except 4 on large or higher
- A gap can be inserted on the X or Y axis
  - "row g-3" = spacing of 3 in both directions
  - "row gx-3 gy-2" = spacing of 3 on X axis and 2 on Y axis

## Tables

Bootstrap works off of HTML tables

- `<table class="table">`
- there are themes within Bootstrap for coloring tables
  - there are 8 to choose from
    - primary
    - secondary
    - success
    - danger
    - warning
    - info
    - light
    - dark
  - `<table class="table table-success">`
  - `<tr class="table-danger">`
  - `<td class="table-warning">`
  - It can also alternate colors:
    - "table-striped" = alternating rows
    - "table-striped-columns" = alternating columns
  - "table-hover" places a contrasting style over the mouseover
  - "table-active" is as if it were being hovered over
- borders can be added or removed
  - "table-bordered" = more borders
  - "table-borderless" = remove borders
- "table-sm" makes the elements smaller to show more information
- `<div class="table-responsive">` allows responsive design (i.e., scrolls sideways)
  - without this, it'll just overflow past the screen
  - "table-responsive-lg" makes it responsive up until that size
- dividers can be applied to thead, tbody, or tfooter:
  - `<thead class="table-group-divider">`
  - it places a vertical line to visually divide it

## Forms

Bootstrap works off of HTML forms

- label is given a class of "form-label"
- input is given a class of "form-control"
  - can be form-control-sm or form-control-lg
- specific input types have default classes
  - form-control-plaintext (i.e., no box around it)
    - form-control-plaintext with the "readonly" handle will make the form look like it's just part of the content
  - form-control-color for a standardized color picker
  - form-range for a standardized slider (no form-control class!)
  - for checkboxes:
    - make sure it sits inside a "div" with "form-check" class
      - make it "form-check form-switch" to make a switch
      - they default to stacking on top of each other, but "form-check-inline" puts them on the same line
    - form-check-input for the input
    - form-check-label for the label
- in "select" HTML, use form-select
  - can also be form-select-sm or form-select-lg

Floating labels are where there's a label inside the text box, which then becomes small text above the input when the box is selected

1. there must be an "input", then a "label" HTML tag
2. the "input" needs a "placeholder" of whatever text you want for a digital reader (doesn't express in most use cases)
2. wrap the entire "input" and "label" tags inside a div with "form-floating" class
   - you can even remove the "form-label" class from the "input" tag and it'll still work fine

There are other visuals for form validation

1. add "novalidate" to the form HTML tag
   - this will make "required" handles fail
2. paste the following into a "script" HTML tag later:
   ```javascript
    const form = document.querySelector("form")

    form.addEventListener('submit', e => {
      if (!form.checkValidity()) {
        e.preventDefault()
      }

      form.classList.add('was-validated')
    })
    // it prevents the default checkValidity of the browser, then adds a class to Bootstrap called "was-validated"
   ```
3. use "was-validated" only on the input handles

- adding the class "is-valid" or "is-invalid" gives a visual demarcation of whether the input box is validated upon page load
- adding a div with class "valid-feedback" and "invalid-feedback" after the input allows text information to give feedback

## Input groups

it allows multiple elements to sit on one line

- input-group class makes all the inputs side-by-side with rounded edges around the whole thing
  - can also be input-group-sm and input-group-lg
- input-group-text makes a readonly grayed-out input box (for presentation purposes)
  - this allows a guided flow through user input

## Specific components

There are a LOT of components, far too many to count

- However, there are some that keep emerging more than others

Buttons

- class "btn"
- can be btn-primary, btn-danger etc
- can have an anchor tag (i.e., hyperlink) styled like a button
  - can add "disabled" tag to disable the anchor tag (will also need to remove the "href" handle or it'll still work)
- btn-link makes a button look like a hyperlink
- can be resized with btn-sm, btn-lg
- adding data-bs-toggle="button" allows toggling of the button's state (a JavaScript-controlled condition)
  - aria-pressed="True" will give the active state of the button
- a div with "btn-group" works similarly to other input groups
  - can be btn-group-lg or btn-group-sm
  - can also be btn-group-vertical (be sure to remove default btn-group class)

Alerts

- class "alert"
  - can have HTML inside it (h1, p, etc.)
- indicates text that lets the user know about something
  - can be alert-link, alert-dark, alert-primary, alert-success, alert-danger, etc.
- can be closeable with alert-dismissible and:
  ```<button  class="btn-close" aria-label="close" data-bs-dismiss="alert">```
- a link with class alert-link will style a hyperlink inside the alert
- can show a neat fading effect with "fade show" added to the alert handle

Cards

- a visual representation of a card
- div with class "card", and div inside with class "card-body"
- can also have "card-title", "card-subtitle", "card-text" for granular emphasis
- can also have img HTML with card-img-top or card-img-bottom
  - can add style="width: 100px;" to adapt the CSS inside it
  - can add card-img-overlay to set the image behind the text
- can have card-header and card-footer for further divisions on the card
- can do a div with card-group to create same as input-group

Modals

- a visual overlay that sits atop everything else
  - almost everything else (buttons, h1, p, etc.) can be added inside the modal
  - NOTE: FOR UX REASONS USE THIS ONE SPARINGLY!!
- 3 nested div classes:
  1. "modal"
  2. "modal-dialog"
     - can be modal-dialog-scrollable to make scrolling text inside the modal (instead of scrolling the whole page)
     - can add modal-sm, modal-lg, modal-xl, modal-fullscreen, etc.
       - can also add more breakpoints (e.g., modal-fullscreen-md-down will make it fullscreen from medium-sized downward)
  3. "modal-content"
- button sits above the modal with data-bs-toggle="modal" and data-bs-target="#(the modal's id)" to link it
- IMPORTANT: add a button inside the modal with data-bs-dismiss="modal" and data-bs-target="#(the modal's id)" to dismiss the modal
- can add fade class to make it nicer
- can demarcate modal-header, modal-body, modal-footer

[LEFT OFF AT 51:54](https://www.youtube.com/watch?v=Jyvffr3aCp0)

- collapse
- navbars
- color utilities
- stack utilities
- border utilities
- display utilities
- spacing utilities
- flexbox utilities
