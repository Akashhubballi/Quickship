# QuickShip™ Logistics - Commercial Courier & Delivery Platform

An enterprise-grade, modern courier and parcel delivery website prototype crafted exclusively with **Semantic HTML5** and **Modern CSS3** (No JavaScript, No Frameworks, No Bootstrap, No Tailwind).

---

## 📦 Project Overview

**QuickShip** is a commercial logistics platform interface engineered to showcase high-fidelity web design, clean layout architecture, and pure-CSS interactivity. It replicates the functionality, design aesthetics, and user experience of leading modern logistics platforms like Flexport, ShipBob, and DHL Express.

### Key Highlights
- **100% Pure HTML5 & CSS3**: Zero JavaScript dependencies, zero external CSS libraries.
- **Pure CSS Navigation**: Responsive slide-down mobile navigation powered by the CSS checkbox hack.
- **Pure CSS Radio Cards**: Interactive delivery speed selection with dynamic `:checked` state styling.
- **Pure CSS Accordion**: FAQ section built with semantic `<details>` and `<summary>` elements with styled toggles.
- **Enterprise Design System**: Reusable CSS custom properties (variables), clean typography (Plus Jakarta Sans & Inter), soft multi-layer shadows, and responsive Flexbox & CSS Grid.
- **Zero Broken Links**: Seamless cross-navigation between all 5 pages.
- **Completely Responsive**: Tested across Mobile (320px–480px), Tablet (481px–768px), Laptop (769px–1024px), and Desktop (1025px+).

---

## 🗂️ Project Structure

```text
quickship/
├── index.html        # Home page (Hero, Quick Tracker, Services, How it Works, Stats, Reviews)
├── booking.html      # Courier booking page (Sender/Receiver form, parcel specs, delivery speed, summary)
├── tracking.html     # Consignment tracking page (Milestone timeline, AWB metadata, audit log)
├── services.html     # Delivery services (Same-Day, Air Express, Ground, Freight & comparison matrix)
├── contact.html      # Contact page (24/7 hotline, operations desk, inquiries form, pure-CSS FAQ)
├── README.md         # Full documentation, resume description & technical interview prep
├── css/
│   └── style.css     # Unified enterprise stylesheet with CSS variables & responsive media queries
└── assets/
    └── images/       # Static assets folder (inline SVGs used for zero-latency, high-DPI clarity)
```

---

## 🚀 How to Run the Project

No build step, node modules, or local server installation is required!

### Option 1: Direct Browser Opening
1. Navigate to the `quickship/` folder on your computer.
2. Double-click on `index.html` to open it in Google Chrome, Mozilla Firefox, Microsoft Edge, or Safari.
3. Use the top navigation bar or CTA buttons to move between all 5 pages.

### Option 2: Using VS Code Live Server (Optional)
1. Open the `quickship/` folder in Visual Studio Code.
2. If installed, right-click `index.html` and click **"Open with Live Server"**.
3. The site will run at `http://127.0.0.1:5500/index.html`.

---

## 📱 Responsive Testing Checklist

| Breakpoint Range | Target Devices | Key Layout Behavior Verified |
| :--- | :--- | :--- |
| **320px – 480px** | iPhone SE, 13/14/15 Mini, Galaxy S series | Hamburger menu active; 1-column stats; stacked forms; full-width inputs; vertical tracking steps. |
| **481px – 768px** | iPad Mini, Android tablets, large foldables | 2-column stats; mobile menu active; stacked booking layout; horizontal overflow scroll on data tables. |
| **769px – 1024px** | iPad Pro, small laptops, Surface tablets | Desktop navigation bar; 2-column hero; 2-column how-it-works; side-by-side forms. |
| **1025px and above** | Desktops, ultrawides, MacBooks | Full multi-column grids; sticky order summary; 4-column timeline; 4-column service cards. |

---

## 💼 Resume-Ready Project Description

You can copy and adapt this bulleted section for your software engineering / frontend resume:

> **QuickShip – Commercial Courier & Logistics Platform (HTML5 / CSS3)**
> - Engineered a commercial-grade, multi-page courier and parcel logistics prototype using **semantic HTML5** and **modern CSS3**, maintaining zero external framework or JavaScript dependencies.
> - Implemented advanced CSS-only interactive components, including a mobile hamburger navigation drawer using the **checkbox hack**, interactive delivery speed selector cards using `:checked` pseudo-classes, and an accordion FAQ using `<details>` and `<summary>`.
> - Designed a modular design system using **CSS Custom Properties (Variables)** for colors, elevation, typography, and spacing, ensuring consistent brand identity across 5 interconnected pages.
> - Built responsive fluid layouts across mobile, tablet, and desktop viewports using **CSS Flexbox** and **CSS Grid**, adhering to WCAG accessibility guidelines with proper `<label>` associations and semantic tags.

---

## 🎯 Technical Frontend Interview Questions & Answers

### Q1: How did you implement an interactive mobile hamburger menu without JavaScript?
**Answer:**  
"I utilized the CSS **Checkbox Hack**. A hidden `<input type="checkbox" id="nav-toggle" class="nav-toggle">` is placed in the DOM right next to a `<label for="nav-toggle">` representing the hamburger icon. In CSS, the navigation menu is positioned off-screen by default using `transform: translateY(-150%)` and `opacity: 0`. When the user clicks the label, the checkbox is toggled. Using the CSS adjacent or general sibling combinator:
```css
.nav-toggle:checked ~ .nav-menu {
  transform: translateY(0);
  opacity: 1;
}
```
the menu smoothly animates into view without a single line of JavaScript."

---

### Q2: Why did you choose CSS Grid over Flexbox for the Delivery Services and How It Works sections?
**Answer:**  
"Flexbox is ideal for **one-dimensional** layouts (either a single row or single column) where items distribute available space along an axis. In contrast, **CSS Grid** is designed for **two-dimensional** layouts with strict row and column tracks. For the services grid and statistics bar, CSS Grid with `grid-template-columns: repeat(auto-fit, minmax(260px, 1fr))` ensures all cards maintain equal height, consistent gutters, and automatically wrap responsively without needing complex margin calculations."

---

### Q3: How did you create the interactive delivery speed selection cards on the booking page without JavaScript?
**Answer:**  
"I used hidden native `<input type="radio" name="delivery_tier" id="tier-express">` elements paired with `<label for="tier-express" class="option-card-label">`. The radio inputs are visually hidden using `position: absolute; opacity: 0; pointer-events: none;`. When a user clicks any option card, the browser natively selects that radio button. We then target the sibling label with the `:checked` pseudo-class:
```css
.option-radio-input:checked + .option-card-label {
  border-color: var(--primary);
  background-color: var(--primary-subtle);
  box-shadow: 0 0 0 2px var(--primary);
}
```
This guarantees 100% native accessibility, keyboard navigation, and zero JavaScript overhead."

---

### Q4: What are the benefits of using CSS Custom Properties (`:root` variables) in a multi-page project?
**Answer:**  
"CSS variables provide centralized tokens for colors, shadows, borders, and typography. Instead of hardcoding hex values across a 600-line stylesheet, changing `--primary: #1d4ed8` updates all buttons, focus rings, badges, and icons instantly. They also cascade dynamically and can be overridden locally or adapted for dark mode themes using media queries like `@media (prefers-color-scheme: dark)`."
