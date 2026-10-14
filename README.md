# Cosmology Toolbox

Distances, ages and the CMB, to more significant figures than the data justify.

A cosmology calculator plus a few other tools you end up needing anyway. It's a single HTML file with no dependencies and no build step, and it runs entirely in your browser. Nothing gets sent anywhere.

**[Open it](https://allangabrielsch.github.io/CosmologyToolbox/)**, or download `index.html` and double-click it. It works offline, which is handy for observing runs.

## What's in it

**Cosmology calculator**
- Any FLRW model: H₀, Ωm, ΩΛ (flat or not), radiation from T_CMB and N_eff, and dark energy with w(a) = w₀ + wₐ(1 − a)
- Presets: Planck 2018, Planck 2015, WMAP9, round numbers, SH0ES H₀, evolving dark energy, Einstein–de Sitter, Milne and Hubble (1929)
- Today: age, Hubble time and distance, q₀, onset of acceleration, matter–DE and matter–radiation equality, and the particle and event horizons
- At redshift z: lookback time, age, D_C, D_M, D_A, D_L, distance modulus, kpc/″ (proper and comoving), comoving volume, H(z), Ωm(z), ρ_crit(z) and T_CMB(z)
- Works backwards too. Give it a lookback time, an age, D_C, D_L, D_A or μ and it finds z. D_A has two solutions, and the calculator tells you about both.
- Plots distances or times against z, copies the results as tab-separated text, and keeps the parameters in the URL so you can share a link
- Flags universes with no Big Bang, a Big Crunch, or a Big Rip (and gives the countdown)

**Lensing (two redshifts)**
- D_d, D_s, D_ds, the time-delay distance D_Δt, the time-delay scale, Σ_crit, and Einstein radii for an SIS (from σ_v) and for a point mass

**H₀ and the Hubble tension**
- Pick two measurements, early-universe or late-universe, or type your own. You get the tension in σ, a p-value, a verdict, and a plot.
- H₀ unit conversions, a Hubble's-law calculator, and a weighted least-squares fit of v = H₀d to your own data

**CMB sky simulator**
- A Gaussian random field on a flat patch (5° to 40°), with a choice of telescope beam from "perfect" down to COBE
- The acoustic peak positions come from the real physics: sound horizon r_s(z\*), D_M(z\*), θ\* and the baryon loading R\*. The peak heights come from a toy model tuned by eye to Planck.
- Plots the power spectrum measured from the map you just made, with cosmic-variance error bars. You can also click a pixel to read its temperature, and save the map as a PNG.
- **This is a toy.** It's good for intuition, teaching and slides. For anything you publish, use [CAMB](https://camb.info) or [CLASS](https://lesgourg.github.io/class_public/class.html).

**Redshift and spectral lines**
- z ↔ a ↔ v (relativistic Doppler), time dilation, Tolman dimming, and where the usual lines (Lyα to H I 21 cm) land in the spectrum

**Unit systems**
- A global selector at the top switches every result between: Cosmologist (Mpc, Gyr, M☉), Simulator (h⁻¹ Mpc, h⁻¹ M☉), SI, cgs, Natural units (ħ = c = k_B = 1, so distances come out in GeV⁻¹), Imperial (furlongs, fortnights, stone, Rankine), American and Star Wars.
  - American: handegg fields (do not call it football), parking spaces, Big Macs, drive-thru waits, presidential terms (assuming each runs the full four years), oil barrels, inches and °F.
  - Star Wars: Kessel Runs, Death Stars and Wookiees.
- Input boxes (velocities, distances, masses, the calculator's "Given" value) and outputs (tables, plots, CMB temperatures, wavelengths) all follow the selected system. H₀ inputs stay in km/s/Mpc, with the converted value shown next to them.
- In the silly systems, the third column always shows the normal cosmologist value, so nothing is lost.

**Units and constants**
- Length, time, mass and energy conversions, including foe, the unit for supernova energies
- CODATA 2018 and IAU constants. Click a row to copy it.

## Accuracy

Distances and ages come from direct numerical integration, Simpson's rule in ln a. They agree with astropy to about 10⁻⁴ for Planck 2018 (t₀ = 13.786 Gyr, D_C(z=1) = 3395.5 Mpc). Neutrinos are treated as massless radiation, so fold any neutrino mass into Ωm. The CMB numbers use fitting formulas: z\* from Hu & Sugiyama (1996) and r_d from Aubourg et al. (2015). Expect about 0.2% accuracy there.

## References

The page uses these. If it saves you time, cite them, not the page.

- Hogg (1999), *Distance measures in cosmology*, [astro-ph/9905116](https://arxiv.org/abs/astro-ph/9905116)
- Hu & Sugiyama (1996), ApJ 471, 542: z\* fitting formula
- Aubourg et al. (2015), PRD 92, 123516: r_d fitting formula
- Caldwell, Kamionkowski & Weinberg (2003), PRL 91, 071301: Big Rip
- Planck Collaboration (2020), A&A 641, A6
- H₀ values: Riess et al. 2022, Freedman et al. 2021, Wong et al. 2020, Birrer et al. 2020, Kelly et al. 2023, Pascale et al. 2025, Pesce et al. 2020, DESI Collaboration 2024
- Required reading on the tension: [xkcd 2516](https://xkcd.com/2516/)

## Features nobody asked for

There are about twenty easter eggs. Catch a shooting star for a hint, or press "Wish upon a star" if you're impatient. Referee #2, at the bottom of the page, also has comments that might help, if you can stand reading them.

## Licence

MIT. See [LICENSE](LICENSE).
