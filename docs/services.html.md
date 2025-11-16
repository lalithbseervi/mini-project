# Documentation: services.html

## Overview
Services page showcasing pricing tiers, feature comparison table, and add-on services.

## HTML Structure

### Featured Service Card
```html
<div class="service-card featured">
    <div class="badge">POPULAR</div>
```
**Purpose:** Visually distinguishes recommended service tier using CSS modifiers.

### Feature List
```html
<ul class="feature-list">
    <li>Up to 5 pages</li>
```
**CSS Styling:** Uses `::before` pseudo-element to add checkmark icons without cluttering HTML.

### Checkmarks & X marks
```html
<td>✓</td>
<td>✗</td>
```
**Unicode symbols:** Simple, no images required, scalable, and accessible.

## CSS Tricks (referenced)
- `.featured` class adds special border and gradient background
- `.badge` uses `position: absolute` for overlay effect
- Table uses `border-collapse: collapse` to remove gaps between cells

## JavaScript
Dynamic year update in footer.
