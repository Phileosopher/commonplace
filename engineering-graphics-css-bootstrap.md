
# Bootstrap specifics

Bootstrap is a straightforward CSS framework, similar to Tailwind. It standardizes lots of the CSS fiddling that normally would have to happen by writing CSS from scratch.

While it's not necessary to work with, Bootstrap also has JavaScript baked into it.

To start with, drop a link and the script into the header of the file.

## Structure

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

[LEFT OFF AT 22:45, ROWS](https://www.youtube.com/watch?v=Jyvffr3aCp0)
