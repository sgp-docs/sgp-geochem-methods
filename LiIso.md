#### Lithium Isotopes

**Commonly cited method papers**

- Moriguti and Nakamura 1998 https://doi.org/10.1016/S0009-2541(97)00163-0
- James and Palmer 2000 http://dx.doi.org/10.1016/S0009-2541(99)00217-X
- Rudnick et al. 2004 https://doi.org/10.1016/j.chemgeo.2004.08.008
- Pogge von Strandmann et al. 2011 https://doi.org/10.1016/j.gca.2011.06.026 (+other Pogge von Strandmann papers, and refs therein - carbonates)
- Li et al. 2022 https://doi.org/10.1016/j.sab.2021.106348 (see for summary diagram of steps)

**Notes**

Digestion and pre-treatment for shales is a total acid digest with HF/HNO3/HClO4 followed by HNO3/HCl, in one case perchloric acid is used "as needed".

To target the carbonate fraction, there is some variability in approach including dilute HCl treatment, 1 M sodium acetate buffered to pH 5 with acetic acid, or leach with ammonium acetate followed by a sequential leach in 0.05M HCl. See papers by Pogge von Strandmann et al. for discussion/evaluation of different approaches.

Li et al. 2022 provide a summary of chromatographic methods. Most studies in SGP use a two-column cation exchange procedure, with AG50W-X12 resin, one study follows a three-step procedure.

The **reference standard** for lithium isotopes is LSVEC.

| analyte(s)     | count_res | code                         | translation                                                                                   | ana_method(s) |
| -------------- | --------- | ---------------------------- | --------------------------------------------------------------------------------------------- | ------------- |
| DELTA_Li7      | 93        | MA3b_3CE                     | HF/HNO3/HClO4, HCl/HNO3, three cation exchange chromatography                                 | ICP:MS-MC     |
| DELTA_Li7      | 34        | MA3b_2CE                     | HF/HNO3/HClO4, HCl/HNO3, two-step cation exchange chromatography (AG50W-X12 resin)            | ICP:MS-MC     |
| DELTA_Li7_CARB | 78        | HCl(0.1N)\_2CE               | 0.1N HCl, two-stage cation exchange chromatography (AG50W-X12 resin)                          | ICP:MS-MC     |
| DELTA_Li7_CARB | 58        | NH4Ac(1M)\_HCl(0.05NSeq)\_CE | 1M ammonium acetate, 0.05N HCl in 4hr/2hr/10min seq. steps, cation exchange (AG50W-X12 resin) | ICP:MS-MC     |
| DELTA_Li7_CARB | 48        | NaOAc(1M)\_2CE               | 1M sodium acetate (AcOH buffered), two stage cation exchange chromatography (AG50W-X12 resin) | ICP:MS-MC     |
| DELTA_Li7_CARB | 3         | MeOH_2CE                     | Methanol/ultrasonic cleaning, two-stage cation exchange chromatography (AG50W-X12 resin)      | ICP:MS-MC     |
