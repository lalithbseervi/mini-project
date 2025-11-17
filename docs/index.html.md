# Documentation: index.html

## Overview
Homepage featuring a hero section with call-to-action buttons.

## HTML Structure

### Header Navigation
- Fixed header with flexbox layout (`display: flex`)
- Logo with inline styles for link appearance
- Navigation links with hover states

### Hero Section
```html
<span class="highlight">You Imagine It</span>
```
**Purpose:** Highlights key text using CSS styling for visual emphasis.

### Footer
```html
<span id="year"></span>
```
**Why:** Dynamic year insertion prevents manual updates annually.

## JavaScript

### Dynamic Year
```javascript
document.getElementById('year').innerHTML = new Date().getFullYear();
```
**Explanation:** 
- `new Date()` creates current date object
- `.getFullYear()` extracts current year (e.g., 2025)
- `.innerHTML` updates DOM element content

**Benefits:** Automatically updates copyright year without manual edits.

**References:**
- [MDN: Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)
- [MDN: Date.getFullYear()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getFullYear)
- [MDN: Element.innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)
- [MDN: Document.getElementById()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)
