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

