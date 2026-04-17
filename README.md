# mtm6201-final
final assignment
# Love Vegan – MTM6201 Final Project
 
A three-page responsive website for a plant-based restaurant, built with the **Bootstrap 5** framework and hosted on GitHub Pages.
 
 

 
## 🔧 Process
 
### Design
I started with Figma wireframes and mockups for all three screen sizes (mobile, tablet, desktop). The design uses an organic, natural aesthetic with earthy greens, warm tans, and script typography to reinforce the plant-based brand identity.
 
### Development
1. Set up the Bootstrap 5 grid as the structural foundation.
2. Overrode Bootstrap's default CSS custom properties (variables) to match the brand palette — no !important overuse, just clean variable replacement.
3. Built each page as a separate HTML file sharing one `css/styles.css` and one `js/main.js`.
4. Implemented responsive images using `<picture>` + `srcset` with two sizes for every food photo.
5. Added a hamburger menu (Bootstrap's built-in `navbar-toggler`) for mobile navigation.
6. Added image zoom-on-click overlay with keyboard support (Escape to close, focus management).
7. Accessibility pass: skip link, semantic HTML (`<header>`, `<nav>`, `<main>`, `<footer>`, `<article>`, `<section>`), ARIA labels, alt text on all images, logical heading order.
### Challenges
 
**1. Bootstrap colour overrides**  
Bootstrap 5 uses CSS custom properties extensively, which made overriding the colour scheme clean — but some components (buttons, form controls) also inherit from compiled Sass variables. I solved this by targeting the specific component classes directly in `styles.css` rather than fighting the cascade.
 
**2. Responsive images**  
Using `<picture>` + `srcset` for every image added markup, but was necessary to serve appropriately sized images on mobile vs desktop. I settled on two breakpoints (576px and 768px) with small and large Unsplash URLs.
 
**3. Navbar on dark background**  
Bootstrap's default hamburger icon is dark-coloured and invisible on the olive navbar. I replaced it with a custom SVG data URI in CSS to draw a tan-coloured hamburger icon.
 
**4. Image zoom overlay**  
Getting the zoom animation to feel satisfying required a `cubic-bezier` spring curve rather than a linear or ease transition, which I discovered by experimenting with `animation-timing-function` values.
 
### What I Learned
- How to properly customise Bootstrap using CSS custom properties without forking the framework.
- The `<picture>` element and `srcset`/`sizes` attributes for art direction and resolution switching.
- How to maintain accessibility (focus management, ARIA, skip links) while building interactive components from scratch.
- The importance of establishing a design token system (`--lv-*` variables) early — it made global colour changes trivial.
---
 
## 📚 Assets & Resources
 
### Frameworks & Libraries
| Name | Version | URL | Purpose |
|------|---------|-----|---------|
| Bootstrap | 5.3.3 | https://getbootstrap.com | CSS/JS framework |
| Animate.css | 4.1.1 | https://animate.style | Additional CSS animation library |
| Google Fonts | — | https://fonts.google.com | Web fonts |
 
### Fonts
| Font | License | URL |
|------|---------|-----|
| Dancing Script | OFL | https://fonts.google.com/specimen/Dancing+Script |
| Lora | OFL | https://fonts.google.com/specimen/Lora |
| Raleway | OFL | https://fonts.google.com/specimen/Raleway |
 

 
## ♿ Accessibility
 
- Skip navigation link on every page
- Semantic HTML5 landmark elements (`<header>`, `<nav>`, `<main>`, `<footer>`)
- Logical heading hierarchy (`h1` → `h2` → `h3`)
- Descriptive `alt` text on all images
- ARIA labels on icon-only links (social media)
- Keyboard navigation: Tab through all interactive elements; Escape closes zoom overlay
- Sufficient colour contrast between text and backgrounds
- `aria-current="page"` on active nav link
- `aria-required="true"` on required form fields
---
 
## 🖼️ Figma Designs
 https://www.figma.com/design/rxNZrDH8KVQq5QAugx2XBB/High-Fidelity-Frames?node-id=0-1&t=6tmGYJADuLxrbmM8-1
 

 I made some changes