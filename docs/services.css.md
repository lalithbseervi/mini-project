# Documentation: services.css

## Overview
Styles for service cards, pricing tiers, comparison tables, and add-ons.

## Service Cards

### Grid Layout
```css
.services-grid {
    display: flex;
    gap: 30px;
    flex-wrap: wrap;
    justify-content: center;
}
```
**Flex over Grid:** More flexible wrapping behavior for varied screen sizes
**`justify-content: center`:** Cards center when row isn't full
b
**References:**
- [MDN: flex-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)
- [MDN: gap](https://developer.mozilla.org/en-US/docs/Web/CSS/gap)
- [Stack Overflow: When to use flexbox vs CSS Grid?](https://stackoverflow.com/questions/45536537/when-to-use-css-grid-layout-vs-flexbox)

### Card Sizing
```css
.service-card {
    width: 320px;
}
```
**Fixed width:** Maintains consistent card sizes regardless of content

### Hover Transform
```css
.service-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 30px rgba(74, 107, 255, 0.15);
}
```
**`translateY(-10px)`:** More pronounced lift than buttons (draws attention to pricing)
**Shadow follows movement:** Larger shadow reinforces floating effect

### Featured Card
```css
.service-card.featured {
    border: 3px solid #4a6bff;
    background: linear-gradient(135deg, rgba(74, 107, 255, 0.05) 0%, #ffffff 100%);
}
```
**Thicker border:** 3px vs 2px makes it stand out
**Subtle gradient:** Very light blue tint (5% opacity) → white
**Purpose:** Visually highlights recommended plan

### Badge Positioning
```css
.badge {
    position: absolute;
    top: -15px;
    right: 20px;
}
```
**`position: absolute`:** Removes from document flow
**Negative top:** `-15px` places badge half outside card edge
**Why this works:** Parent `.service-card` has default `position: relative`
**Visual effect:** Badge appears to "float" above card

**References:**
- [MDN: position (absolute)](https://developer.mozilla.org/en-US/docs/Web/CSS/position#absolute)
- [Stack Overflow: What is the difference between position: absolute and position: relative?](https://stackoverflow.com/questions/10426497/what-is-the-difference-between-position-absolute-and-position-relative)

## Feature List

### Custom Checkmarks
```css
.feature-list li:before {
    content: "✓";
    position: absolute;
    left: 0;
    color: #4a6bff;
}
```
**`::before` pseudo-element:** Adds content via CSS
**`position: absolute`:** Positions checkmark independently
**Why not list-style:** More control over appearance and color
**`left: 0`:** Aligns with `padding-left: 25px` on `li`

**References:**
- [MDN: ::before](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
- [MDN: content](https://developer.mozilla.org/en-US/docs/Web/CSS/content)

## Comparison Table

### Table Styling
```css
.comparison-table {
    border-collapse: collapse;
    overflow: hidden;
}
```
**`border-collapse: collapse`:** Removes gaps between table cells
**`overflow: hidden`:** Clips content to rounded corners (on container)

**References:**
- [MDN: border-collapse](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
- [MDN: overflow](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)

### Header Gradient
```css
.comparison-table th {
    background: linear-gradient(135deg, #4a6bff 0%, #3a5bef 100%);
    color: white;
}
```
**Why gradient on headers:** Adds visual interest to otherwise plain table
**White text:** Ensures readability on dark blue background

### Row Hover
```css
.comparison-table tr:hover {
    background-color: #f7fafc;
}
```
**Purpose:** Helps users track rows across wide tables
**Subtle color:** Light gray doesn't distract

### Scrollable Container
```css
.table-container {
    overflow-x: auto;
}
```
**Mobile-friendly:** Allows horizontal scrolling on narrow screens
**Better than:** Shrinking text to fit (which becomes unreadable)

## Add-on Cards

### Hover Lift
```css
.addon-card:hover {
    transform: translateY(-5px);
}
```
**Moderate lift:** More than text link, less than main service cards
**Hierarchy:** Main services = 10px, add-ons = 5px, links/buttons = 2-3px
