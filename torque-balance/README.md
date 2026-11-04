# Torque Balance Lab · Meterstick Equilibrium

A 100.0 cm meterstick on a knife-edge fulcrum with masses hanging from it. Move a hanger along the
stick or move the fulcrum until the torques balance — τ = r·m·g taken about the pivot — with the
stick's own weight acting at its center of gravity.

**Run it:** open [index.html](index.html) in any browser. It is one self-contained file — no build
step, no dependencies, works offline and on a phone. Dark/light is the button in the header and is
remembered.

**Student version:** [student.html](student.html) is the same rig with the torque column and torque
sums taken out of the data table, which is titled **Data** — see *Student version* below.

## What it does

- **Drag anything on the stick**, or tap it and fine-tune it in the Controls card with a 0.1 cm
  slider. Move the fulcrum the same way.
- **Fine-move bar under the board.** Whenever a hanger or the fulcrum is selected, a bar sits right
  below the stick with its position and **−0.1 / +0.1 cm** buttons (plus −1 / +1 for coarse moves),
  so you can step a mass into place without scrolling to the Controls card. On a keyboard, ← and →
  move the selection by 0.1 cm and Shift + ← / → by 1 cm. Steps round to 0.1 cm and stay on the
  0–100 cm stick.
- **Each hanger is drawn as a weight with its mass written underneath** ("100 g"), outside the
  block, because the block is only as wide as the mass it represents. The role (m1, m2 …) stays on
  the block and its x position is printed below the mass. The board grows its viewBox when a heavy
  mass hangs near the end of the stick, so the labels are never clipped.
- **The cases from the experiment** are preloaded — Case 1, 2(a), 2(b), 3, 5 and 6(a)–(d) — each
  with its procedure and its own apparatus setup (pivot, stick CG, hangers), plus a free-explore
  mode. Loading a case does not change the stick's mass.
- **The fulcrum is labelled with its own position** — `x = 40.0 cm` under the knife-edge stand,
  the same way each hanger's position is printed under its mass — and it tracks the pivot as you
  drag or step it.
- **One stick, one mass:** the metre stick is **89.5 g in every case**, so the same stick hangs on
  the same fulcrum from Case 1 through Case 6(d) and the recorded torques match from case to case.
  The mass is printed on the board (`stick 89.5 g`) and shown in **Apparatus → Stick mass**, which
  is editable; a value you type applies to every case too. Case 6(d)'s opening pivot is solved from
  it, so it always lands where 6(c) balanced.
- **Torques about the fulcrum** are shown with the lever arms drawn on the stick and coloured by
  side. The stick is a uniform ruler, so its weight acts at its centre of gravity whenever the
  pivot is not there (Case 5).
- **"Level it"** solves whichever element that case leaves free: the position of a hanger or the
  fulcrum itself.
- **Predictions** where the experiment asks for them (2b, 6d): type your answer and *Check* reports
  how far off you are before nudging you back to the torque equation. The answer it compares
  against is solved from the current masses and stick mass, so it always matches what the rig
  actually does.
- **Case 6(d) opens at Case 6(c)'s balancing position**, worked out from the stick's actual mass
  rather than a figure typed in for a 150 g stick, so its opening pose really is the answer you
  just measured in 6(c) (about 43.1 cm for an 89.5 g stick, against 44.3 cm for 150 g).
- **Unknown mass (Case 3)** hides one mass completely: its row and torque read `?`, the unknown
  side's total and the percent difference are withheld, and the method of moments appears once you
  balance it. *Weigh it on the lab balance* then reveals the true value.
- **Data & torques table** — every mass, position, lever arm, side and torque, both sums, the
  percent difference, and a toggle between N·m and g·cm. An optional view splits the stick into two
  segments (Case 5b) to show the same torque a second way.
- **Export** — *Board image (PNG)* saves the animation panel exactly as it stands (2× the viewBox,
  so 2000 × 1000 px, or taller when a hanger makes the board grow) with the theme's own colours,
  text and lever arms. *All cases (CSV)* writes one sheet covering every case: one row per hanger
  and for the stick with `case_id`, `case`, `element`, `mass_g`, `x_cm`, `lever_arm_cm`, `side`,
  `torque_Nm`, `percent_difference` and `pivot_cm`, followed by each case's two Στ rows and its
  percent difference. The case you are working on exports its live values; the others export their
  starting pose, and an unrevealed unknown mass is written as `?`.
- The stick mass, stick centre of gravity, hanger clamp mass and g are all editable, and everything
  is kept in the browser across reloads.

## Layout

- On a laptop or desktop (**≥ 900 px wide**) the page fills the whole window in two columns: the
  board gets the left one and every panel — experiment case, Controls, Hangers, Data (Data &
  torques in the full build), Export, Apparatus, footer — stacks down the right. The board column is a little wider (1.35 : 1), and the
  board is sized by that column's width instead of a height cap, so it grows with the screen
  (1046 × 523 px at 1920 wide, 727 × 364 at 1366).
- The board column is sticky, so the stick stays in view while you scroll down the right-hand panels.
- Controls and Hangers sit side by side only when the right column has room (≥ 1500 px window);
  below that they stack.
- Under 900 px the app is one column in reading order, with the board sticky at the top and the
  height cap (**46 dvh**) that keeps it on screen — the phone layout is unchanged.

## Student version

[student.html](student.html) is the same lab prepared for handing to students:

- the data card is titled **Data**, not *Data & torques*, and its table records only the
  measurements — element, **m**, **x**, the lever arm **r** and which side of the fulcrum it is on;
- the **τ** column, the two **Στ** rows and the **percent difference** row are gone from the table,
  so the student works out every torque themselves; the N·m / g·cm switch went with them, since it
  only changed the torque column;
- the **Level it** solver is gone: the header icon, the chip above the board and *Level it with this
  hanger* in Controls are all removed, along with the solve routine behind them, so the only way to
  balance the stick is to work out where the hanger or the fulcrum has to go;
- everything else is unchanged: the rig, all ten cases, the lever arms on the board, the predictions,
  the unknown mass (Case 3), the segment view, the ±0.1 cm fine move and the live chips.

It also keeps the **Export** card: the PNG works exactly as in the full build, and the CSV is the
same sheet minus the torque and percent-difference columns (measurements only: `mass_g`, `x_cm`,
`lever_arm_cm`, `side`, `pivot_cm`).

The live readouts outside the table still show torque: the chips above the board (net τ and the
percent difference), the selected hanger in **Controls** and the case box. Say so if those should
be stripped as well.

It saves under its own key, `torque-student-v1` (theme: `torque-student-theme`), so the two
versions can sit side by side without sharing a setup.

## Notes

- Saved under the `torque-lab-v1` localStorage key, with the theme at `torque-lab-theme`.
  The student build uses `torque-student-v1` and `torque-student-theme`.
- Models **PHY1510 Exp 08 – Torques, Equilibrium, and Center of Mass**.
- Listed in the site hub (`index.html` at the repository root) as **Torque Balance Lab**.
- Previously served from `physics/torque-balance.html`; that path now redirects here.
