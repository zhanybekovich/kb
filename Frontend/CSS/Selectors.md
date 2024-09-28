## Type Selectors

```css
html {
	color: black;
}

h1 {
	color: blue;
}
```

## Grouping Selectors

```css
h2, p {
	color: gray;
}
```

## Universal Selector

```css
* {
	font-weigh: bold;
}
```

## Class Selector

```css
.warning {
	color: yellow;
}
```

## ID Selector

```css
#lead {
	font-weight: bold;
}
```

## Attribute Selector

```css
a[href="http://www.css-discuss.org/about.html"] {
	font-weight: bold;
}

a[href="https://www.w3.org/"][title="W3C Home"] {
	font-size: 200%;
}

p[class="urgent warning"] {
	font-weight: bold;
}
```

### Partial Attribute Values

Selects any element with an attribute foo whose value contains the word bar in a space-separated list of words 

```css
[foo~="bar"] {
...
}
```

Selects any element with an attribute foo whose value contains the substring bar

```css
[foo*="bar"] {
...
}
```

Selects any element with an attribute foo whose value begins with bar

```css
[foo^="bar"] {
...
}
```

Selects any element with an attribute foo whose value ends with bar

```css
[foo$="bar"] {
...
}
```

Selects any element with an attribute foo whose value starts with bar followed by a hyphen (U+002D) or whose value is exactly equal to bar

```css
[foo|="bar"] {
...
}
```

Case insensitivity

```css
a[href$='.PDF' i]
```

## Descendant Selectors

```css
h1 em {
	color: gray;
}

ul ol ul em {
	color: gray;
}
```

### Child Combinator

Select `strong` element that is direct child of `h1`

```css
h1 > strong {
	color: red;
}
```

### Adjacent-Sibling

Select `p` that is immediately follows an `h1`

```css
h1 + p {
	margin: 0;
}
```

### Following Siblings

Select `ol` that follows `h1` and also shares a parent with `h1`

```css
h1 ~ ol {
	font-style: italic;
}
```

