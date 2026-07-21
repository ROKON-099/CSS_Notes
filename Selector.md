# CSS Selectors

CSS selectors are used to **select HTML elements** so that you can apply styles to them. A selector tells the browser **which element(s) should receive the CSS rules**.

---

# 1. Universal Selector (`*`)

## Definition

The **Universal Selector** selects **every element** on the page.

It is commonly used for CSS reset or applying a common style to all elements.

## Syntax

```css
* {
    property: value;
}
```

## Example

### HTML

```html
<h1>Welcome</h1>
<p>This is a paragraph.</p>
<button>Click Me</button>
```

### CSS

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

## Output

- All elements have zero margin.
- All elements have zero padding.
- Every element uses `border-box`.

## Common Use Cases

- CSS Reset
- Global Font
- Global Box Sizing

---

# 2. Element Selector

## Definition

The **Element Selector** selects all HTML elements of the specified tag name.

## Syntax

```css
element {
    property: value;
}
```

## Example

### HTML

```html
<h1>CSS Notes</h1>

<p>Paragraph One</p>
<p>Paragraph Two</p>
```

### CSS

```css
p {
    color: blue;
}
```

## Output

Both paragraphs become blue.

---

# 3. Class Selector (`.`)

## Definition

The **Class Selector** selects elements with the specified class name.

Multiple elements can use the same class.

## Syntax

```css
.class-name {
    property: value;
}
```

## Example

### HTML

```html
<p class="text">Paragraph One</p>

<p class="text">Paragraph Two</p>

<h2 class="text">Heading</h2>
```

### CSS

```css
.text {
    color: green;
    font-weight: bold;
}
```

## Output

All elements having the class `text` become green and bold.

## Why Use Class?

- Reusable
- Recommended for styling
- Can be used multiple times

---

# 4. ID Selector (`#`)

## Definition

The **ID Selector** selects one unique element with the specified ID.

An ID should be unique on a page.

## Syntax

```css
#id-name {
    property: value;
}
```

## Example

### HTML

```html
<h1 id="title">CSS Tutorial</h1>
```

### CSS

```css
#title {
    color: crimson;
}
```

## Output

Only the heading with id `title` becomes crimson.

## Why Use ID?

- Styling a unique element
- JavaScript targeting
- Navigation (Anchor Links)

---

# 5. Group Selector (`,`)

## Definition

The **Group Selector** applies the same style to multiple selectors.

Instead of writing separate CSS rules, multiple selectors are separated using commas.

## Syntax

```css
selector1,
selector2,
selector3 {
    property: value;
}
```

## Example

### HTML

```html
<h1>Heading</h1>

<p>Paragraph</p>

button>Click</button>
```

### CSS

```css
h1,
p,
button {
    font-family: Arial;
}
```

## Output

Heading, paragraph, and button use the Arial font.

## Benefit

Reduces duplicate CSS code.

---

# 6. Descendant Selector (Space)

## Definition

The **Descendant Selector** selects all matching elements inside another element, regardless of nesting level.

## Syntax

```css
parent child {
    property: value;
}
```

## Example

### HTML

```html
<div>
    <p>Paragraph 1</p>

    <section>
        <p>Paragraph 2</p>
    </section>
</div>
```

### CSS

```css
div p {
    color: blue;
}
```

## Output

Both paragraphs become blue.

Because both are inside the `div`.

---
# 7. Child Selector (`>`)

## Definition

The **Child Selector** selects only the direct children of an element.

It does not select grandchildren or deeper descendants.

## Syntax

```css
parent > child {
    property: value;
}
```

## Example

### HTML

```html
<div>

    <p>Paragraph 1</p>

    <section>
        <p>Paragraph 2</p>
    </section>

</div>
```

### CSS

```css
div > p {
    color: red;
}
```

## Output

Only Paragraph 1 becomes red.

Paragraph 2 remains unchanged because it is inside the section.

---

# 8. Adjacent Sibling Selector (`+`)

## Definition

The **Adjacent Sibling Selector** selects the immediate next sibling element.

## Syntax

```css
element + element {
    property: value;
}
```

## Example

### HTML

```html
<h2>Heading</h2>

<p>Paragraph One</p>

<p>Paragraph Two</p>
```

### CSS

```css
h2 + p {
    color: blue;
}
```

## Output

Only Paragraph One becomes blue.

Paragraph Two is not selected.

---

# 9. General Sibling Selector (`~`)

## Definition

The **General Sibling Selector** selects all sibling elements that come after the first element.

## Syntax

```css
element ~ element {
    property: value;
}
```

## Example

### HTML

```html
<h2>Heading</h2>

<p>Paragraph One</p>

<p>Paragraph Two</p>

<p>Paragraph Three</p>
```

### CSS

```css
h2 ~ p {
    color: green;
}
```

## Output

All paragraphs become green because they are siblings after the heading.

---

# 10. Attribute Selector (`[]`)

## Definition

The **Attribute Selector** selects elements based on their HTML attributes.

## Syntax

```css
element[attribute] {
    property: value;
}
```

## Example 1

### HTML

```html
<input type="text">

<input type="password">
```

### CSS

```css
input[type="text"] {
    border: 2px solid blue;
}
```

## Output

Only the text input gets the blue border.

---

## Example 2

### HTML

```html
<a href="https://google.com">Google</a>

<a>Home</a>
```

### CSS

```css
a[href] {
    color: red;
}
```

## Output

Only the link that has the `href` attribute becomes red.

---

# Summary Table

| Selector | Symbol | Selects |
|-----------|--------|---------|
| Universal | `*` | Every element |
| Element | `p` | All specified HTML elements |
| Class | `.` | Elements with the same class |
| ID | `#` | One unique element |
| Group | `,` | Multiple selectors together |
| Descendant | ` ` (space) | All matching descendants |
| Child | `>` | Direct children only |
| Adjacent Sibling | `+` | Immediate next sibling |
| General Sibling | `~` | All following siblings |
| Attribute | `[]` | Elements with specific attributes |

---

# Best Practices

- Use **class selectors** for reusable styles.
- Use **ID selectors** only for unique elements.
- Avoid overusing the universal selector (`*`) because it affects every element.
- Prefer **group selectors** to reduce duplicate CSS.
- Use **child (`>`)** or **descendant (` `)** selectors carefully to keep styles predictable.
- Use **attribute selectors** for forms, links, and custom attributes.
