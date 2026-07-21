# CSS Basics

CSS (Cascading Style Sheets) is the language used to style and design web pages. It controls the appearance of HTML elements such as colors, fonts, spacing, layouts, animations, and responsive behavior.

---

# What is CSS?

## Definition

**CSS (Cascading Style Sheets)** is a stylesheet language used to describe the presentation of HTML documents.

HTML provides the **structure** of a webpage, while CSS controls its **appearance**.

Without CSS, web pages would display only plain HTML elements with the browser's default styles.

---

## Example

### HTML

```html
<h1>Hello World</h1>
<p>Welcome to CSS.</p>
```

### Without CSS

- Black text
- White background
- Default browser font

### With CSS

```css
h1 {
    color: blue;
}

p {
    color: gray;
}
```

### Output

- Heading becomes blue.
- Paragraph becomes gray.

---

## Real-Life Analogy

Think of a house:

- **HTML** → Structure of the house (walls, doors, windows)
- **CSS** → Paint, furniture, decoration, lighting
- **JavaScript** → Electricity, switches, smart devices

---

# Why is CSS Used?

CSS is used to improve the appearance and usability of websites.

## Benefits of CSS

### 1. Makes Websites Attractive

CSS allows you to add colors, fonts, backgrounds, borders, and layouts.

Example:

```css
h1 {
    color: royalblue;
}
```

---

### 2. Separates Design from Content

HTML stores the content.

CSS stores the design.

This makes websites easier to maintain.

---

### 3. Reuse Styles

One CSS file can style hundreds of HTML pages.

Example:

```html
<link rel="stylesheet" href="style.css">
```

---

### 4. Responsive Design

CSS helps websites look good on:

- Mobile
- Tablet
- Laptop
- Desktop

Example:

```css
@media (max-width: 768px) {
    body {
        font-size: 14px;
    }
}
```

---

### 5. Faster Website Maintenance

Instead of changing every HTML page individually, update one CSS file.

---

### 6. Better User Experience

CSS provides:

- Hover effects
- Animations
- Smooth transitions
- Better spacing
- Better readability

---

# CSS Syntax

## Definition

A CSS rule consists of a **selector** and a **declaration block**.

## Syntax

```css
selector {
    property: value;
}
```

### Structure

```css
h1 {
    color: blue;
}
```

Here:

- `h1` → Selector
- `color` → Property
- `blue` → Value

---

## Multiple Properties

```css
h1 {
    color: blue;
    font-size: 40px;
    text-align: center;
}
```

---

## Multiple Rules

```css
h1 {
    color: blue;
}

p {
    color: gray;
}
```

---

# CSS Comments

## Definition

Comments are ignored by the browser.

They are used to explain code or temporarily disable CSS rules.

## Syntax

```css
/* This is a comment */
```

---

## Example

```css
/* Main Heading */

h1 {
    color: blue;
}

/* Paragraph */

p {
    color: gray;
}
```

---

## Multi-line Comment

```css
/*
This is a
multi-line
comment.
*/
```

---

## Why Use Comments?

- Explain code
- Improve readability
- Organize sections
- Disable CSS temporarily during testing

---

# CSS Types

There are three ways to apply CSS.

---

# 1. Inline CSS

## Definition

Inline CSS applies styles directly inside an HTML element using the `style` attribute.

## Syntax

```html
<tag style="property: value;">
```

## Example

```html
<h1 style="color: blue;">Hello World</h1>
```

---

## Advantages

- Quick styling
- Useful for testing
- Overrides many other styles

---

## Disadvantages

- Difficult to maintain
- Cannot be reused
- Not recommended for large projects

---

# 2. Internal CSS

## Definition

Internal CSS is written inside the `<style>` tag in the `<head>` section of an HTML document.

## Example

```html
<!DOCTYPE html>

<html>

<head>

<style>

h1 {
    color: blue;
}

p {
    color: gray;
}

</style>

</head>

<body>

<h1>Hello</h1>

<p>Welcome</p>

</body>

</html>
```

---

## Advantages

- Easy for small projects
- No separate CSS file needed

---

## Disadvantages

- Cannot be reused across multiple pages
- Increases HTML file size

---

# 3. External CSS

## Definition

External CSS stores all styles in a separate `.css` file.

The HTML page links to the CSS file.

## HTML

```html
<link rel="stylesheet" href="style.css">
```

## style.css

```css
h1 {
    color: blue;
}

p {
    color: gray;
}
```

---

