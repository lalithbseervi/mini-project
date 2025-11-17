# Documentation: faq.css

## Overview
Styles for accordion-style FAQ with expandable/collapsible answers.

## FAQ Container

```css
.faq-container {
    max-width: 900px;
    margin: 0 auto;
}
```
**Narrower than page:** FAQs read better in constrained width
**Center alignment:** `margin: 0 auto` centers container
**Optimal reading:** 900px prevents overly long lines

## FAQ Category Headers

```css
.faq-category {
    font-size: 24px;
    color: #4a6bff;
}
```
**Brand color:** Distinguishes section headers from questions
**Larger than questions:** Visual hierarchy (24px vs 16px)

## FAQ Items

### Base Styling
```css
.faq-item {
    background: #ffffff;
    overflow: hidden;
    transition: box-shadow 0.3s, border-color 0.3s;
}
```
**`overflow: hidden`:** Critical for answer animation (prevents content overflow during transition)
**Transitions:** Smooth hover effects

### Question Section
```css
.faq-question {
    padding: 20px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
}
```
**`cursor: pointer`:** Indicates clickability
**Flexbox layout:** Question text left, icon right
**`justify-content: space-between`:** Maximum separation between text and icon

### Interactive Feedback
```css
.faq-question:hover {
    background-color: #f7fafc;
}
```
**Subtle background:** Slight gray on hover
**UX improvement:** Shows element is interactive before clicking

## Answer Animation

### Collapsed State
```css
.faq-answer {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s;
    padding: 0 20px;
}
```
**`max-height: 0`:** Hides content
**`overflow: hidden`:** Prevents content from showing outside collapsed area
**`transition: max-height`:** Animates expansion
**Why max-height not height:** Can't transition to `height: auto`

### Expanded State
```css
.faq-item.active .faq-answer {
    max-height: 1000px;
    padding: 0 20px 20px 20px;
}
```
**`.active` class:** Applied via JavaScript
**`max-height: 1000px`:** Large enough for longest answer
**Padding change:** Adds bottom padding in expanded state
**Animation:** Transitions from 0 to 1000px smoothly

### Why This Technique?
- `display: none` → Cannot be animated
- `height: 0` → `height: auto` → Cannot transition to `auto`
- `max-height: 0` → `max-height: 1000px` → Works!
**Tradeoff:** Transition speed varies with content length (longer content = slower)

**References:**
- [MDN: max-height](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height)
- [Stack Overflow: Transition height: 0 to height: auto using CSS?](https://stackoverflow.com/questions/3508605/how-can-i-transition-height-0-to-height-auto-using-css)
- [Stack Overflow: Smooth accordion animation with max-height](https://stackoverflow.com/questions/23450158/css-transition-height-0-to-height-auto)

## FAQ Icon

```css
.faq-icon {
    font-size: 24px;
    color: #4a6bff;
    font-weight: bold;
}
```
**Large size:** Easy click target
**Brand color:** Consistent with design
**Changed by JavaScript:** `+` → `−` when expanded

## Answer Content

```css
.faq-answer ul,
.faq-answer ol {
    line-height: 1.9;
    padding-left: 20px;
}
```
**Generous line-height:** Easy reading for longer content
**Proper indentation:** Lists visually nested under questions

### Links
```css
.faq-answer a {
    color: #4a6bff;
    text-decoration: none;
}
.faq-answer a:hover {
    text-decoration: underline;
}
```
**Underline on hover only:** Cleaner appearance, still accessible
**Brand color:** Distinguishes links from body text

**References:**
- [MDN: :hover](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover)
- [MDN: text-decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
