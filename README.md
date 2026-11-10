# utbnord-incident-report — Utbildning Nord Incident Reporter

A lightweight, accessible, multilingual incident and near-miss reporting web application designed for students and staff at **Utbildning Nord / Koulutus NORD**.

## Features

- **4 Nordic & International Languages**: Full UI translation across English (`EN`, default), Swedish (`SV`), Finnish (`FI`), and Norwegian (`NO`).
- **Arbetsmiljöverket Compliant**: Aligned with Swedish Work Environment Authority standards for incident (*tillbud*) reporting:
  - Reporter identity & optional anonymity toggle
  - Witness documentation
  - Date & exact incident timestamp
  - Vocational department & location classification
  - Comprehensive event description & hazard risk assessment
  - Direct causes (equipment, lighting, stress, human factors)
  - Immediate corrective actions taken
  - Safety representative (*skyddsombud*) notification tracking
  - Photo / visual evidence attachment with preview
- **Zero-Dependency Lightweight Architecture**: Runs purely in the browser using HTML5, Tailwind CSS, and vanilla JavaScript.
- **Offline & Local Buffer**: Stores submissions locally via `localStorage` for reliability and auditing.

## Project Structure

```
├── index.html       # Single-page incident reporting form & internationalization engine
├── .gitignore       # Git ignore rules
└── README.md        # Project overview and documentation
```

## Running the Application

Simply open `index.html` in any modern web browser or serve it using any static web server:

```bash
# Using Python
python -m http.server 8080

# Using Node.js npx serve
npx serve .
```
