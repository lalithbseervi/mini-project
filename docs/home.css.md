# Documentation: home.css

## Overview
Styles specific to the homepage hero section.

## Video play on loading the page
**References:**
- [w3schools](https://www.w3schools.com/howto/howto_css_fullscreen_video.asp)

## Hero Section

### Layout
```css
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}
```
**`min-height: 100vh`:** Full viewport height (100% of screen)
**`display: flex` with centering:** 
- `align-items: center` → vertical centering
- `justify-content: center` → horizontal centering
**Result:** Content perfectly centered on screen

**References:**
- [MDN: min-height](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height)
- [Stack Overflow: How to center vertically and horizontally with flexbox?](https://stackoverflow.com/questions/19461521/how-to-center-an-element-horizontally-and-vertically)

### Background Effect
```css
background: radial-gradient(circle at 50% 50%, rgba(74, 107, 255, 0.08) 0%, transparent 50%);
```
**Radial vs Linear:**
- Radiates from center point outward
- Creates spotlight/glow effect
**`circle at 50% 50%`:** Center of element (horizontal, vertical)
**`rgba(74, 107, 255, 0.08)`:** Very subtle blue (8% opacity)
**`transparent 50%`:** Fades to transparent at 50% radius
**Visual effect:** Soft blue glow behind hero content without overwhelming text

**References:**
- [MDN: radial-gradient()](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/radial-gradient)
- [MDN: CSS Gradients](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_images/Using_CSS_gradients)

### Typography
```css
.hero-title {
    font-size: 48px;
    line-height: 1.2;
}
```
**`line-height: 1.2`:** 
- Tight spacing for headlines (1.2 × font-size)
- Default is typically 1.5
- Tighter feels more impactful, less reading-focused

**References:**
- [MDN: line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
- [MDN: font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)

### Highlight Color
```css
.highlight {
    color: #4a6bff;
}
```
**Purpose:** Makes key phrase stand out in title
**Consistent branding:** Uses same blue throughout site
