# Documentation: portfolio.css

## Overview
Styles for portfolio project cards, gradient overlays, tech stacks, and statistics.

## Portfolio Grid

```css
.portfolio-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
}
```
**Similar to services grid:** Flex-based responsive layout
**Centers content:** Works well with varying number of items per row

## Portfolio Cards

### Card Sizing
```css
.portfolio-item {
    width: 350px;
    overflow: hidden;
}
```
**Fixed width:** Maintains consistency
**`overflow: hidden`:** Clips content to rounded borders
**Critical for:** Ensures image gradients respect `border-radius`

### Image Section Height
```css
.portfolio-image {
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
}
```
**Fixed height:** All portfolio previews same size
**Flexbox centering:** Centers overlay text within gradient background
**Background set inline:** Each project has unique gradient (in HTML)

### Overlay Effect
```css
.portfolio-overlay {
    text-align: center;
    padding: 20px;
}
```
**Purpose:** Text layer on top of gradient background

## Tech Stack Badges

```css
.tech-stack {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}
```
**Horizontal list:** Flex makes list items flow in row
**`flex-wrap: wrap`:** Badges wrap to next line if needed
**`gap: 10px`:** Consistent spacing between badges

### Badge Styling
```css
.tech-stack li {
    background: rgba(74, 107, 255, 0.1);
    padding: 5px 12px;
    border-radius: 15px;
    border: 1px solid rgba(74, 107, 255, 0.2);
}
```
**Pill shape:** `border-radius: 15px` with horizontal padding
**Translucent background:** `rgba(..., 0.1)` = 10% opacity blue
**Border transparency:** `rgba(..., 0.2)` = 20% opacity for subtle definition
**Why semi-transparent:** Maintains visual connection to overall design while being distinct

## Statistics Section

### Stat Cards
```css
.stat-card {
    width: 200px;
    text-align: center;
}
```
**Fixed width:** Keeps cards uniform
**Center alignment:** Numbers and labels both centered

### Hover Scale
```css
.stat-card:hover {
    transform: scale(1.05);
}
```
**`scale(1.05)`:** Enlarges element by 5% in all directions
**Different from translateY:** Grows rather than lifts
**Visual effect:** Number "pops" when hovered, drawing attention

### Large Numbers
```css
.stat-number {
    font-size: 48px;
    font-weight: bold;
    color: #4a6bff;
}
```
**48px:** Very large for emphasis
**Brand color:** Consistent blue theme
**Bold weight:** Increases visual impact