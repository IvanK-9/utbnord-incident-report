# Utbildning Nord — Incident & Near-Miss Reporter
### *Tillbudsrapport • Läheltä piti -ilmoitus • Avviksrapport*

> A zero-dependency, fully accessible, multilingual incident and near-miss (*tillbud*) reporting web application engineered for students, instructors, and staff at **Utbildning Nord / Koulutus NORD** (Övertorneå, Sweden). Fully compliant with Swedish **Arbetsmiljöverket** systematic work environment standards (SAM).

[![Author](https://img.shields.io/badge/Author-Ivan%20Kozyrev-0b4f7c?style=flat-square&logo=github)](https://github.com/IvanK-9)
[![Project](https://img.shields.io/badge/Type-Educational%20Coursework%20Project-success?style=flat-square)](#-academic--educational-context)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=flat-square&logo=github)](https://IvanK-9.github.io/utbnord-incident-report/)
[![Compliance](https://img.shields.io/badge/Compliance-Arbetsmilj%C3%B6verket%20Standard-emerald?style=flat-square)](#-statutory-compliance-arbetsmilj%C3%B6verket)
[![Languages](https://img.shields.io/badge/Languages-EN%20%7C%20SV%20%7C%20FI%20%7C%20NO-orange?style=flat-square)](#-multilingual-architecture)
[![Architecture](https://img.shields.io/badge/Stack-Vanilla%20JS%20%7C%20HTML5%20%7C%20Tailwind%20CSS-purple?style=flat-square)](#-tech-stack--engineering-decisions)

---

## 🎓 Academic & Educational Context

This project was developed by **Ivan Kozyrev** as an educational coursework project at **Utbildning Nord / Koulutus NORD** (Övertorneå, Sweden).

The goal of the assignment is to design and implement a production-grade, enterprise-ready digital solution for a real-world institutional requirement: simplifying and accelerating workplace safety reporting across a culturally diverse, tri-national vocational education campus.

* **Developer**: Ivan Kozyrev ([@IvanK-9](https://github.com/IvanK-9))
* **Email**: [ivan.kozyrev@edunord.se](mailto:ivan.kozyrev@edunord.se)
* **Institution**: Utbildning Nord / Koulutus NORD, Övertorneå, Sweden
* **Focus**: Frontend Architecture, Accessibility (WCAG 2.2 AA), Multi-language UX, Regulatory Compliance.

---

## 📌 Context & Problem Statement

**Utbildning Nord** is a unique Nordic vocational training foundation established under international treaties between **Sweden, Finland, and Norway**. 

In high-risk vocational learning environments—including automotive mechanics, industrial welding, CNC machining, construction, HVAC, healthcare, and commercial culinary kitchens—speed and clarity in incident reporting prevent fatal accidents. 

This project removes communication and technical barriers:
1. **No Language Barrier**: Available instantly in **English**, **Swedish**, **Finnish**, and **Norwegian**.
2. **Zero Installation / Frictionless**: Runs directly in any desktop or mobile browser via standard HTML5/JS without requiring mobile apps or portal logins.
3. **Whistleblower / Privacy-Friendly**: Allows 1-click anonymous reporting to eliminate fear of reprimand while gathering crucial safety data.

---

## ✨ Key Features

- **🌐 Tri-National Multilingual Engine**: Seamless client-side switching between **English (default)**, **Swedish (`SV`)**, **Finnish (`FI`)**, and **Norwegian (`NO`)**. Localizes all UI labels, form controls, placeholders, department taxonomies, and validation messages without page reloads.
- **📸 Advanced Multi-Photo Documentation**:
  - Drag-and-drop file upload zone.
  - Multi-file selection (`<input type="file" multiple>`).
  - **Cumulative upload queue**: Adding photos incrementally does not overwrite previously selected images.
  - Interactive preview gallery with formatted file sizes (KB/MB), individual removal (`✕`), and "Remove all" controls.
  - High-performance memory management using `URL.createObjectURL` and `URL.revokeObjectURL` (no heavy base64 strings blocking the main thread).
- **🛡️ Privacy by Design (GDPR / SAM)**: Toggle between identified and anonymous reporting. In anonymous mode, contact input fields collapse, validation attributes (`required`) are removed dynamically, and no personal identifying metadata is saved.
- **⚡ Smart Defaults**: Automatically seeds local timestamps (ISO-8601) to minimize input fatigue during critical situations.
- **💾 Offline Resilience Buffer**: Automatically buffers submitted reports into browser `localStorage` to safeguard against connection drops in remote workshop zones.
- **🎨 Authentic Scandinavian Identity**: 
  - Official Utbildning Nord circular identity mark.
  - Tri-national ribbon border mirroring the official Nordic flag colors (Norway, Sweden, Finland).
  - Modern Scandinavian design system with rounded cards, clean contrast, and subtle depth.
- **🦌 Arctic Easter Egg**: Click the Lapland reindeer icon in the footer to automatically pre-populate the form with culturally authentic, humorous Arctic test scenarios across all 4 languages.

---

## ⚖️ Statutory Compliance (Arbetsmiljöverket)

The reporting data model directly implements the 7 mandatory requirements of the Swedish Work Environment Authority (*Arbetsmiljöverket*) for Systematic Work Environment Management (**SAM** - *Systematiskt arbetsmiljöarbete*, AFS 2001:1):

| # | Statutory Requirement | Implementation in System |
|:---:|---|---|
| **1** | **Vem** (Reporter & Witnesses) | Optional identified contact or anonymous toggle + involved witness tracking |
| **2** | **När** (Timestamp) | Exact incident date and time with smart automated initial value |
| **3** | **Var** (Location / Unit) | Structured taxonomy of campus departments (Welding, IT, Automotive, etc.) |
| **4** | **Vad hände** (Event Narrative) | Description covering both what occurred and potential near-miss consequences |
| **5** | **Orsaker** (Direct Causes) | Machinery defects, slippery surfaces, lighting, time pressure, human factors |
| **6** | **Åtgärder** (Immediate Actions) | On-site preventive actions taken (equipment tagged out, area cordoned off) |
| **7** | **Skyddsombud & Bevis** (Safety Rep & Photos) | Confirmation of safety rep notification + multi-photo documentation gallery |

---

## 🛠️ Tech Stack & Engineering Decisions

| Layer | Technology | Architectural Rationale |
|---|---|---|
| **Core Architecture** | Semantic HTML5 & Vanilla JavaScript (ES2020+) | Zero runtime dependencies, no build pipeline required, instant load times, 100% auditable source code. |
| **Styling** | Tailwind CSS & Modern CSS Custom Properties | Rapid design system iteration, responsive layout, accessible typography, consistent spacing tokens. |
| **Asset Management** | Inline Vector SVGs & Object URLs | Eliminates external font/icon requests, prevents layout shift (CLS), ensures offline functionality. |
| **Storage & Persistence** | HTML5 `localStorage` & File API | Offline buffer ensuring no report loss even if internet connectivity drops in field workshops. |

---

## 📂 Project Structure

```
utbnord-incident-report/
├── assets/
│   ├── logo.png             # Official circular logo (transparent PNG)
│   └── logo.jpg             # High-resolution raster brand mark
├── index.html               # Complete application (UI, i18n dictionary, state logic)
├── .gitignore               # Standard hygiene for OS and editor artifacts
└── README.md                # Project documentation and technical specification
```

---

## 🚀 Quick Start & Local Run

Because this project is built with **zero runtime dependencies**, it runs out-of-the-box in any modern web browser:

### Option 1: Direct File Run
Simply double-click `index.html` or open it directly in your browser:
```powershell
# Windows PowerShell
Start-Process "index.html"
```

### Option 2: Run with a Local Static Server
```bash
# Clone the repository
git clone https://github.com/IvanK-9/utbnord-incident-report.git
cd utbnord-incident-report

# Serve via any static web server
npx serve .
# or
python -m http.server 8080
```

---

## 📬 Contact & Portfolio

* **Developer**: Ivan Kozyrev
* **Institution**: Utbildning Nord / Koulutus NORD
* **GitHub**: [@IvanK-9](https://github.com/IvanK-9)
* **Email**: [ivan.kozyrev@edunord.se](mailto:ivan.kozyrev@edunord.se)
* **Live Application**: [https://IvanK-9.github.io/utbnord-incident-report/](https://IvanK-9.github.io/utbnord-incident-report/)
