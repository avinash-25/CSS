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
display: grid; /* Generate block-level grid */
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

- auto and 1fr are same.

### 15.




## ~ Grid Item Properties

CSS Grid item properties allow you to position and control individual grid items within a grid container. These properties give you precise control over where items are placed and how they behave.

## Grid Line Positioning Properties

### 1. `grid-row-start`
Specifies which row line the grid item starts on.

```css
grid-row-start: value;
```

**Values:**
- `1, 2, 3...` - Line numbers (starting from 1)
- `span n` - Span across n rows
- `auto` - Automatic placement (default)

**Example:**
```css
.item {
  grid-row-start: 2; /* Start at row line 2 */
}
```

### 2. `grid-row-end`
Specifies which row line the grid item ends on.

```css
grid-row-end: value;
```

**Values:**
- `1, 2, 3...` - Line numbers
- `span n` - Span n rows from start position
- `auto` - Automatic placement (default)

**Example:**
```css
.item {
  grid-row-end: 4; /* End at row line 4 */
}
```

### 3. `grid-column-start`
Specifies which column line the grid item starts on.

```css
grid-column-start: value;
```

**Values:**
- `1, 2, 3, 4...` - Column line numbers
- `span n` - Span across n columns
- `auto` - Automatic placement (default)

**Example:**
```css
.item {
  grid-column-start: 1; /* Start at column line 1 */
}
```

### 4. `grid-column-end`
Specifies which column line the grid item ends on.

```css
grid-column-end: value;
```

**Values:**
- `1, 2, 3, 4...` - Column line numbers
- `span n` - Span n columns from start position
- `auto` - Automatic placement (default)

**Example:**
```css
.item {
  grid-column-end: 3; /* End at column line 3 */
}
```

## Shorthand Properties

### 5. `grid-row` (Shorthand for grid-row-start / grid-row-end)
Combines `grid-row-start` and `grid-row-end` in a single declaration.

```css
grid-row: start / end;
```

**Syntax:**
- `grid-row: 1 / 3;` - Start at line 1, end at line 3
- `grid-row: 2 / span 2;` - Start at line 2, span 2 rows
- `grid-row: span 3;` - Span 3 rows from auto start

**Example:**
```css
.item {
  grid-row: 2 / 4; /* Start at row 2, end at row 4 */
}
```

### 6. `grid-column` (Shorthand for grid-column-start / grid-column-end)
Combines `grid-column-start` and `grid-column-end` in a single declaration.

```css
grid-column: start / end;
```

**Syntax:**
- `grid-column: 1 / 4;` - Start at column 1, end at column 4
- `grid-column: 2 / span 3;` - Start at column 2, span 3 columns
- `grid-column: span 2;` - Span 2 columns from auto start

**Example:**
```css
.item {
  grid-column: 1 / 3; /* Start at column 1, end at column 3 */
}
```

## Self-Alignment Properties

### 7. `justify-self`
Aligns the grid item horizontally (along the inline/row axis) within its grid area.

```css
justify-self: value;
```

**Values:**
- `stretch` - Stretch to fill the grid area (default)
- `start` - Align to the start of the grid area
- `end` - Align to the end of the grid area
- `center` - Center within the grid area

**Example:**
```css
.item {
  justify-self: center; /* Center horizontally */
}
```

### 8. `align-self`
Aligns the grid item vertically (along the block/column axis) within its grid area.

```css
align-self: value;
```

**Values:**
- `stretch` - Stretch to fill the grid area (default)
- `start` - Align to the start of the grid area
- `end` - Align to the end of the grid area
- `center` - Center within the grid area

**Example:**
```css
.item {
  align-self: end; /* Align to bottom */
}
```

## Ultimate Shorthand Property

### 9. `grid-area`

The most powerful shorthand that can define all grid item positioning in one declaration.

```css
grid-area: row-start / column-start / row-end / column-end;
```

**Alternative syntax with named areas:**
```css
grid-area: area-name;
```

**Examples:**
```css
/* Position using line numbers */
.item1 {
  grid-area: 1 / 1 / 3 / 3; /* row-start / col-start / row-end / col-end */
}

/* Using named grid areas */
.item2 {
  grid-area: header; /* Must match a named area in grid-template-areas */
}

/* Mixed syntax */
.item3 {
  grid-area: 2 / 1 / span 2 / span 3;
}
```

## Practical Examples

### Complete Grid Layout Example

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 100px 200px 100px;
  gap: 10px;
}

.header {
  grid-area: 1 / 1 / 2 / 4; /* Span full width */
}

.sidebar {
  grid-column: 1;
  grid-row: 2;
}

.main-content {
  grid-column: 2 / 4; /* Span 2 columns */
  grid-row: 2;
  justify-self: stretch;
  align-self: center;
}

.footer {
  grid-area: 3 / 1 / 4 / 4; /* Full width footer */
}
```

## Key Concepts to Remember

- **Grid lines** are numbered starting from 1
- **Negative numbers** count from the end of the grid
- **`span` keyword** creates items that span multiple tracks
- **Shorthand properties** reduce code and improve readability
- **Self-alignment properties** control item positioning within their assigned grid area
- **`grid-area`** is the ultimate shorthand for complete item positioning





<br><br><br><br><br><br><br>

**_Topic For interview_**

- Lazy loading
- optimization
- How to handle load
- Mmicro frontend
- Fibre
