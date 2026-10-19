# Pools & Fluxes

A Stella-style stock-and-flow modeler for teaching dynamical systems in ecosystem ecology. Students draw pools, fluxes, converters and connectors, type rate equations, and run coupled ordinary differential equations in the browser.

The whole tool is one file, `pools_and_fluxes.html`. Open it in any modern browser; it needs no install and no server, and works offline once its two web fonts have loaded (it falls back to system fonts without them).

## What it does

- **Diagram editor:** pools (stocks), fluxes (flows, with clouds for "outside the model"), converters, and connectors that carry information. As in Stella, an equation may use only quantities that have a connector into it, and the page says which connector is missing.
- **Equations:** `+ - * / ^`, `exp ln log10 sqrt abs min max sin cos mod int round`, `IF ... THEN ... ELSE`, `TIME`, `DT`, `STEP`, `RAMP`, `PULSE`. Spaces in names become underscores.
- **Solver:** Euler or Runge–Kutta 4, with non-negative pools and one-way fluxes.
- **Predict, then run:** results stay hidden until the student presses Run, and hide again after any change to the model, so students choose what to plot and predict before they see the outcome. "Rerun on every edit" turns on live updating.
- **Results:** graph against time or one variable against another, a pinned run for comparison, a table, the model written out as `d(pool)/dt = inflows − outflows`, CSV export, and Copy graph (a picture with a legend).
- **Sharing:** Save and Open a .json model file, or Copy model and paste it back on the page.

## Built-in examples

1. Soil carbon: one pool with constant input and first-order decay.
2. Plant and soil carbon: saturating GPP, respiration, litterfall, decomposition, and NEP.
3. Hares and lynx: Lotka–Volterra predator and prey (Euler spirals outward; RK4 closes the loop).
4. Leaf decomposition, carbon and nitrogen: microbes take bites of detritus; each bite's N surplus or shortfall sets gross mineralization or immobilization, so mineral N falls (net immobilization) and then rises (net mineralization) as detritus C:N drops past the critical C:N.
