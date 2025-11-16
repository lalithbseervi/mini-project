# Documentation: faq.html

## Overview
Accordion-style FAQ section with expandable/collapsible answers.

## HTML Structure

### FAQ Item Structure
```html
<div class="faq-item">
    <div class="faq-question" onclick="toggleFaq(this)">
```
**Inline onclick:** Directly binds click handler. Alternative: addEventListener in separate JS.

### FAQ Icon
```html
<span class="faq-icon">+</span>
```
**Changes to:** `−` (minus) when expanded via JavaScript.

### FAQ Answer Container
```html
<div class="faq-answer">
```
**Default state:** `max-height: 0` and `overflow: hidden` (CSS)
**Expanded state:** `.active` class adds `max-height: 1000px`

## JavaScript

### Toggle Function
```javascript
function toggleFaq(element) {
    var faqItem = element.parentElement;
```
**`parentElement`:** Traverses DOM to get container div from clicked question.

### Close Other FAQs
```javascript
var allFaqs = document.querySelectorAll('.faq-item');
for (var i = 0; i < allFaqs.length; i++) {
    if (allFaqs[i] !== faqItem && allFaqs[i].classList.contains('active')) {
        allFaqs[i].classList.remove('active');
```
**Purpose:** Implements accordion behavior - only one FAQ open at a time.
**Why loop instead of forEach?** Broader browser compatibility.

### Toggle Current FAQ
```javascript
if (faqItem.classList.contains('active')) {
    faqItem.classList.remove('active');
    icon.innerHTML = '+';
} else {
    faqItem.classList.add('active');
    icon.innerHTML = '−';
}
```
**Conditional logic:** Checks current state and toggles accordingly.
**Character note:** `−` is minus sign (U+2212), different from hyphen `-`.

### Why Not `display: none`?
Using `max-height` with `transition` creates smooth animation. `display: none` cannot be animated.
