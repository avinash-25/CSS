# CSS Grid Layout

CSS Grid is a **two-dimensional layout module** that provides powerful tools for creating complex web layouts.

## Grid Terminology

### 1. Grid Lines
Grid lines are horizontal and vertical lines that run through the entire CSS grid. These lines separate elements from one another. In a table analogy, the lines which separate the columns are grid lines.

### 2. Grid Tracks
The space between any two consecutive grid lines is called a grid track. It is basically the space or area between the lines.

### 3. Grid Cells
Grid cells are the space present between any four intersecting grid lines. From the table analogy, every table cell can be thought of as a grid cell too. It is the smallest unit in CSS grid.

### 4. Grid Areas
Grid areas are nothing but a collection of grid cells that form a rectangular area on the grid. Grid areas can be of 1 cell or multiple cells.

### 5. Grid Columns
Grid columns are similar to grid tracks. The space between any two adjacent vertical grid lines is known as a grid column. The columns in a table can be considered as grid columns.

### 6. Grid Rows
The space between any two adjacent horizontal grid lines is known as a grid row. The rows in a table can be considered as grid rows. It is similar to grid tracks.

### 7. Gutters
When you want a gap between two adjacent rows or columns, a gutter is created. In short, gutter is the space between any two adjacent rows or columns.

## Grid Container Properties

### 1. `display`
```css
display: grid;        /* Generate block-level grid */
display: inline-grid; /* Generate inline-level grid */
```
It defines the element as a grid container.

### 2. `grid-template-columns`
```css
grid-template-columns: size_of_column_1 size_of_column_2 size_of_column_3;
```
It is used to create columns inside the grid.

### 3. `grid-template-rows`
```css
grid-template-rows: size_of_row_1 size_of_row_2 size_of_row_3;
```
It is used to create rows inside the grid.

### 4. `grid-template`
```css
grid-template: grid_template_rows / grid_template_columns;
```
It is the shorthand property of `grid-template-rows` and `grid-template-columns`.

### 5. `gap`
```css
gap: row_gap column_gap;
```
It is used to create gutters.

### 6. `justify-items`
```css
justify-items: value;
```
It aligns items in rows (horizontally).

### 7. `align-items`
```css
align-items: value;
```
It aligns items vertically (in columns).

### 8. `place-items`
```css
place-items: align-items justify-items;
```
It is the shorthand property of `align-items` and `justify-items`.

### 9. `justify-content`
```css
justify-content: value;
```
It is used to align the grid horizontally inside the grid container.

### 10. `align-content`
```css
align-content: value;
```
It is used to align the grid vertically inside the grid container.

### 11. `place-content`
```css
place-content: align-content justify-content;
```
It is the shorthand property of `align-content` and `justify-content`.

### 12. `grid-auto-flow`
```css
grid-auto-flow: value;
```
It is used to define how the auto-placement algorithm works.

### 13. `grid-auto-rows`
```css
grid-auto-rows: size;
```
It defines the size of any auto-generated rows.

### 14. `grid-auto-columns`
```css
grid-auto-columns: size;
```
It defines the size of any auto-generated columns.


### 15. 




















<br><br><br><br><br><br><br>


***Topic For interview***

- Lazy loading
- optimization
- How to handle load
- Mmicro frontend
- Fibre