# Utbildning Nord — Incident Reporter

> A lightweight, accessible, multilingual incident and near-miss (*tillbud*) reporting application engineered for students and staff at **Utbildning Nord / Koulutus NORD** across Sweden, Finland, and Norway. Fully compliant with **Arbetsmiljöverket** standards.

[![Tech](https://img.shields.io/badge/Stack-HTML5%20%7C%20Tailwind%20CSS%20%7C%20Vanilla%20JS-blue?style=flat-square)](#-tech-stack)
[![Compliance](https://img.shields.io/badge/Compliance-Arbetsmilj%C3%B6verket%20Standard-emerald?style=flat-square)](#-statutory-compliance)
[![Languages](https://img.shields.io/badge/Languages-EN%20%7C%20SV%20%7C%20FI%20%7C%20NO-orange?style=flat-square)](#-multilingual-engine)
[![Architecture](https://img.shields.io/badge/Architecture-Zero--Dependency-purple?style=flat-square)](#-architecture--design-decisions)

---

## 📌 Context & Problem Statement

**Utbildning Nord / Koulutus NORD** (Övertorneå, Sweden) is a tri-national vocational training foundation educating students from **Sweden, Finland, and Norway**. 

In vocational environments involving machinery, welding, construction, healthcare, and culinary arts, rapid and barrier-free safety reporting is critical. This project eliminates friction by providing a fast, mobile-friendly reporting portal available in all four campus languages, removing psychological and linguistic barriers to incident reporting.

---

## ✨ Key Features

- **🌐 4-Language Dynamic Engine**: Instant zero-reload translation across **English** (default), **Swedish** (`SV`), **Finnish** (`FI`), and **Norwegian** (`NO`), including localized select options and validation states.
- **🛡️ Privacy by Design**: Seamless toggle between identified and anonymous reporting, dynamically mutating DOM validation rules to prevent accidental identity leakage.
- **📷 Media Attachment Support**: Client-side image upload with thumbnail preview powered by the HTML5 `FileReader` API.
- **⏱️ Smart Defaults**: Automatically seeds local timestamps (ISO format) to reduce user effort during reporting.
- **💾 Local Resilience Buffer**: Saves submitted reports to `localStorage` buffer to protect against accidental browser closing or network drops.
- **🎨 Authentic Scandinavian Branding**: Clean UI featuring the school's signature Nordic tricolor border and custom vector SVG national heraldry.

---

## ⚖️ Statutory Compliance (Arbetsmiljöverket)

The data model directly adheres to the 7 mandatory guidelines established by the Swedish Work Environment Authority (*Arbetsmiljöverket*):

| # | Regulatory Requirement | System Implementation |
|---|---|---|
| **1** | **Vem** (Reporter & Witnesses) | Contact details + optional anonymity toggle + witness log |
| **2** | **Datum & Tid** (Timestamp) | Exact incident date and time with auto-populated defaults |
| **3** | **Plats & Enhet** (Location) | Vocational department taxonomy (Welding, IT, Construction, etc.) |
| **4** | **Beskrivning** (Description) | Incident narrative & near-miss potential risk assessment |
| **5** | **Direkta orsaker** (Direct Causes) | Machinery, lighting, environmental, stress, or human factors |
| **6** | **Åtgärder** (Immediate Actions) | On-site remedial actions (tag-out, cordon, first aid) |
| **7** | **Skyddsombud & Foto** (Safety Rep & Media) | Safety representative notification status + photo evidence |

---

## 🛠️ Tech Stack & Design Decisions

| Layer | Choice | Rationale |
|---|---|---|
| **Core** | Semantic HTML5 & Vanilla JS (ES6+) | Zero build step, instant deployment, zero maintenance overhead |
| **Styling** | Tailwind CSS (Utility-First) | Predictable, responsive, modern Scandinavian minimalist design |
| **Icons** | Inline Vector SVGs | Crisp rendering across all platforms without third-party font/asset bloat |
| **Storage** | Client-side `localStorage` API | Offline resilience buffer and client audit readiness |

---

## 📂 Project Structure

```
├── index.html       # Self-contained application (UI markup, styles, i18n dictionary, runtime logic)
├── .gitignore       # Production hygiene rules
└── README.md        # Technical documentation & project portfolio overview
```

---

## 🚀 Quick Start

The project runs completely client-side with zero external dependencies or build tooling:

```bash
# Clone the repository
git clone https://github.com/your-username/utbnord-incident-report.git
cd utbnord-incident-report

# Open directly in browser
start index.html

# Or serve via local server
npx serve .
# or
python -m http.server 8080
```
