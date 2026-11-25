# Zeiterfassung · Internistische Praxis Linda Pars Pour

**Open the app:** https://ario-ghs.github.io/praxis-zeiterfassung/

![Staff board](docs/screenshots/02-stempeltafel.png)

A staff time-tracking kiosk for a small medical practice (up to 10 employees), in German and English. It runs on one shared PC or tablet at the reception desk.

## How it works

- **Staff board:** every employee has a card on the board. Tap your card, enter your 4-digit PIN, then tap **Kommen**, **Pause beginnen**, **Pause beenden** or **Gehen**.
- **My month:** after logging in, each employee sees today's times, actual vs. target hours, overtime balance and remaining vacation days.
- **Requests:** employees request vacation, report sick, request time off in lieu or ask for a time correction. Absences only count after the practice lead approves them.
- **Admin area (PIN-protected):** live overview of who is present, approval of requests, correction of times with a required reason (every change is logged), staff management and settings.
- **Variable shifts:** target hours are set per weekday for each employee (for example Wednesday 4 hours). Actual start and end times can differ every day.
- **Reports:** monthly Excel (summary sheet plus one sheet per employee) and PDF (summary page plus one page per employee with signature fields), with the practice logo.
- **German rules built in:** Hamburg public holidays (other states selectable) and Working Time Act (ArbZG) warnings for breaks, maximum hours and rest periods.

## Documentation

- **User manual (German):** [Benutzerhandbuch](docs/Benutzerhandbuch.md) · [PDF](docs/Benutzerhandbuch.pdf) – step-by-step chapters for staff and for the practice lead
- **Technical documentation (English):** [DOCUMENTATION](docs/DOCUMENTATION.md) · [PDF](docs/DOCUMENTATION.pdf) – architecture, data model, calculation rules, deployment

## Screenshots

| Clock in | Admin overview | Monthly report |
|---|---|---|
| <img src="docs/screenshots/04-mitarbeiterbereich.png" width="280" alt="Employee panel"> | <img src="docs/screenshots/09-uebersicht.png" width="280" alt="Admin overview"> | <img src="docs/screenshots/22-bericht-mitarbeiter.png" width="280" alt="PDF report"> |

## Data and privacy

All data is stored **only on the device** where the app runs. Nothing is sent to a server. Save a backup regularly (**Verwaltung → Einstellungen → Sicherung speichern**), for example to a USB stick or practice drive.

## Demo

On first start, choose **Mit Demo-Daten starten** to try the app with four sample employees (PINs 1111, 2222, 3333, 4444; admin PIN 0000). Delete the demo data in **Einstellungen** before real use and set a new admin PIN.

## Files

| File | Purpose |
|---|---|
| `index.html` | The app |
| `manifest.json`, `sw.js` | Installable app and offline support |
| `xlsx.min.js` | Excel export ([xlsx-js-style](https://github.com/gitbrent/xlsx-js-style), Apache-2.0) |
| `jspdf.umd.min.js`, `jspdf.plugin.autotable.min.js` | PDF export ([jsPDF](https://github.com/parallax/jsPDF), [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable), MIT) |
| `logo.png`, `icon-192.png`, `icon-512.png` | Practice logo and app icons |
| `docs/` | User manual, technical documentation and screenshots |

## License

Code released under the [MIT License](LICENSE). The practice name and logo belong to Internistische Praxis Linda Pars Pour and are not covered by this license.

Built by [Ario Samani](https://github.com/ario-ghs).
