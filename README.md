# Sian Studio — CSS-Only Sidebar Navigation

A photography portfolio UI featuring a fully interactive sliding sidebar — **built with pure HTML and CSS, zero JavaScript**.

![Project Preview](req_photo.jpg)


## 💡 What Makes This Special

Most sidebar menus rely on JavaScript to toggle open/close state. This project achieves the same result using a **hidden checkbox + CSS `:checked` sibling selector** — a pure CSS state management technique.

```css
/* Sidebar slides in when checkbox is checked */
#check:checked ~ .sidebar_menu {
  left: 0;
}

/* Hamburger button hides when sidebar is open */
#check:checked ~ .btn_one {
  opacity: 0;
}
```

No `addEventListener`. No `classList.toggle`. No JS at all.

---

## ✨ Features

- **CSS-only toggle** — sidebar open/close driven entirely by `<input type="checkbox">` and the `:checked` pseudo-class
- **Glassmorphism sidebar** — frosted-glass effect using `rgba` background and `box-shadow` with white glow
- **Smooth transition** — `transition: all 0.3s linear` on the sidebar's `left` property for a clean slide-in
- **Responsive layout** — sidebar is `position: fixed` and full-height (`100vh`), works across screen sizes
- **Hover micro-interactions** — menu items glow on hover; icons subtly scale; hamburger icon grows on hover — all CSS
- **Font Awesome icons** — semantic icons for every nav link and social media channel
- **Google Fonts (Poppins)** — clean, modern typeface loaded via preconnect for performance
- **Full-screen hero background** — `background-size: cover` ensures the photo fills the viewport at any resolution

---

## 🗂️ Project Structure

```
sian-studio/
├── index.html          # Markup: sidebar, menu items, social links
├── main_project.css    # All styling and interaction logic
└── req_photo.jpg       # Hero background (camera photo)
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Semantic structure |
| CSS3 | Layout, animation, and state management |
| Font Awesome 6.4 | Icons |
| Google Fonts (Poppins) | Typography |

**No frameworks. No libraries. No JavaScript.**

---

## 🧠 Key CSS Concepts Used

| Concept | Where It's Applied |
|---|---|
| `position: fixed` | Sidebar sticks to the left edge of the viewport |
| CSS sibling selector (`~`) | Links checkbox state to sidebar and button visibility |
| `transition` | Smooth slide-in animation on `left` property |
| `rgba()` transparency | Glassmorphism effect on the sidebar panel |
| `box-shadow` with white glow | Subtle border and depth on sidebar and menu items |
| Pseudo-class `:checked` | Drives the entire open/close interaction |
| `opacity` | Hides hamburger button when sidebar is open |
| `transform: scale()` | Hover effect on social media icons |

---

## 📖 How the Toggle Works

The trick is using HTML's native checkbox state as a CSS hook:

1. A hidden `<input type="checkbox" id="check">` acts as the state store.
2. The hamburger button (`btn_one`) is a `<label for="check">` — clicking it checks/unchecks the box.
3. The close `×` button (`btn_two`) inside the sidebar is also a `<label for="check">` — clicking it unchecks the box.
4. CSS sibling selectors (`~`) watch the checkbox state and update the sidebar position and button visibility accordingly.

This pattern replaces JavaScript toggle logic entirely.

---

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/sian-studio.git
cd sian-studio
# Open index.html in your browser — no build step needed
```

Or just open `index.html` directly in any modern browser.

