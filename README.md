# ClinHistory — Adaptive History Taking & Case Presentation

A single-file web app for medical students to take systematic patient history as per **Archith Boloor — *Insider's Guide to Clinical Medicine*** and auto-generate a viva-ready case presentation with provisional & differential diagnosis.

**Live app:** `history-taking-app.html` — just open in any browser. No build, no server. All data stays in `localStorage`.

## Features (8-step wizard)

1. **Patient Particulars** — Name, Age, Sex, Occupation, Religion, Handedness, Address, Informant & Reliability
2. **Chief Complaints** — In patient's words, duration, onset, progression + *aggravation of chronic baseline symptoms* (e.g., COPD exacerbation)
3. **History of Present Illness (Adaptive)** — Parses chief complaints (chest pain, dyspnea, cough, fever, headache, abdominal pain, etc.) and generates SOCRATES-based questions. Also captures aggravating/relieving factors & treatment response.
4. **Past History** — Comorbidities, childhood illness, hospitalizations/surgeries/transfusions, detailed drug & allergy history, immunization
5. **Personal / Social & Habits** — Diet, sleep, bowel/bladder, weight, smoking (pack-years), alcohol (units), tobacco/areca/cannabis, occupational/environmental exposure, travel/contact. **Menstrual & Obstetric** auto-appears when Sex=Female (menarche, cycle, LMP, G/P/L/A).
6. **Family & Socioeconomic** — Pedigree, consanguinity, SES (Kuppuswamy), housing, support
7. **Review of Systems** — 7-system checklist, auto-ticks relevant to chief complaints
8. **Provisional Diagnosis & Differentials** — Rule-based from combined history (ACS, HF, pneumonia, TB, acute abdomen, CNS infection, etc.) + manual clinician impression

## Presentation Output

Right panel shows a **live, printable case presentation** in standard medical format, ready to copy or `Print → Save as PDF`. Format:

> Patient particulars → Chief complaints (chronological) → HPI narrative (SOCRATES + adaptive answers) → Past / Personal / Family / ROS → Provisional & Differentials → Plan (examination + investigations)

## How to use

```bash
open history-taking-app.html
# or double-click the file
```

1. Fill steps 1→8 clicking **Next**
2. Watch live preview update on the right
3. **Copy Text** or **Print / PDF** to share

Data autosaves in browser; **Reset** clears it. Disclaimer included — academic aid only, correlate with examination.

## Tech

- Single HTML file, Tailwind CDN, vanilla JS
- No backend, no dependencies to install
- Adaptive engine at `symptomDB` and `generateDiagnosis()`

## Reference

Based on history-taking methodology in **Archith Boloor — *An Insider's Guide to Clinical Medicine***.

## License

Academic use.
