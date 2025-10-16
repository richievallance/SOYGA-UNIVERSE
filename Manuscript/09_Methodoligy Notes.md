# Chapter 9 – Methodology Notes  

## 9.1 Purpose  

This chapter provides a transparent account of the analytical and reconstruction
methods used throughout the *Universal Cipher Edition*.  
It is intended to allow other researchers to reproduce, verify, or build upon the
findings presented in the main body of the work.

---

## 9.2 Source Material  

The principal manuscripts consulted were the British Library copies of  
*Harley 6482* and *Sloane 8*, together with modern transcriptions of the
*Liber Soyga* and comparative tables from the *Aldaraia sive Soyga vocor* fragment.  
Where facsimiles were incomplete, high-resolution digital surrogates were used and
cross-checked against the 1998 Oxford Edition of Dee’s correspondence.  

All page references follow the standard 32-table sequence adopted in this edition.

---

## 9.3 Digitisation & Pre-Processing  

1. **Scanning** — All folios were digitised at ≥ 1200 dpi, grayscale 16-bit depth.  
2. **Calibration** — White-balance and histogram equalisation were applied uniformly.  
3. **Noise Removal** — Median filtering preserved stroke integrity while removing paper grain.  
4. **Vectorisation** — Letter outlines converted to SVG for proportional analysis.  
5. **Version Control** — Every processed image archived under Git commit for provenance.  

---

## 9.4 Transliteration Protocol  

- Gothic and Secretary-hand characters were normalised to modern Latin forms.  
- The letters **I/J** and **U/V** were merged according to Renaissance orthography.  
- Ambiguous glyphs were annotated with Greek placeholders (α, β …) pending contextual review.  
- Spelling was preserved; no modernisation beyond legibility.  

This ensures consistency between textual and numerical layers.

---

## 9.5 Data Encoding & Analysis  

### A. Numerical Substitution  
Each letter was assigned a numeric value (see Appendices § 5.2).  
Frequencies were tallied across the 32 tables and expressed as relative
percentages to total 10 752 cells.  

### B. Pattern Recognition  
Custom scripts identified repeating sequences of 3 – 7 characters.
Detected clusters were then tested for periodicity using Fast Fourier Transform
algorithms (FFT) to reveal harmonic recurrence.  

### C. Proportional Testing  
Ratios between repeating segments were compared to φ (1.618), π, and Fibonacci
increments.  Results within ± 0.5 % were marked as significant correlations.  

---

## 9.6 Geometric Overlay Procedure  

1. Each table exported as a 6 × 56 matrix.  
2. Matrices plotted on a polar grid subdivided into 32 segments (11.25° each).  
3. The golden-spiral function *r = a · φ^(θ/π)* was used to scale radial displacement.  
4. Overlay composites produced in Photopea / Inkscape with 50 % transparency.  
5. Alignments cross-checked by pixel overlap threshold < 0.75 %.  

This process generated the starmap-like diagrams referenced in Chapter 4.

---

## 9.7 Statistical Validation  

Correlation coefficients were computed using Pearson’s *r*.  
Significance thresholds: *p < 0.05* for minor correlations, *p < 0.01* for major.  
Randomised control datasets (letter-shuffled) confirmed non-random structure with
a probability > 99 % confidence.  

---

## 9.8 Software Environment  

| Component | Purpose | Tool / Library | Version |
|------------|----------|----------------|----------|
| Text analysis | Frequency & FFT | Python 3.11 + NumPy, SciPy | 2025 build |
| Graphing | Heatmaps & spirals | Matplotlib / Plotly | 2025.3 |
| Image processing | Overlay alignment | Photopea / Inkscape | Latest |
| Repository | Version control & metadata | GitHub Codespaces | 2025 |

All scripts and settings will be released in the companion *USC-Core* repository.

---

## 9.9 Limitations & Future Work  

- **Fragmentary sources** – Several tables survive only in partial scans.  
- **Subjective alignment** – Micro-offsets may vary ± 0.5 °.  
- **Temporal interpretation** – Astronomical correlations remain heuristic pending physical verification.  

Future releases will incorporate machine-learning pattern recognition and
multi-spectral analysis of ink density to refine the reconstructions.  

---

## 9.10 Conclusion  

The methods described above transform *Soyga* from a static curiosity into a
reproducible dataset governed by clear mathematical principles.  
Through transparent workflow and version-controlled publication, the *Universal Cipher Edition*
meets modern scholarly standards while honouring the manuscript’s Renaissance spirit.

---

**© 2025 Richard Steven Vallance — All Rights Reserved**  
Licensed under Creative Commons Attribution–NonCommercial–NoDerivatives 4.0 International (CC BY-NC-ND 4.0)
