---
title: 30 CSS Selectors
layout: snippet
comments: false
---

## 30 CSS Selectors

<p>1. *</p>

```css
* {
  margin: 0;
  padding: 0;
}
```

Let's knock the obvious ones out, for the beginners, before we move onto the more advanced selectors. The star symbol will target every single element on the page. It adds too much weight on the browser, and is unnecessary. The * can also be used with child selectors.

```css
#container * {
  border: 1px solid black;
}
```

This will target every single element that is a child of the #container div. Again, try not to use this technique very much, if ever.

---

<p>2. #X</p>

```css
#container {
  width: 960px;
  margin: auto;
}
```

Prefixing the hash symbol to a selector allows us to target by id. This is easily the most common usage, however be cautious when using id selectors.

id selectors are rigid and don't allow for reuse. If possible, first try to use a tag name, one of the new HTML5 elements, or even a pseudo-class.

---

<p>3. .X</p>

```css
.error {
  color: red;
}
```

This is a class selector. The difference between ids and classes is that, with the latter, you can target multiple elements. Use classes when you want your styling to apply to a group of elements. Alternatively, use ids to find a needle-in-a-haystack, and style only that specific element.

---
