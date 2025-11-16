# Documentation: contact.html

## Overview
Contact page with form submission, contact information cards, map integration, and social media links.

## HTML Structure

### Form Method
```html
<form action="form_response.html" method="get">
```
**Why GET instead of POST?**
- GET appends form data to URL as query parameters
- Allows form_response.html to read data via JavaScript
- **Note:** In production, use POST for privacy and security

### Form Elements

#### Required Fields
```html
<input type="text" id="name" name="name" required>
```
**Why `required` attribute:**
- HTML5 native validation prevents empty submission
- Browser shows validation message automatically
- No JavaScript needed for basic validation

#### Select Dropdown
```html
<option value="">Select a service</option>
```
**Why empty first option:** Acts as placeholder; forces user selection before submission.

### Google Maps Embed
```html
<iframe src="..." loading="lazy" title="Office Location Map">
```
**`loading="lazy"`:** Defers iframe loading until user scrolls near it, improving page load speed.
**`title` attribute:** Accessibility feature for screen readers.

## JavaScript

### Dynamic Year (same as index.html)
Updates footer copyright year automatically.
