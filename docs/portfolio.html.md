# Documentation: portfolio.html

## Overview
Portfolio showcase with project cards, statistics section, and call-to-action.

## HTML Structure

### Inline Background Gradients
```html
<div class="portfolio-image" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">
```
**Why inline styles here:**
- Each project has unique gradient
- More maintainable than creating separate classes

### Overlay Pattern
```html
<div class="portfolio-overlay">
    <h3>E-Commerce Platform</h3>
```
**Purpose:** Overlay sits on top of gradient background, revealed on hover.

### Tech Stack List
```html
<ul class="tech-stack">
    <li>HTML5</li>
    <li>CSS3</li>
```
**Semantic choice:** List is appropriate for collection of related items.
**CSS styling:** Renders as horizontal pill-shaped badges.

## JavaScript
Only dynamic year update; stat counters could be animated with additional JS.
