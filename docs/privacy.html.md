# Documentation: privacy.html

## Overview
Privacy policy page with dynamic date formatting.

## HTML Structure

### Dynamic Date Placeholder
```html
<p class="page-subtitle">Last Updated: <span id="lastUpdated"></span></p>
```
**Purpose:** Displays formatted date, populated by JavaScript.

### Structured Content
- Numbered headings (h2) for major sections
- Sub-headings (h3) for subsections
- Bullet lists for easy scanning

### Acknowledgment Box
```html
<div class="policy-acknowledgment">
    <p><strong>By using our website...</strong></p>
```
**Purpose:** Visually emphasizes legal acceptance clause.

## JavaScript

### Date Formatting
```javascript
var currentDate = new Date();
var months = ['January', 'February', ...];
var formattedDate = months[currentDate.getMonth()] + ' ' + currentDate.getDate() + ', ' + currentDate.getFullYear();
```

**Why manual formatting?**
- `.getMonth()` returns 0-11, needs month name array
- `.toLocaleDateString()` alternative exists but gives less control
- Creates format: "November 16, 2025"

**Array indexing:** `months[currentDate.getMonth()]` maps numeric month (0-11) to name.

**String concatenation:** Builds formatted string like "November 16, 2025".
