# Atwood's Machine Lab · Photogate

Two masses on either side of a pulley, connected by a light string, timed with a photogate. Fit
velocity against time to get the acceleration, then relate that acceleration to the mass difference
and to the total mass.

**Run it:** open [index.html](index.html) in any browser. It is one self-contained file — no build
step, no dependencies, works offline and on a phone. Dark/light is the button in the header and is
remembered.

## What it does

- **The apparatus:** a ring stand and clamp holding a pulley with a photogate straddling its rim,
  two masses hanging from the string and a cm ruler showing the descent. Release the masses and the
  heavier side falls while the pulley spins and the gate pulses once per spoke. The falling side is
  caught after the set travel and the rig holds that pose — pulley and all — until the next step
  (changing the masses, the model or the plan) puts it back to the start.
- **The photogate is the measurement.** Velocity is sampled once every tenth of a turn of the pulley
  — one sample per 1.60 cm of string, what the Ultra Pulley's 10-spoke groove gives — and a
  least-squares line is fitted to those points, as the *Curve Fit → Linear* step does. The slope is
  the acceleration; the fit's intercept, r² and sample count (about 28 per run) are reported.
- **The experiment's two parts are the guided plans.** *Part I* keeps the total mass at 200 g and
  moves 5 g from m₂ to m₁ each trial (100/100 → 120/80). *Part II* keeps the 10 g difference and adds
  10 g to both sides (50/60 → 90/100). Five trial slots per part, with the masses the procedure calls
  for shown greyed until you record them.
- **Both data tables are the experiment's** — trial, m₁, m₂, a, m_diff = m₁ − m₂ (kg), m_T (kg).
- **Analysis steps 1–5**, with both graphs: **a vs |Δm|** (Part I) is a straight line through the
  origin whose slope is compared against g/m_T, and **a vs m_T** (Part II) is plotted against the
  predicted curve while a·m_T is reported per trial. Step 5 writes out the combination,
  **a = |Δm|g / m_T**.
- **All five extensions are answered live:** free-body diagrams with both Newton's-second-law
  equations and the algebra that gives a = Δm g/m_T; expected versus measured trial by trial; an
  unknown mass on the left, solved from a = m₂(g − a)/(g + a) and then revealed; the tension on both
  sides; and the force the pulley feels, 2T against the total weight.
- **Ideal / realistic** toggle. Realistic adds the pulley's rotational inertia (as an equivalent
  mass) and its bearing friction, both adjustable, so the fitted acceleration comes out a few percent
  low — which is what the experiment's second extension question is about. A machine whose driving
  force is below the bearing friction correctly refuses to move.

## Layout

On a phone or tablet the page is one column and the apparatus pins under the header while you
scroll. From 900 px wide (laptop and desktop) it fills the whole window in two columns: the
apparatus on the left with the Procedure directly beneath it, and **Masses on the string** and
**Model** stacked down the right-hand side. The photogate graph, the data tables, the analysis
and the extensions run full width below both. The board is sized so the apparatus and its run
bar fit one screen height at any desktop size.

## Notes

- Saved under the `atwood-lab-v1` localStorage key, with the theme at `atwood-lab-theme`.
- Models **PHY1510 Exp 07 – Atwood's Machine**. The pulley is drawn oversized so it reads on screen,
  but its rotation and spoke rate follow a real 1-inch radius, and travel is limited to 40–60 cm
  because the masses must be able to move at least 40 cm before the falling one strikes the floor.
- Listed in the site hub (`index.html` at the repository root) as **Atwood's Machine Lab**.
- Previously served from `physics/atwood-machine.html`; that path now redirects here.
