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

**References:**
- [MDN: box-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)
- [MDN: Universal selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)

### Body Background
```css
background: linear-gradient(135deg, #f5f7fa 0%, #e8ecf1 50%, #dce3eb 100%);
```
**135deg:** Diagonal gradient from top-left to bottom-right
**Why 3 stops:** Creates subtle color transition across page
**min-height: 100vh:** Ensures gradient covers full viewport height

**References:**
- [MDN: linear-gradient()](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient)
- [MDN: Viewport units (vh)](https://developer.mozilla.org/en-US/docs/Web/CSS/length#vh)

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

**References:**
- [MDN: margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
- [Stack Overflow: How to horizontally center a div?](https://stackoverflow.com/questions/114543/how-to-horizontally-center-a-div)

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

**References:**
- [MDN: position](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
- [MDN: z-index](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)

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

**References:**
- [MDN: Flexbox (CSS Flexible Box Layout)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
- [MDN: justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)
- [MDN: align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)

### Navigation Links
```css
.nav-link {
    transition: background-color 0.3s, border-color 0.3s, color 0.3s;
}
```
**Why 0.3s:** Smooth but quick transition, feels responsive
**Multiple properties:** All visual changes animate simultaneously

**References:**
- [MDN: transition](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)
- [MDN: Using CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transitions/Using_CSS_transitions)

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

**References:**
- [MDN: box-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)

### Hover Transform
```css
.btn:hover {
    transform: translateY(-2px);
}
```
**`translateY(-2px)`:** Lifts button up by 2 pixels

**References:**
- [MDN: transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
- [MDN: translate()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate)

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

**References:**
- [MDN: Class selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors)
- [Stack Overflow: What does a space mean in a CSS selector?](https://stackoverflow.com/questions/7002023/what-does-a-space-mean-in-a-css-selector-i-e-what-is-the-difference-between)

## CTA Section

```css
.cta-section {
    background: linear-gradient(135deg, rgba(74, 107, 255, 0.08) 0%, #ffffff 100%);
}
```
**`rgba(74, 107, 255, 0.08)`:** Very subtle blue tint (8% opacity)
**Fades to white:** Creates soft, engaging background without overwhelming content
