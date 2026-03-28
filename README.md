# CompTIA Tech+ (FC0-U71) — Interactive Study Guide

A **single-file, browser-based** study guide for **CompTIA Tech+** certification. No build step, no npm—open the HTML, study offline or online, and track progress in your browser.

> **Disclaimer:** This project is **independent study material**. It is not affiliated with, sponsored by, or endorsed by CompTIA. Exam names and objectives are trademarks of their respective owners. Passing the real exam depends on your preparation and Pearson VUE testing conditions—not on this repository.

---

## Features

| Feature | Description |
|--------|-------------|
| **Seven domain chapters** | IT concepts, infrastructure, applications & OS, software development, data & databases, security, plus acronyms & drills. |
| **Lesson-style content** | Narrative explanations, tables, scenarios, “Exam Essentials” recap blocks, and troubleshooting flow. |
| **Progress tracking** | Per-objective checkboxes and optional “Skip — I know this” per domain; progress bar excludes skipped modules. |
| **Chapter check-ins** | Five-question mini-quizzes after each chapter with explanations. |
| **Full practice exam** | **52 questions** (46 single-choice + **6 select-all-that-apply**), shuffled sessions, grading with explanations. |
| **45-minute timer** | Optional exam-pace drill on the practice page. |
| **Acronym table** | Large built-in glossary with **search/filter** and a **matching drill** (random rounds). |
| **Study mode** | Fullscreen toggle for fewer distractions. |
| **Persistence** | State saved in **`localStorage`** under the key `techplusStudyGuide_v1` (same browser/profile). |
| **Pass-readiness contract** | Checklist on the home screen for how to prep before scheduling the real test. |

---

## Quick start

1. Clone or download this repository.
2. Open **`TechPlus_Study_Guide.html`** in a modern browser (Chrome, Edge, Firefox, or Safari).
3. Use the left sidebar to navigate **Home**, chapters **1–7**, or **Practice exam**.

**Important:** Some browsers restrict `localStorage` or file access when opening HTML via `file://`. If anything behaves oddly, serve the folder with a tiny static server, for example:

```bash
# Python 3
python -m http.server 8080
```

Then open `http://localhost:8080/TechPlus_Study_Guide.html`.

---

## Repository layout

```
TechPlus/
├── README.md                    ← this file
└── TechPlus_Study_Guide.html    ← the entire app (content + styles + scripts)
```

All study content—including **Exam Essentials** recap sections—is self-contained in the HTML file.

---

## How to study (recommended)

1. Read chapters **1 → 7** in order; complete each **Chapter check-in** mini-quiz.
2. Check off objectives only when you could explain them **without** reading.
3. Use the **acronym** table + **matching drill** until rounds feel easy.
4. Take the **practice exam** multiple times on **shuffled** sessions; use the **45-minute timer** for at least one full run.
5. Follow the **pass-readiness contract** on the Home page before booking the exam.

Official objectives (always verify the current bulletin):

**[CompTIA Tech+ certification & objectives](https://www.comptia.org/en-us/certifications/tech/#objectives)**

---

## Resetting progress

- Use **Reset saved progress** in the sidebar to clear objectives, skip flags, and reset on-screen quizzes/practice exam for this site origin.

---

## Browser storage

| Key | Purpose |
|-----|---------|
| `techplusStudyGuide_v1` | Objective checkmarks, module skip flags (`localStorage`) |

Export/import is not built in; back up your browser profile or avoid resetting if you care about history.

---

## Tech stack

- **HTML5** + **CSS** (custom dark theme, responsive sidebar)
- **Vanilla JavaScript** (IIFE, no frameworks)
- Fonts: **Space Grotesk** + **JetBrains Mono** (loaded from Google Fonts; requires network unless cached)
