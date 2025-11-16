# Documentation: policy.css

## Overview
Styles for Privacy Policy and Terms of Service pages.

## Policy Content Container

```css
.policy-content {
    background: #ffffff;
    border: 2px solid #e0e6ed;
    border-radius: 12px;
    padding: 28px;
    line-height: 1.9;
}
```
**White background:** Improves readability of dense text
**Border:** Defines content area clearly
**`line-height: 1.9`:** Spacing for comfortable reading of legal text
**Why 1.9:** Legal/policy documents benefit from extra spacing

## Typography Hierarchy

### H2 Headings
```css
.policy-content h2 {
    font-size: 22px;
    margin-top: 24px;
    margin-bottom: 10px;
}
```
**Top margin > bottom margin:** Creates space between sections
**Pattern:** `margin-top: 24px` groups heading with previous section
**`margin-bottom: 10px`:** Brings heading close to its content

### H3 Subheadings
```css
.policy-content h3 {
    font-size: 18px;
    margin-top: 16px;
    margin-bottom: 8px;
}
```
**Smaller margins:** H3 is sub-section, needs less separation
**Size hierarchy:** H2 (22px) > H3 (18px) > body (15px)

## Lists

```css
.policy-content ul,
.policy-content ol {
    padding-left: 20px;
    margin: 10px 0;
}
```
**`padding-left: 20px`:** Indents list from parent
**Consistent margins:** Separates lists from surrounding paragraphs
**Why padding not margin:** Browser default list markers sit in padding area

### List Items
```css
.policy-content li {
    margin: 6px 0;
}
```
**Vertical spacing:** Prevents list items from cramming together
**Small margin:** Enough for breathing room, not too much separation

## Acknowledgment Box

```css
.policy-acknowledgment {
    margin-top: 20px;
    padding: 16px;
    background: rgba(74, 107, 255, 0.08);
    border: 1px solid rgba(74, 107, 255, 0.2);
    border-radius: 8px;
}
```
**Colored background:** Draws attention to important legal clause
**Semi-transparent:** `rgba(..., 0.08)` = 8% opacity
**Matching border:** `rgba(..., 0.2)` = 20% opacity for subtle edge
**Purpose:** Visually emphasizes user agreement section
**Psychology:** Light blue = professional, trustworthy (not alarming red)

## Design Rationale

**Readability focus:**
- White background reduces eye strain
- Large line-height (1.9) for dense text
- Clear heading hierarchy
- Ample padding and margins

**Legal document best practices:**
- Numbered headings for reference
- Indented lists for sub-points
- Highlighted acknowledgment section
- Consistent spacing throughout
