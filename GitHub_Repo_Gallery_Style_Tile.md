# GitHub Repo Gallery: Style Tile

A quick-reference guide to the colors, type, and reusable UI patterns already established in this project's HTML and CSS. Use this to keep new sections consistent with what's already built, and share it with Claude when prompting for new components.

---

## Color Palette

| Swatch | Name | Hex | Used For |
| :---- | :---- | :---- | :---- |
| 🟪 | Deep Purple | `#483978` | Page title banner background, profile section background, primary button fill, small accent circle in the top corner tab |
| 🟪 | Deep Purple (hover) | `#2f2550` | Primary button hover state |
| 🟪 | Soft Lavender | `#9b8dc9` | Divider line under profile stats |
| 🟪 | Pale Lavender | `#eee9ff` | Repo card title hover background |
| 🟧 | Coral | `#f86d58` | GitHub icon color, repo card border, repo card title text |
| 🟨 | Pale Yellow | `#fbf9de` | Page background |
| ⬜ | White | `#fff` | Card and section backgrounds, button text |
| ⬛ | Body Text | `#333` | Default body text |
| ⬜ | Neutral Grey | `grey` | Decorative corner tab background |
| ⬜ | Border Grey | `#ccc` | Primary button hover border |

---

## Typography

**Headings:** Oswald, weight 500, uppercase
**Body copy:** Open Sans, weights 400 (regular) and 700 (bold)
**Base font size:** `16px`

| Element | Font | Size | Notes |
| :---- | :---- | :---- | :---- |
| Page title (h1) | Oswald, 500 | `56px` | Uppercase, centered, white text on purple; padding of `16px` top/bottom and `8px` left/right |
| Repo card title (h3) | Oswald, 500 | default | Coral, left-aligned in cards |
| Body text | Open Sans, 400 | `16px` | Default color `#333` |
| Profile section text | Open Sans | `18px` | White text on purple background |

Fonts are loaded from Google Fonts:
```
Open Sans: wght@400;700
Oswald: wght@500
```

Icons come from Font Awesome Pro 5.10.0 (e.g. `fa-github-alt`).

*Pixel values above are given as a designer would hand them off. It's on you to decide how to translate them into responsive units (px, %, em, rem) when you build.*

---

## Core UI Components

### Badge + Circle
A small decorative tab that sits above the page header.

```css
.badge {
    height: 80px;
    width: 50px;
    background-color: grey;
    z-index: 98;
    margin-bottom: -35px;
    margin-top: 10px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
}

.circle {
    width: 20px;
    height: 20px;
    background-color: #483978;
    border-radius: 100%;
    z-index: 99;
    align-self: center;
    margin-top: auto;
    margin-bottom: 8px;
}
```
**Markup:**
```html
<div class="badge">
    <div class="circle"></div>
</div>
```

---

### Breakpoints

| Breakpoint | Behavior |
| :---- | :---- |
| Default (mobile) | Single-column stacking; repo cards full width |
| `min-width: 700px` | Profile section items go to `45%` width, text left-aligns; repo cards go to `48%` width, space-between |
| `max-width: 700px` | Profile section paragraph gets extra margin |
| `min-width: 1200px` | Repo cards narrow to `30%` width (three-up grid) |
