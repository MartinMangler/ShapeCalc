# ShapeCalc

**ShapeCalc** is an Excel-based tool for estimating 3D crystal shape from 2D crystal outline measurements in thin sections. It is designed to support robust **crystal size distribution (CSD)** analysis in geological and volcanological studies, but is equally applicable for quantifying the 3D shape of any approximately cuboid particles based on 2D data.

---

## Overview

ShapeCalc enables researchers to **estimate 3D crystal shape** (expressed as the short : intermediate : long dimension ratio, or S:I:L) from 2D width-length (w/l) measurements commonly obtained from thin section images using tools such as ImageJ.

- Input 2D width and length data are compared to a library of **2618 model w/l distributions** representing shapes from **1:1:1 to 1:20:20**, generated via 20,000 random section simulations per model.
- ShapeCalc determines the best 3D shape estimate by minimizing the misfit between sample and model distributions.
- Results include classical uncertainty estimates, enabling more informed interpretation of projection-based shape estimates.
- Outputs can be directly used in *CSDCorrections* (Higgins, 2000), providing a fully consistent pipeline from measurement to CSD analysis.

ShapeCalc is designed as a direct replacement for older tools such as CSDslice (Morgan & Jerram, 2005), which can yield erroneous results in natural samples with multiple crystal populations and lacks uncertainty estimates (see analysis in Mangler et al., 2022).
Unlike these earlier approaches, ShapeCalc uses a library of over 2500 simulated shapes and includes statistical error estimates, enabling more accurate and consistent 3D shape reconstruction from 2D crystal measurements.

---

## Key Features

- **Broad shape range:** Resolve >2500 unique cuboid morphologies from S:I:L = 1:1:1 to 1:1:20  
- **Reliable shape estimation:** Incorporates statistical uncertainty in 3D shape projections from 2D sections  
- **Consistent CSD analysis:** Shares the same underlying algorithm as *CSDCorrections*, allowing end-to-end analytical consistency  

Whether you are aiming to **calculate 3D crystal shape**, **convert 2D measurements into 3D aspect ratios**, or **determine crystal geometry from thin-section data**, ShapeCalc offers a transparent and replicable workflow grounded in peer-reviewed methodology.

---

## How to Use

1. Extract 2D width and length measurements from images of crystal intersections — **≥200 crystals** is recommended for statistical robustness (see Mangler et al., 2022). *Tip: Use the "Fit Ellipse" tool in ImageJ.*
2. Open the Excel file  
3. Paste your measurements into the input columns  
4. ShapeCalc will automatically compute the most likely 3D aspect ratio, including associated uncertainties  

Detailed explanations of the binning procedure and statistical approach, as well as a comparison with CSDslice are available in the documentation.

---

## Files Included

- [ShapeCalc_v1.0.xlsx](https://github.com/MartinMangler/ShapeCalc/raw/refs/heads/main/Shapecalc_v1.0.xlsx) — Excel tool for estimating 3D shape from 2D outlines  
- [ShapeCalc_documentation](./ShapeCalc_documentation.pdf) — Methodological details and comparison to CSDslice
- [LICENSE.md](./LICENSE) — License information
- [README.md](./README.md) — This file  

---

## Citation

If you use ShapeCalc in your work, please cite:

> **Mangler, M.F., Humphreys, M.C.S., Wadsworth, F.B., Iveson, A.A., Higgins, M.** (2022).  
> Variation of plagioclase shape with size in intermediate magmas: a window into incipient plagioclase crystallisation.  
> *Contributions to Mineralogy and Petrology*, **177**, 64.  
> [https://doi.org/10.1007/s00410-022-01922-9](https://doi.org/10.1007/s00410-022-01922-9)

---

## References

- Mangler et al. (2022). Variation of plagioclase shape with size in intermediate magmas, *Contrib Mineral Petrol*, 177, 64.  
- Higgins, M.D. (2000). Measurement of Crystal Size Distributions, *Am Mineral*, 85, 1105–1116.  
- Morgan, D.J. & Jerram, D.A. (2006). On estimating crystal shape for crystal size distribution analysis, *J Volcanol Geotherm Res*, 154, 1–2.

---

## Author

Martin Mangler  
Lecturer in Applied Geoscience  
University of Southampton  
M.F.Mangler@soton.ac.uk

---

## License

This tool is licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.
See the [LICENSE](./LICENSE) file for details.

