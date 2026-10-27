# Torque Balance Lab · Meterstick Equilibrium

A 100.0 cm meterstick on a knife-edge fulcrum with masses hanging from it. Move a hanger along the
stick or move the fulcrum until the torques balance — τ = r·m·g taken about the pivot — with the
stick's own weight acting at its center of gravity.

**Run it:** open [index.html](index.html) in any browser. It is one self-contained file — no build
step, no dependencies, works offline and on a phone. Dark/light is the button in the header and is
remembered.

## What it does

- **Drag anything on the stick**, or tap it and fine-tune with a 0.1 cm slider and ±0.1 / ±1 nudges.
  Move the fulcrum the same way.
- **The cases from the experiment** are preloaded — Case 1, 2(a), 2(b), 3, 5 and 6(a)–(d) — each
  with its procedure and its own apparatus setup, plus a free-explore mode.
- **Torques about the fulcrum** are shown with the lever arms drawn on the stick and coloured by
  side. The stick is a uniform ruler, so its weight acts at its centre of gravity whenever the
  pivot is not there (Case 5).
- **"Level it"** solves whichever element that case leaves free: the position of a hanger or the
  fulcrum itself.
- **Predictions** where the experiment asks for them (2b, 6d): type your answer and *Check* reports
  how far off you are before nudging you back to the torque equation.
- **Unknown mass (Case 3)** hides one mass completely: its row and torque read `?`, the unknown
  side's total and the percent difference are withheld, and the method of moments appears once you
  balance it. *Weigh it on the lab balance* then reveals the true value.
- **Data & torques table** — every mass, position, lever arm, side and torque, both sums, the
  percent difference, and a toggle between N·m and g·cm. An optional view splits the stick into two
  segments (Case 5b) to show the same torque a second way.
- The stick mass, stick centre of gravity, hanger clamp mass and g are all editable, and everything
  is kept in the browser across reloads.

## Notes

- Saved under the `torque-lab-v1` localStorage key, with the theme at `torque-lab-theme`.
- Models **PHY1510 Exp 08 – Torques, Equilibrium, and Center of Mass**.
- Listed in the site hub (`index.html` at the repository root) as **Torque Balance Lab**.
- Previously served from `physics/torque-balance.html`; that path now redirects here.
