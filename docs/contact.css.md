# Documentation: contact.css

## Overview
Styles for contact form, info cards, and map.

## Contact Layout

### Two-Column Layout
```css
.contact-container {
    display: flex;
    gap: 40px;
    flex-wrap: wrap;
    justify-content: center;
}
```
**`flex-wrap: wrap`:** Columns stack on narrow screens automatically
**`gap: 40px`:** Modern property for spacing between flex items (replaces margin hacks)
**`justify-content: center`:** Centers items when wrapping occurs

### Flex Item Sizing
```css
.contact-form-section, .contact-info-section {
    flex: 1 1 420px;
    max-width: 520px;
}
```
**`flex: 1 1 420px`** breakdown:
- First `1`: flex-grow (can expand)
- Second `1`: flex-shrink (can shrink)
- `420px`: flex-basis (starting width)
**Result:** Columns equal width, wrap below 420px, never exceed 520px

**References:**
- [MDN: flex](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)
- [MDN: flex-basis](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-basis)
- [Stack Overflow: What are flex-grow, flex-shrink and flex-basis?](https://stackoverflow.com/questions/28542031/what-are-the-differences-between-flex-basis-and-width)

## Form Styles

### Input Focus States
```css
.form-group input:focus {
    outline: none;
    border-color: #4a6bff;
    background-color: #ffffff;
}
```
**`outline: none`:** Removes default browser outline
**Background change:** `#f8fafc` → `#ffffff` provides subtle visual feedback

**References:**
- [MDN: :focus](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [MDN: outline](https://developer.mozilla.org/en-US/docs/Web/CSS/outline)
- [Stack Overflow: How to remove outline around input elements?](https://stackoverflow.com/questions/1457849/how-to-remove-the-border-highlight-on-an-input-text-element)

### Transitions
```css
transition: border-color 0.3s, background-color 0.3s;
```
**Smooth interactions:** Prevents sudden color changes
**Performance:** Only animating colors (not layout properties)

### Checkbox Special Case
```css
.form-group input[type="checkbox"] {
    width: auto;
    margin-right: 8px;
}
```
**`width: auto`:** Overrides `width: 100%` from general input styling
**Why needed:** Full-width checkboxes look bad

**References:**
- [MDN: Attribute selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors)
- [MDN: width](https://developer.mozilla.org/en-US/docs/Web/CSS/width)

## Info Cards

### Hover Effects
```css
.contact-info-card:hover {
    box-shadow: 0 6px 18px rgba(74, 107, 255, 0.12);
    border-color: #4a6bff;
}
```
**Subtle interaction:** Cards "activate" on hover
**Shadow parameters:**
- `0`: No horizontal offset
- `6px`: Downward offset (floating effect)
- `18px`: Blur radius (soft shadow)
- `0.12` opacity: Very subtle

## Map Section

### Container Styling
```css
.map-container {
    border-radius: 12px;
    box-shadow: 0 4px 18px rgba(0,0,0,0.08);
}
```
**Rounded corners:** Softens harsh rectangular iframe
**Shadow:** Creates depth, makes map appear elevated
