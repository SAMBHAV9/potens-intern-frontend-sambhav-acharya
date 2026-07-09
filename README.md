# potens-intern-frontend-sambhav-acharya
# Operations Cockpit Dashboard

This dashboard is designed for a senior operations user opening it at the start of the day. It presents the most urgent work first, gives a quick view of system alerts, and keeps the interface calm, readable, and efficient.

## How to run it

1. Open the project folder in a terminal.
2. Start a simple local server:
   - Python: `python -m http.server 8000`
3. Open the page in a browser at http://127.0.0.1:8000/index.html.

If you prefer, you can also open the HTML file directly, though the local server is the smoother option for a quick preview.

## What is included

- A top-5 action list with one-line context, priority metadata, and approve/hold actions.
- A mock anomaly panel showing system alerts.
- A live ticking countdown for a time-sensitive review metric.
- Full English and Hindi language support through a toggle.
- Keyboard shortcuts for power users: J and K to move, A to approve, and H to hold.
- A low-bandwidth mode that simplifies the layout and reduces visual weight.
- A dark interface designed to feel functional and calm rather than purely cosmetic.

## Design decisions

- Priority-first layout: The top five items are placed at the top because they are the most useful decisions to make early in the day.
- Calm visual hierarchy: The dark theme, generous spacing, and restrained color accents keep the screen easy to scan quickly.
- Simple language: The copy is written to feel natural and direct rather than overly polished or corporate.
- Bilingual support: English and Hindi are available in one toggle so the same view can work for mixed teams.
- Power-user support: Keyboard shortcuts are included for people who want to move through the list quickly without using a mouse.
- Desktop-first but responsive: The layout is designed for a desktop monitor, while still adapting to tablet widths without breaking the structure.

## Stretch options

- Keyboard shortcuts: Implemented. J and K move through the list, while A and H approve or hold the selected item.
- Low-bandwidth toggle: Implemented. A toggle in the header switches the UI to a simpler, lower-visual-weight layout with reduced shadows and lighter spacing.
- Dark mode: Implemented. The dashboard uses a dark interface by default to keep the experience calm and readable.

## What is still unfinished

- The data is mock content, so this is a UI prototype rather than a connected operations system.
- The action states are local to the page and do not persist after refresh.
- The live metric is a visual countdown and not connected to a real backend feed.
- The Hindi copy is intentionally simple, but it could be tightened further by a native speaker.

## What I would build next

- Connect the dashboard to real task, alert, and metric data.
- Add persistent state so approved or held items stay updated after refresh.
- Introduce filtering and sorting for different teams or priorities.
- Add a small data history view so the user can see how issues changed over time.
- Refine the mobile experience more fully if this is ever used outside of tablet and desktop.

## Notes on the implementation

The UI is built as a single-page static dashboard using HTML, a small amount of JavaScript, and Tailwind for styling. The main complexity is in keeping the language switch, keyboard navigation, action state, and low-bandwidth mode all in sync without creating a lot of duplicated logic.

## AI use log

- GitHub Copilot (VS Code assistant) — used to draft the dashboard structure, refine the copy, and help document the implementation.
- Python local server — used to preview the page locally in the browser.
- Browser preview — used to verify the layout and interactions visually.