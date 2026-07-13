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

## Content Reference (Copy-Paste Placeholders)

This project pulls all of its content live from the GitHub API rather than typing it into the HTML by hand. Since you won't wire up any JavaScript yet, use the text below as placeholder content so your shell already reads like the finished page once the data is fetched in.

### Profile Section

| Label | Sample Data |
| :---- | :---- |
| Avatar | Included in img directory of style assets |
| Name | Tauri StClaire |
| Bio | Hello! I am a responsive coder who loves Javascript React! HTML5 CSS3 FTP Web Hosting Git Version Control JSX ES6 |
| Location | San Diego, California |
| Number of public repos | 118 |

### Repo Gallery List (card titles only)

- gen-ai-recipe-chatbot
- 105-turn_back_time-2
- wordpress-nutrition-blog
- national-park-tour-planner
- study-buddy-with-ui
- study-buddy

### Repo Detail View (shown after a card is clicked)

Clicking a card swaps the gallery for a detail view with its own labeled data. Two real examples, so you can see the pattern before you build it:

**Example 1**

| Label | Sample Data |
| :---- | :---- |
| Name | gen-ai-recipe-chatbot |
| Description | ChefBoost Gen AI app made with LangChain, Supabase, and pgvector |
| Default Branch | main |
| Languages | Python, JavaScript, CSS, HTML, PLpgSQL |
| Link text | View Repo on GitHub! |

**Example 2**

| Label | Sample Data |
| :---- | :---- |
| Name | national-park-tour-planner |
| Description | An app that allows you to plan trips to national parks using LangChain and Wikipedia and National Parks APIs! |
| Default Branch | main |
| Languages | HTML, CSS, Python, JavaScript |
| Link text | View Repo on GitHub! |

### Other Static UI Text

- Page title: GitHub Repo Gallery
- Search input placeholder: Search by name
- Back button text: Back to Repo Gallery

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

| Breakpoint | Device |
| :---- | :---- |
| Default | Mobile
| `min-width: 700px` | Tablet
| `min-width: 1200px` | Desktop
