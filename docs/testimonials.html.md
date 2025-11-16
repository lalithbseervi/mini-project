# Documentation: testimonials.html

## Overview
Client testimonials with avatar placeholders, ratings, and trusted client logos.

## HTML Structure

### Star Ratings
```html
<div class="testimonial-rating">⭐⭐⭐⭐⭐</div>
```
**Unicode stars:** Simple, accessible alternative to icon fonts or images.
**Enhancement opportunity:** Could use semantic rating markup for SEO.

### Avatar Placeholders
```html
<div class="author-avatar" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">RK</div>
```
**Why gradients + initials:**
- Placeholder for real images
- Colorful and visually interesting
- Each testimonial gets unique gradient
**Accessibility:** Initials provide text content for screen readers

### Client Logos
```html
<div class="client-logo">FashionHub</div>
```
**Text-based logos:** Placeholders for actual logo images. Easy to replace with `<img>` tags later.

## CSS Tricks
- Circular avatars: `border-radius: 50%` on fixed width/height
- Flexbox centering in avatars: `display: flex; align-items: center; justify-content: center`

## JavaScript
Dynamic year update in footer.
