# 🎓 UniFind: Campus Lost and Found Management Portal
**College Internet Programming Project**

A modern, responsive, and interactive web application designed to help university students, faculty, and administrative staff report, track, and reclaim lost items across campus.

---

## 🌟 Features Implemented

1. **Dual-Tab Interface**:
   - Seamlessly toggle between **Lost Items** and **Found Items**.
   - Live badge counters displaying active reports for each tab.

2. **Category Filtering**:
   - Instant filtering pills for key campus categories:
     - 💻 **Electronics** (Laptops, Earbuds, Chargers, Calculators)
     - 🪪 **ID Cards** (Student IDs, Access Cards, Library Passes)
     - 📚 **Books/Notes** (Textbooks, Binders, Handwritten Notebooks)
     - 🔑 **Keys** (Dormitory Keys, Bike Locks, Vehicle Keys)
     - 🎒 **Personal Accessories** (Backpacks, Sunglasses, Bottles)
   - "All Categories" option for comprehensive browsing.

3. **Interactive Item Reporting Form (Modal)**:
   - Dynamic report form supporting both Lost and Found submissions.
   - Comprehensive input fields:
     - **Item Name** (with real-time validation)
     - **Category** dropdown
     - **Date Last Seen / Date Found** (calendar picker restricted to past/today dates)
     - **Campus Location** (pre-set university landmarks like Central Library, Engineering Hall, Student Center, Sports Complex, etc.)
     - **Specific Room / Area**
     - **Contact Information** (Name, Phone/Email)
     - **Description & Identifiable Marks**
     - **Item Photo** (Local file upload via FileReader API with live thumbnail preview or external image URL)
   - Client-side validation with inline error messaging.

4. **Live Search & Multi-Criteria Filtering**:
   - **Real-time Keyword Search**: Matches item titles, descriptions, specific rooms, and reporter info on every keystroke.
   - **Campus Location Filter**: Narrows down items by specific buildings or grounds.
   - **Status Filter**: View Active Only, Reunited/Resolved, or All items.
   - **Date Sorting**: Sort by newest or oldest reports.
   - **Active Filter Chips**: Visually displays all applied filters with one-click removal.

5. **Item Details & Claim Management**:
   - Detailed modal card with full item specification and description.
   - Direct contact buttons (`mailto:` and `tel:`).
   - "Mark as Reunited / Claimed" status toggle.
   - Delete report capability.

6. **Persistence & Demo Data**:
   - Built with the **HTML5 Web Storage API (`localStorage`)** so items and status updates persist across page reloads.
   - Preloaded with realistic college campus demo data.
   - "Reload Demo Data" button to instantly restore sample records for grading demonstrations.

---

## 💻 Tech Stack & Internet Programming Concepts

- **HTML5**: Semantic tags (`<header>`, `<main>`, `<article>`, `<section>`, `<dialog>`/modal patterns, `<figure>`, `<time>`, accessible `aria-*` attributes).
- **CSS3**:
  - CSS Custom Properties (Variables) for theming.
  - Flexbox and CSS Grid for responsive multi-column layouts.
  - Media Queries (`@media`) for cross-device responsiveness (mobile, tablet, desktop).
  - Micro-interactions, transitions, backdrop blur, and toast animations.
- **JavaScript (ES6+)**:
  - Modular clean code architecture with unified application state.
  - DOM manipulation and event delegation.
  - Form validation and input sanitization.
  - Web Storage API (`localStorage`) for persistence.
  - HTML5 FileReader API for in-browser client-side image preview.

---

## 🚀 How to Run the Project

No server installation, Node.js, or external package managers are needed!

1. Navigate to the project directory:
   ```
   C:\Users\kusha\.gemini\antigravity\scratch\campus-lost-found\
   ```
2. Double-click **`index.html`** to launch the portal in any web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari).
3. Alternatively, if using VS Code, right-click `index.html` and select **"Open with Live Server"**.

---

## 📂 Project Structure

```
campus-lost-found/
├── index.html       # Semantic HTML5 markup, modals, controls, and layout
├── style.css        # CSS3 custom variables, grid, flexbox, cards, and responsiveness
├── app.js           # Application state, localStorage, real-time filtering, DOM logic
└── README.md        # Comprehensive documentation & project report
```

---

## 💡 Viva / Presentation Discussion Points

- **Why use LocalStorage?**
  It provides zero-setup client-side persistence, enabling the portal to retain reported items even if the user refreshes or closes the browser window.
- **How does live search work?**
  An `input` event listener fires on the search field, combining the search string with active category and location filters to compute a filtered items list in memory and re-render the DOM efficiently.
- **How is mobile responsiveness achieved?**
  Using a mobile-first approach with flexible CSS Grid (`repeat(auto-fill, minmax(320px, 1fr))`) and media queries at `768px` and `992px` breakpoints to adapt navigation, form rows, and card layouts smoothly.
