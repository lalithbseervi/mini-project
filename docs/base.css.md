# Documentation: base.css

## Overview
Core stylesheet providing global styles, header, footer, buttons, and page layout foundation.

## Global Styles

### Universal Reset
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
**Why `box-sizing: border-box`:**
- Makes width/height include padding and border
- Default `content-box` only counts content
- **Example:** `width: 100px; padding: 10px` → total width stays 100px (not 120px)
- Essential for predictable layouts

### Body Background
```css
background: linear-gradient(135deg, #f5f7fa 0%, #e8ecf1 50%, #dce3eb 100%);
```
**135deg:** Diagonal gradient from top-left to bottom-right
**Why 3 stops:** Creates subtle color transition across page
**min-height: 100vh:** Ensures gradient covers full viewport height

## Container

```css
.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}
```
**`margin: 0 auto`:** Centers container horizontally
**90% width:** Responsive spacing on small screens
**max-width: 1200px:** Prevents excessive stretching on large monitors

## Header

### Fixed Positioning
```css
.header {
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 100;
}
```
**`position: fixed`:** Keeps header visible while scrolling
**`z-index: 100`:** Ensures header stays above page content
**`width: 100%`:** Stretches across full viewport width

### Header Layout
```css
.header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```
**Flexbox advantages:**
- `space-between`: Logo left, nav right
- `align-items: center`: Vertically centers items
- Simple, responsive solution

### Navigation Links
```css
.nav-link {
    transition: background-color 0.3s, border-color 0.3s, color 0.3s;
}
```
**Why 0.3s:** Smooth but quick transition, feels responsive
**Multiple properties:** All visual changes animate simultaneously

## Buttons

### Primary Button
```css
.btn-primary {
    background: linear-gradient(135deg, #4a6bff 0%, #3a5bef 100%);
    box-shadow: 0 6px 18px rgba(74, 107, 255, 0.3);
}
```
**Gradient benefits:**
- More depth than flat color
- Modern, professional appearance
**Box-shadow:**
- `0 6px` → 6px downward (no horizontal offset)
- `18px` → blur radius
- `rgba(74, 107, 255, 0.3)` → semi-transparent shadow matching button color

### Hover Transform
```css
.btn:hover {
    transform: translateY(-2px);
}
```
**`translateY(-2px)`:** Lifts button up by 2 pixels

## Footer

```css
.footer {
    margin-top: 60px;
    background-color: #ffffff;
}
```
**`margin-top: 60px`:** Pushes footer away from content
**Alternative approach:** Could use flexbox on body with `margin-top: auto` on footer

## Page Content

```css
.page-content {
    padding-top: 100px;
}
```
**Why 100px:** Accounts for fixed header height (~80px) + spacing
**Without this:** Content would hide behind fixed header

## Active Navigation State

```css
.nav-link.active {
    background-color: #4a6bff;
    color: white;
}
```
**Class chaining:** `.nav-link.active` requires both classes
**Purpose:** Highlights current page in navigation

## CTA Section

```css
.cta-section {
    background: linear-gradient(135deg, rgba(74, 107, 255, 0.08) 0%, #ffffff 100%);
}
```
**`rgba(74, 107, 255, 0.08)`:** Very subtle blue tint (8% opacity)
**Fades to white:** Creates soft, engaging background without overwhelming content
