<<<<<<< HEAD
# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
=======
# FactWise · People Dashboard

> A sleek, dark-themed employee analytics dashboard built with **AG Grid** — designed to match the FactWise product UI and handle large datasets efficiently.

![FactWise Dashboard](https://img.shields.io/badge/AG%20Grid-31.3.2-00c49a?style=flat-square&logo=javascript&logoColor=white)
![Vanilla JS](https://img.shields.io/badge/Vanilla-JavaScript-f59e0b?style=flat-square&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-a78bfa?style=flat-square)
![Status](https://img.shields.io/badge/Status-Assessment%20Ready-22c55e?style=flat-square)

---

## What's Inside

A single-file dashboard (`index.html`) that brings together everything needed to explore, filter, and export employee data — no build step, no dependencies to install, just open and go.

```
📁 factwise-dashboard/
└── 📄 index.html        ← entire app lives here
```

---

## Features

**Grid**
- Client-side AG Grid with 12 columns of rich employee data
- Column sorting, resizing, and reordering out of the box
- Pinned `Employee` column so names stay in view while scrolling
- Custom cell renderers for every column — no raw text anywhere

**Filters**
- Live search across name, email, position, location, department, and manager
- Department dropdown filter
- Active / Inactive status filter
- All three filters compose together in real time
- KPI cards update dynamically as you filter

**KPI Summary Bar**
- Total employees · active vs inactive split
- Average salary across visible records
- Average performance rating
- Total projects completed
- Department and office location count

**Export**
- One-click CSV export via AG Grid's native API

**Design**
- Dark navy theme extracted directly from `factwise.io`
- Teal `#00c49a` accent — the FactWise brand colour
- Inter font, tabular numerals, tight letter-spacing
- Department colour-coded badges and avatar initials
- Glowing green dot for active status
- Performance bar that shifts green → teal → amber by score

---

## Quick Start

No installation. No terminal. Just:

```bash
# Option 1 — double-click
open index.html
```

```bash
# Option 2 — local server (recommended)
npx serve .
# then visit http://localhost:3000
```

```bash
# Option 3 — Python
python -m http.server 8080
# then visit http://localhost:8080
```

---

## Dataset

20 employees across 5 departments — Engineering, Marketing, Sales, HR, and Finance — spanning 6 US cities. Each record includes:

| Field | Type |
|---|---|
| `id` | number |
| `firstName` / `lastName` | string |
| `email` | string |
| `department` | string |
| `position` | string |
| `salary` | number |
| `hireDate` | ISO date string |
| `age` | number |
| `location` | string |
| `performanceRating` | float (0–5) |
| `projectsCompleted` | number |
| `isActive` | boolean |
| `skills` | string[] |
| `manager` | string \| null |

---

## Scaling to Real Data

The grid is configured for client-side rendering — swap the inline `employees` array for a `fetch()` call and nothing else changes:

```js
// Replace this:
const employees = [ /* hardcoded */ ];

// With this:
const response = await fetch('https://your-api.com/employees');
const employees = await response.json();
```

For datasets beyond ~10,000 rows, enable AG Grid's Server-Side Row Model by changing one option:

```js
rowModelType: 'serverSide'
```

---

## Tech Stack

| Layer | Choice | Why |
|---|---|---|
| Grid | AG Grid Community 31.3.2 | Fastest client-side grid available |
| Runtime | Vanilla JS (ES2020) | Zero framework overhead |
| Fonts | Inter via Google Fonts | Matches FactWise product typography |
| Icons | Inline SVG | No icon font dependency |
| Styles | Plain CSS with custom properties | Easy to theme, no preprocessor needed |

---

## Customisation

All colours live in `:root` CSS variables at the top of the file — change the theme in one place:

```css
:root {
  --fw-bg:    #0a0e1a;   /* page background   */
  --fw-teal:  #00c49a;   /* primary accent     */
  --fw-text:  #f1f5f9;   /* primary text       */
}
```

Adding a new column is one object in `columnDefs`:

```js
{
  headerName: 'Your Column',
  field: 'yourField',
  minWidth: 120,
  cellRenderer: ({ value }) => `<span>${value}</span>`
}
```

---

## Built For

This dashboard was built as part of the **FactWise frontend assessment** — demonstrating AG Grid proficiency, FactWise design system fluency, and clean scalable code structure.

---

<div align="center">
  <sub>Built with 🖤 for the FactWise team</sub>
</div>
>>>>>>> 274a4b8edddd0487b780053d54abb37e00098161
