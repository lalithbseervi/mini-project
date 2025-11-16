# Documentation: testimonials.css

## Overview
Styles for testimonial cards, author avatars, and client logos.

## Testimonial Cards

### Grid Layout
```css
.testimonial-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
}
```
**Consistent pattern:** Same layout approach as other pages
**Flexibility:** Handles 1, 2, or 3 columns based on screen width

### Card Hover
```css
.testimonial-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(74, 107, 255, 0.15);
}
```
**Moderate lift:** 5px (less than services, more than add-ons)
**Larger shadow:** `25px` blur creates substantial depth
**Interactive feedback:** Shows content is readable/clickable

## Testimonial Content

### Italic Text
```css
.testimonial-text {
    font-style: italic;
}
```
**Convention:** Italics indicate quoted/spoken text
**Visual differentiation:** Separates testimonial from surrounding content

### Line Height
```css
line-height: 1.7;
```
**Readable paragraphs:** More spacing than headlines (1.2)
**Why 1.7:** Sweet spot for readability in body text
**Less than:** Standard 1.5 feels cramped
**More than:** 1.8-2.0 feels too loose

## Author Section

### Avatar Layout
```css
.testimonial-author {
    display: flex;
    align-items: center;
    gap: 15px;
}
```
**Horizontal layout:** Avatar next to name
**`align-items: center`:** Vertically centers avatar with text
**`gap: 15px`:** Spacing between avatar and text

### Circular Avatar
```css
.author-avatar {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}
```
**`border-radius: 50%`:** Makes square element circular
**Why 50%:** Half of width/height creates perfect circle
**Fixed dimensions:** Equal width and height required for circle
**Flex centering:** Centers initials within circle
**Background set inline:** Each avatar has unique gradient (in HTML)

### Author Info
```css
.author-info h4 {
    margin: 0;
}
.author-info p {
    margin: 5px 0 0 0;
}
```
**Tight margins:** Keeps name and title close together
**`margin: 0` on h4:** Removes default heading margins
**Small top margin on p:** Slight separation between name and title

## Client Logos

### Logo Cards
```css
.client-logo {
    background: #ffffff;
    padding: 20px 30px;
    font-weight: bold;
    transition: background-color 0.3s, color 0.3s, border-color 0.3s;
}
```
**Horizontal padding:** `30px` creates rectangular "buttons"
**Bold text:** Makes placeholder names stand out
**Multiple transitions:** Smooth color changes on hover

### Hover Effect
```css
.client-logo:hover {
    background-color: #4a6bff;
    color: white;
    border-color: #4a6bff;
}
```
**Color inversion:** White → blue background, dark → white text
**Brand consistency:** Uses signature blue
**Interactive:** Suggests logos could be clickable links (even if static)
