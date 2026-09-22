# Physics & Data Analysis Projects

Python scripts written during my BSc Physics (First-Class Honours), University of Manchester,
kept here as a verifiable record of coding style and applied statistical methods.

## Contents

**`atomic.py`** — PHYS10362, Assignment 1
Models a two-isotope atomic decay system: a decaying "type-A" population alongside
an oscillating "type-B" population. Takes validated user input for half-life and
oscillation frequency, computes the combined decay/oscillation numerically with
NumPy, and identifies the last point at which the fraction crosses a user-defined
threshold. Plots the result with Matplotlib.

**`doppler.py`** — PHYS10362, Assignment 2
Detects an exoplanet from radial-velocity (Doppler shift) data on its host star.
Reads and cleans multiple raw datasets (removing non-numeric rows and >3σ outliers),
then fits a sinusoidal orbital model to the cleaned data by minimising chi-squared
with `scipy.optimize.fmin`. A second filtering pass removes remaining outliers
against the fitted curve before refitting. Estimates parameter uncertainties from
the Δχ² = 1 method, propagates these into the planet's mass and orbital separation,
and produces a four-panel figure (fit, residuals, χ² contour, results summary).

## Notes
Both scripts were written as timed, individually graded coursework assignments
rather than open-ended personal projects. Kept here as evidence of applied
statistical modelling (curve fitting, outlier rejection, uncertainty propagation)
and coding practice (input validation, docstrings, modular functions) — not as
an actively maintained codebase.
