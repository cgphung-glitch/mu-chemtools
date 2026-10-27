# Work & Power Lab · Cart on an Incline

A cart on an inclined board, pulled up the board by a weight hanging over a pulley. Release the
cart, time the run, and then work out the force, work, power and the energy bookkeeping.

**Run it:** open [index.html](index.html) in any browser. It is one self-contained file — no build
step, no dependencies, works offline and on a phone. Dark/light is the button in the header and is
remembered.

**Student version:** [student.html](student.html) is the same rig without the live speed and
model-acceleration readouts and without the post-lab analysis — see *Student version* below.

## What it does

- **The rig:** a board on a stand with a pulley at the raised end, a cart on the board and a string
  over the pulley to a hanging weight. Its length and raised-end height fix sinθ = H/L, and the
  distance the cart travels is set by a draggable stop mark.
- **Nine trials** — three mass groups × three trials, exactly as the experiment asks, with the
  trials auto-advancing once a mass group is full.
- **Two ways to time it:** **photo-gate** or **stopwatch**, where you tap Stop and your reaction time
  becomes part of the reading. Every reading — either mode — carries about **±0.5 %** of measurement
  scatter, so repeated trials of one mass come out close but not identical. Letting the cart run off
  the end without stopping it voids the trial.
- **The forces on the cart can be drawn** — the pull from the hanging weight, the cart's weight
  along the slope and, in Realistic mode, rolling resistance — so it is visible why the cart only
  breaks free once the hanging weight beats m·g·sinθ + f. The arrows are **off by default** and the
  switch in Model & timing turns them on; your choice is remembered.
- **Record sheet** reproducing the experiment's data table: mass added, total mass, three trial
  times and their average, plus the hanger mass, distance travelled, rise and cart mass.
- **Post-lab analysis** per mass with the arithmetic shown: v<sub>avg</sub> = d/t̄, a = 2d/t̄²,
  v<sub>f</sub> = 2d/t̄, F = m g, W = F d, P = W/t, W<sub>cons</sub> = ΔPE = m<sub>cart</sub> g h,
  ΔKE = ½m<sub>cart</sub>v<sub>f</sub>², and whether the system comes out conservative — including
  splitting the leftover energy into friction and the stopwatch's timing error. It is **collapsed by
  default**; the **Show analysis** button in its header opens it, and that choice is remembered.
- **Ideal / realistic** toggle with an adjustable rolling-resistance coefficient, and a g input.
- **Layout:** the page fills the whole window at every size. On a laptop or desktop the board sits
  in the left column with the procedure under it,
  while the Incline & cart, Hanger & weights and Model & timing panels stack down the right; below
  both columns the record sheet and analysis run full width. On a tablet the incline and hanger
  panels sit side by side with the model panel across the width beneath them, and a phone stacks
  everything in one column with the board pinned to the top while you scroll.

## Student version

[student.html](student.html) is the same lab prepared for handing to students:

- the animation panel shows only **Time** and **Position** — no live **Speed** and no **Model a**
  acceleration readout;
- the **Post-lab analysis** card is not in the file at all, so no worked answers are on the page
  (the analysis code behind it was removed too, not just hidden);
- everything else is unchanged: the rig, the nine trials, both timing modes, the ± 0.5 % scatter,
  the record sheet and the Ideal/Realistic models.

It saves under its own key, `workpower-student-v1` (theme: `workpower-student-theme`), so the two
versions can sit side by side without sharing trials.

## Notes

- Saved under the `workpower-lab-v1` localStorage key, with the theme at `workpower-lab-theme`.
- Models **PHY1510 Exp 06a – Work and Power**.
- Listed in the site hub (`index.html` at the repository root) as **Work & Power Lab (incline)**.
- Previously served from `physics/work-power-lab.html`; that path now redirects here.
