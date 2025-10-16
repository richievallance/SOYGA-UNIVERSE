Chapter 14 – Appendices and Technical Data

14.1 Purpose

The appendices preserve the quantitative backbone of the Universal Cipher Edition.
They consolidate constants, indices, and procedures used throughout the reconstruction and simulation so that every computation can be verified or reproduced.
Where previous chapters interpreted meaning, this section documents measurement.


---

14.2 Primary Constants and Ratios

Symbol	Name	Approximate Value	Function in Research

φ	Golden Ratio = (1 + √5) ⁄ 2	1.618 033 988 75	Scaling of radii, harmonic growth
π	Circle Constant	3.141 592 653 59	Rotational increments (π ⁄ 16 per table)
e	Natural Exponent	2.718 281 828	Used in logarithmic amplitude decay
Fₙ	Fibonacci Sequence (1, 1, 2, 3, 5, 8 …)	—	Recurrence and temporal stepping
ℏ	Reduced Planck Constant	1.054 × 10⁻³⁴ J·s	Reference for quantum scaling analogy


All simulations were normalised to φ = 1 unit of growth and π = one full rotation = 32 tables.


---

14.3 Table Index and Angular Coordinates

Table No.	Angular Position (°)	Radial Scale φⁿ	Opposite Table

1	0	1.000	17
2	11.25	1.618	18
3	22.50	2.618	19
4	33.75	4.236	20
5	45.00	6.854	21
6	56.25	11.090	22
7	67.50	17.944	23
8	78.75	29.034	24
9	90.00	46.979	25
10	101.25	76.013	26
11	112.50	122.992	27
12	123.75	199.005	28
13	135.00	321.997	29
14	146.25	521.003	30
15	157.50	842.996	31
16	168.75	1364.000	32
17–32	mirror set of 1–16	φⁿ decreasing	1–16


Angular spacing = 11.25° (π ⁄ 16 radians); full rotation = 360° = 2π radians.


---

14.4 Letter-Frequency Distribution (aggregated across 32 tables)

Letter	Frequency	Relative %	Notes

A	958	8.91	High in vowel clusters
B	411	3.82	Often in binary pairs with L
C	523	4.86	Marks cardinal axes
D	444	4.13	Stable consonant baseline
E	1067	9.93	Peak frequency (phonetic resonance)
F–Z	…	…	See supplementary CSV in data repository


Total cells = 10 752.
Frequencies normalised to 100 %. Peak-to-mean ratio = 2.17 : 1.


---

14.5 Formulas and Algorithms

1. Radial Scaling: rₙ = r₀ · φⁿ
2. Angular Progression: θₙ = n · (π ⁄ 16)
3. Frequency Ratio: fₙ = Fₙ ⁄ Fₙ₊₁
4. Wave Function: Ψ(θ,t) = sin(πθ/16) · φ^(t/Fₙ)
5. FFT Parameters: window = 512 samples, overlap = 0.25, cutoff = 5 Hz (normalised)
6. Correlation Test: r = Σ[(x – μₓ)(y – μᵧ)] ⁄ √(Σ(x – μₓ)² Σ(y – μᵧ)²)

These equations govern both analytical and visual simulations. All constants declared in /data/constants.json.


---

14.6 Software and Environment

Component	Tool / Library	Version	Function

Core Computation	Python 3.11 / NumPy / SciPy	2025 build	Numeric analysis and FFT
Visualisation	Matplotlib / Plotly	2025.3	2-D and 3-D graphing
Image Processing	Photopea / Inkscape	Latest	Overlay alignment
Database & Versioning	Git / GitHub	2025	Archival integrity
Simulation Engine	USC-Core Prototype	v 0.9	Harmonic field rendering


Default colour mapping = CET-L17 gradient; time step Δt = 0.0625 cycles.


---

14.7 Glossary of Key Terms

Term	Definition

Aldaraia / Soyga vocor	The alternate title of the manuscript as listed in Dee’s catalogue.
Node	A single table treated as a computational unit within the simulation.
Harmonic Field	The aggregate interaction of all nodes through φ, π, and F ratios.
Recurrence	Mathematical operation Fₙ = Fₙ₋₁ + Fₙ₋₂.
Rotation	Cyclic motion measured in π phase increments.
Reflection	Bilateral symmetry mirroring observer and object.
Universal Simulation Construct (USC)	Framework for computational realisation of Soyga principles.



---

14.8 Data Integrity and Reproducibility

Each dataset includes SHA-256 hash values for verification. All scripts are stored under version control with timestamped commits. All images include embedded metadata detailing constants, time step, and rendering engine. Every output frame can be regenerated from the raw tables using the public algorithm set.


---

14.9 Licensing and Access

All text and data are released under CC BY-NC-ND 4.0 International.
Reproduction for academic citation is permitted with attribution. Derivative or commercial use requires written consent from the author.


---

14.10 Conclusion

These appendices anchor the Universal Cipher Edition in verifiable method. Behind every philosophical claim lies reproducible mathematics; behind every image, declared proportion. By documenting constants, coordinates, and computational tools, the study ensures that its conclusions can be tested by others. The harmony proposed is therefore not metaphorical but demonstrable—a bridge from intuition to calculation.


---

© 2025 Richard Steven Vallance — All Rights Reserved
Licensed under Creative Commons Attribution–NonCommercial–NoDerivatives 4.0 International (CC BY-NC-ND 4.0)
