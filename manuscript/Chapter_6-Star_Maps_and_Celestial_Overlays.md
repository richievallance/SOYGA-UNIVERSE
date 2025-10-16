You’re right—my bad earlier. Here’s a brand-new, fully expanded Chapter 6 that fits naturally after your foundations and before your later material. I’ve made it practical Chapter 6 – Star Maps & Celestial Overlays

6.1 Purpose

This chapter turns theory into sky. It specifies how the thirty-two Soyga tables map onto the celestial sphere, how to build overlays that line up with modern star catalogues, and how those overlays generate the “starmap” imagery used throughout this edition and in the USC simulation.


---

6.2 Coordinate Framework

Reference frame: Ecliptic coordinates (λ longitude, β latitude).

Epoch: J2000.0 (precession handled in §6.8).

Division: 32 sectors × 11.25° = 360°.

Table → sector: Table n covers λ ∈ [11.25°·(n−1), 11.25°·n).

Latitude band: Primary overlays use |β| ≤ 9° (zodiacal band) with optional extensions to ±23.44° (solar limit).



---

6.3 Projection & Grids

Planar quick-view: Equirectangular (λ horizontal, β vertical).

Precision plate: Lambert azimuthal equal-area, centred per quarter (Tables 1–8, 9–16, 17–24, 25–32).

Polar detail: North/South stereographic for high-latitude annotations.
Each overlay carries a 32-spoke sector grid (11.25° ticks) plus φ-scaled radius rings (r₀·φ⁰ … r₀·φ⁵) to visualise the growth law.



---

6.4 Sector Register (quick index)

Tables	Longitudes	Seasonal arc	Cardinal

1–8	0°–90°	Vernal ascent	8 ≈ 90°
9–16	90°–180°	Summer apex	16 ≈ 180°
17–24	180°–270°	Autumn descent	24 ≈ 270°
25–32	270°–360°	Winter return	32 ≈ 360°/0°


Use this as your “plate list” when exporting images (e.g., Plate 6.3: Tables 9–16).


---

6.5 Overlay Recipe (tool-agnostic)

Inputs: a) star background (black), b) catalogue stars (white dots sized by magnitude), c) sector grid (gold), d) Soyga frequency heatmap (amber/blue), e) labels.

1. Canvas: 4096×2048 px equirectangular, 300 dpi.


2. Sectors: draw 32 rays at λ = 0, 11.25, 22.5… 348.75°.


3. Rings: r = r₀·φ⁰…φ⁵ (use thin lines at 5–10% opacity).


4. Stars: plot to mag 6.0 (size ∝ 10^(−0.2·mag)).


5. Heatmap: for each table matrix, normalise letter counts; map vowels→warm, consonants→cool (alpha 0.35).


6. Labels: put table numbers just inside each sector; add equinox/solstice markers at 90°,180°,270°,360°.



Free tools that work well: Photopea (browser), Inkscape (SVG precision), GIMP (raster compositing).


---

6.6 Bright-Star Landmarks (J2000 ecliptic longitudes, rounded)

Star	Constellation	λ (°)	Use in plates

Aldebaran (α Tau)	Taurus	~70	Sector 7
Regulus (α Leo)	Leo	~152	Sector 14
Spica (α Vir)	Virgo	~205	Sector 19
Antares (α Sco)	Scorpius	~249	Sector 23
Fomalhaut (α PsA)	Ps. Austrinus	~346	Sector 31–32
These serve as “pegs” for quick visual registration when you sanity-check sector boundaries by eye.			



---

6.7 Planetary Paths (qualitative overlays)

Ecliptic band: plot ±5° guide to cover typical planetary latitudes.

Venus 8:13 rhythm: mark every 13 years on the λ-axis; petals land near φ² spacing in successive sectors.

Jupiter 12-year cadence: star every 30°; highlight where it crosses sector spokes.


These paths aren’t for ephemeris accuracy here; they’re didactic curves that make the harmonic cadence legible on static plates.


---

6.8 Precession & Dating

If you compare historical charts:

Convert historical RA/Dec to J2000 using a standard precession model (IAU 2006/2000A).

For rough visual work, a 50.3″/yr shift (~0.014°/yr) is a quick sanity check.

Note the epoch on every plate (e.g., “Overlay rendered at J2000; historical stars precessed from 1600.0”).



---

6.9 Data Packs (repo layout)

/overlays/
  base_starmap_4096x2048.png
  grid_32_sectors_phi_rings.svg
  soyga_heatmap_tables_1-32.png
  plate_6.1_tables_1-8.png
  plate_6.2_tables_9-16.png
  plate_6.3_tables_17-24.png
  plate_6.4_tables_25-32.png

/data/astro/
  bright_stars_j2000.csv        # name, λ_deg, β_deg, mag
  planetary_guides.csv          # schematic path samples
  sector_register.csv           # table, λ_min, λ_max

Keep SVG for the grid so you can scale without blur; composite as PNG for the final plates.


---

6.10 Repro Steps (manual, no coding)

1. Open grid_32_sectors_phi_rings.svg in Inkscape → export PNG.


2. In Photopea (or GIMP), stack layers: base_starmap → stars → grid → heatmap → labels.


3. Set heatmap layer to Multiply or Overlay at ~35% opacity.


4. Export the four quarter-plates (Tables 1–8, 9–16, 17–24, 25–32).


5. Sanity-check Aldebaran/Regulus/Spica/Antares/Fomalhaut against the correct sectors.


6. Save final plates to /overlays/ and list them in your README.

---

6.11 Reading the Plates

Brightness lobes that repeat every 8 sectors = π/4 rhythm (seasonal quarters).

Spiral drift of maxima across consecutive tables = φ-growth in radius.

Hot bands aligned with planetary guides = mnemonic encoding of the visible sky.
Interpretation remains conservative: the overlays demonstrate harmonic correspondence, not astrological causation.


---

6.12 Conclusion

The star-map overlays make Soyga’s celestial logic visible at a glance. They align the 32-sector lattice with the ecliptic, expose seasonal quartering, and provide fixed landmarks for verification. These same plates serve as the input textures for the USC renderer, so the book and the simulation share one sky.

---
🔗 Navigation

[⬅️ Previous Chapter](05_Chapter_3-Table_Structures.md) | [Next Chapter ➡️](07_Chapter_5-Appendices_and_Data.md)

---

© 2025 Richard Steven Vallance. All Rights Reserved.
Licensed under CC BY-NC-ND 4.0.

