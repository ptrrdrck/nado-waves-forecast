# Nado Waves — Coronado forecast

A physically derived swell aperture for the three breaks on Coronado Central
Beach, rebuilt after each GFS-Wave cycle.

**Live: https://ptrrdrck.github.io/nado-waves-forecast/**

This repository is a delivery surface and nothing else. `index.html` is built
from `app/forecast.html` in the private `nado-waves` repository, which holds the
geometry, the transform and the tests, and `forecast.json` is written there by
`forecast/live.py`. `geometry.html` is drawn there from the same geometry file
the forecast reads, by `forecast/geomviz.py`, and `info.html` is built from
`app/info.html`. All three are pushed here by a workflow. **Edit them there** —
anything committed directly to this repository is overwritten by the next cycle.

## What the page shows, and what it does not

It shows how much of the offshore swell at buoy 46232 is aimed through each
break's open window — north, centre and south, which are not one beach: the west
edge of the window is the bearing to the Point Loma tip, and that bearing sweeps
as you walk the sand.

**Nothing has ever measured a wave at these three breaks.** The output is
*physically derived*, never accurate, and carries no error bar because there is
nothing to compute one against. `info.html` states what each tab is standing
on — geometry, model, calibration, observation — and two of those read *none*.

Each break's number is the offshore spectrum carried by physics to where it
breaks: refraction, bottom friction and diffraction over the seabed, shoaling
to 5 m of water, then breaking on the surveyed beach profile at the tide. It is
**not a wave height at the beach** as a surfer calls it: a significant height,
not a face height, and the transfer between them has never been fitted, because
nothing has observed these beaches.

## Why it is separate from the observation log

`nado-waves-log` serves the observer form, and that form never shows a forecast:
an observer who has seen one is not an independent witness, and a series
contaminated that way cannot judge the forecast that shaped it. Keeping the two
on separate sites keeps the forecast off the path an observer walks.

Note that GitHub Pages project sites share one origin, so this is a separation
of paths and of links, not a browser security boundary.
