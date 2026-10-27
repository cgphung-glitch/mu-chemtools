# Circuit Lab · Draw & Measure

A circuit board you draw on: place wire, resistors, batteries, capacitors, inductors, voltmeters,
ammeters and switches on a grid, set their values, and read the meters live when the circuit is
closed.

**Run it:** open [index.html](index.html) in any browser. It is one self-contained file — no build
step, no dependencies, no network access, works offline and on a phone. Dark/light is the button in
the header and is remembered.

## What it does

- **Parts palette** — wire, resistor, battery, capacitor, inductor, voltmeter, ammeter and switch,
  plus a current-direction arrow. Rotate, delete or undo a part, and click any part to edit it in
  the inspector.
- **Drawing mode** shows only the circuit elements: no meter readings and no current arrows, so you
  can lay out and label a diagram.
- **Simulation mode** closes the circuit: the voltmeter and ammeter show their readings and the
  current arrows appear.
- **Ideal / realistic** toggle for the simulation. Realistic gives each element 1–2 % of internal
  resistance, so the meters no longer read the textbook values.
- **Values you set:** a battery's voltage, a resistor's resistance and the current. Voltmeters read
  the potential difference across the part they are placed over; ammeters read the current through
  the branch they sit in.
- **Board size** is adjustable — add or remove rows and columns, and the grid rescales.
- **Export the drawing** as an image, and give any element a **custom label**.
- Every change is kept in the browser, so a board survives a reload.

## Notes

- Saved under the `circuit-lab-board-v1` localStorage key, with the theme at `circuit-lab-theme`.
- Listed in the site hub (`index.html` at the repository root) as **Circuit Diagram Builder**.
- Previously served from `physics/circuit-diagram.html`; that path now redirects here.
