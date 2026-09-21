# MediCare+ — Hospital & Healthcare Management System

An **accessibility-first** Hospital & Healthcare Management System frontend, built with **HTML5, CSS3 and Bootstrap 5** — no framework, no backend, no build step. Open a page in a browser and it runs.

The project digitizes hospital operations (patients, doctors, appointments, departments, prescriptions and billing) and adds a **Clinical Command Center** with an emergency triage board and a live bed-occupancy view.

---

## Group No.

**Group 2**

## Team Members

| S.No | Name | Enrollment No. | Role |
|------|------|----------------|------|
| 1 | Ansh Pratap Singh | 2415000256 | Team Lead |
| 2 | Ankit Parashar | 2415000235 | Member |
| 3 | Aniket Singh | 2415000216 | Member |
| 4 | Akhil Tripathi | 2415000160 | Member |

**Team Lead:** Ansh Pratap Singh

---

## Features

- **Command Center dashboard** — hospital statistics, "Now serving" token ticker, triage summary, bed occupancy and low-stock medicines.
- **Patients** — searchable/filterable records, add-patient form, and a unified **health timeline** (appointments → diagnoses → prescriptions → bills).
- **Doctors & Departments** — card directory with department filters and availability badges.
- **Appointments** — list with status badges and a booking modal.
- **Prescriptions & Billing** — digital records with **print-ready** output (hospital letterhead via `@media print`).
- **Clinical Command Center** — **ER triage board** (Manchester urgency scale) and a **bed-occupancy grid**.
- **Accessibility-first** — WCAG 2.1 Level AA: skip link, keyboard navigation, visible focus, ARIA labels, non-colour status badges, three themes (Light / Dark / High-Contrast) and text-size controls.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Structure | HTML5 (semantic markup) |
| Styling | CSS3 (custom properties / design tokens) |
| UI framework | Bootstrap 5 (CDN) |
| Icons | Bootstrap Icons (CDN) |
| Behaviour | Bootstrap bundle JS + a small inline script (theme, text size, mobile menu) |

## Project Structure

```
.
├── index.html              # Command Center dashboard
├── login.html              # Login / sign up
├── patients.html           # Patients list
├── patient-profile.html    # Patient health timeline
├── add-patient.html        # Add / edit patient
├── doctors.html            # Doctors directory
├── appointments.html       # Appointments + booking
├── departments.html        # Departments
├── prescriptions.html      # Prescriptions (print-ready)
├── billing.html            # Invoices (print-ready)
├── triage.html             # Emergency triage board
├── beds.html               # Bed occupancy grid
├── accessibility.html      # Accessibility statement
└── css/
    ├── style.css           # Design tokens, layout, components, print styles
    ├── theme-dark.css      # Dark theme
    └── theme-contrast.css  # High-contrast theme
```

## How to Run

No installation or build step is required. Choose either option:

**Option 1 — open directly**

Double-click `index.html`, or:

```bash
xdg-open index.html
```

**Option 2 — local server (recommended)**

```bash
python3 -m http.server 8080
```

Then open <http://localhost:8080> in your browser.

> Bootstrap and Bootstrap Icons load from a CDN, so an internet connection is needed for the styling and icons.

## Work Division

Work is divided by files to keep ownership clear and avoid merge conflicts.

| Member | Part | Responsibility | Code files |
|--------|------|----------------|------------|
| **Ansh Pratap Singh** | Part 1 | Foundations, Command Center, Triage & Bed Occupancy | `login.html`, `index.html`, `triage.html`, `beds.html`, `css/style.css`, `css/theme-dark.css`, `css/theme-contrast.css` |
| **Ankit Parashar** | Part 2 | Patients | `patients.html`, `add-patient.html`, `patient-profile.html` |
| **Aniket Singh** | Part 3 | Doctors, Appointments & Departments | `doctors.html`, `appointments.html`, `departments.html` |
| **Akhil Tripathi** | Part 4 | Prescriptions, Billing & Accessibility | `prescriptions.html`, `billing.html`, `accessibility.html` |

> The three stylesheets under `css/` are shared by every page and are maintained by Part 1 (Ansh Pratap Singh). All other files are owned solely by the member listed above.

## Git Workflow

- `main` holds the stable, submission version and is never pushed to directly.
- `dev` is the integration branch — all feature Pull Requests merge here first.
- Each member works in a `feature/*` branch and opens a Pull Request into `dev`.
- After testing, a single final Pull Request merges `dev` into `main`.

```
feature/*  →  PR  →  dev  →  test  →  PR  →  main
```
