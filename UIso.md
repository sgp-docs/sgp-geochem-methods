#### Uranium Isotopes

**Commonly cited method papers**

- Potter et al. 2005 https://doi.org/10.1016/j.ijms.2005.08.017
- Stirling et al. 2007 https://doi.org/10.1016/j.epsl.2007.09.019
- Weyer et al. 2008 https://doi.org/10.1016/j.gca.2007.11.012
- Brennecka et al., 2011 https://doi.org/10.1073/pnas.1106039108
- Kendall et al. 2013 https://doi.org/10.1016/j.chemgeo.2013.08.010
- Dang et al. 2016 https://doi.org/10.1021/acs.est.6b01459
- Lau et al. 2016 https://doi.org/10.1073/pnas.1515080113
- Wang et al. 2016 https://doi.org/10.2475/01.2016.02
- White et al. 2018 https://doi.org/10.1016/j.epsl.2018.09.020 (incl. 1M HNO3 leach)
- Clarkson et al. 2018 https://doi.org/10.1073/pnas.1715278115 (incl. ox-red cleaning procedure)
- Dang et al. 2018 https://doi.org/10.1016/j.scitotenv.2017.08.156
- Lau et al. 2019 https://doi.org/10.1017/9781108584142
- Clarkson et al. 2020 https://doi.org/10.1016/j.chemgeo.2019.119412 (carbonate)
- Zhang et al. 2020 https://doi.org/10.1016/j.gca.2020.05.011 (carbonate)
- Kalderon-Asael et al. 2021 https://doi.org/10.1038/s41586-021-03612-1 (leaching procedure for carbonates)
- Dang et al. 2022 https://doi.org/10.1016/j.chemgeo.2021.120644 (authigenic)

**Notes**

Uranium isotopes in SGP are relatively evenly divided between total/bulk and carbonate-specific measurements, with rare examples coded as authigenic. Bulk isotopes are determined after a strong acid digest (often with a combustion/ashing step) and carbonate isotopes (and one authigenic) after a light or moderate acid digest.

White et al. 2018, and subsequent related papers, describe a procedure where the "sample powder was digested at room temperature by adding 20 mL of 1M HNO3, followed by the slow addition of 3 mL of concentrated HNO3 to replace the acid neutralized by reaction with CaCO". This is coded simply as HNO3(1M).

Authigenic uranium isotopes in SGP come from two studies so far. Those from Lu et al. 2020 are calculated relative to PAAS. Those from Dang et al. 2022 are measured after an aqua regia leach - see Dang et al. 2022 for discussion of authigenic components generally.

_Additional steps not coded_
As discussed above, many protocols include pre-digest cleaning steps, intermediate treatments, or post-column-chemistry steps, often with similar aims, which are _not coded_ for. For example:

- a pre-digest cleaning step described in Tostevin et al. 2019, based on Clarkson et al. 2018: "two-step reductive and oxidative cleaning procedure to remove potential Mn-oxides and residual organic matter"
- an intermediate treatment described in Dang et al. 2022 (after initial acid digest): "Clear solutions were dried at 95degC before samples were redissolved in 4 mL HCl. The solutions were dried again and a second 4 mL of HCl were added. These steps were designed to dissolve any fluoride precipitate. If needed (brown-colored solutions), 0.5 to 2 mL of H2O2 was added in HCl acid media to oxidize any residual organic content"
- a similar intermediate treatment described in White et al. 2018, and related papers (after initial 1M HNO3 digest): " Spiked samples were subsequently dried down to equilibrate the spike mixture, and the residue was treated with a solution of 0.3 mL 32% H2O2 and 2 mL concentrated HNO3 at ~100°C for one hour to oxidize any residual organic carbon leached from the samples prior to column chemistry."
- a post-column chemistry step described in Lu et al. 2023: "After column chemistry, samples were treated with both concentrated HNO3 and 30% H2O2 (hydrogen peroxide) twice to break down any residual organic matter from the resin"

_Chromatography/Purification_

By far the most commonly used **resin** is Triskem/Eichrom UTEVA. Others use TRU or RE resins, these are specified in the code.

In some cases, it is explicitly stated that two column steps/two column passes were used, and this is included in the code. In some cases, two steps are described with different resins, for example

- anion exchange with AG1X8 resin, preceding ion exchange with UTEVA in Clarkson et al. 2021
- ion exchange with DGA resin ("to remove excess Na"), after ion exchange with UTEVA e.g. Cheng et al. 2020, Remirez et al. 2024.

Double-spike (usually IRMM-3636 236U-233U, sometimes in-house) is used to correct for U isotope fractionation during the column chemistry and instrumental mass bias. Sample-standard bracketing is also commonly used.

In SGP the **reference standard** used so far for uranium isotopes is CRM-145/CRM-112a, and in one instance NIST SRM 950a (Kendall et al. 2013 http://dx.doi.org/10.1016/j.chemgeo.2013.08.010, with the following noted: "We report the U isotope composition of each sample relative to the SRM950a standard as δ238U [‰] = [238/235Usample / 238/235USRM950a − 1] × 1000. We have determined that standard CRM145 (also known as CRM112a; Telus et al., 2012) has a statistically identical U isotope composition compared to SRM950a (δ238U = 0.04 ± 0.06‰; 2SD, n = 38), in agreement with initial results reported by Weyer et al. (2008)."

**Proxy Primer**

Dr. Kimberly Lau, Uranium Isotopes https://www.youtube.com/watch?v=tg7Zf6hjaMI

| analyte(s)      | count_res | code                    | translation                                                                                      | ana_method(s) |
| --------------- | --------- | ----------------------- | ------------------------------------------------------------------------------------------------ | ------------- |
| DELTA_U238      | 252       | CB_MA3_IE               | Combustion/ashing, HNO3/HCl/HF digest, ion exchange chromatography (UTEVA resin)                 | ICP:MS-MC     |
| DELTA_U238      | 53        | CB_MA3d_IE              | Combustion/ashing, HNO3/HF, aqua regia, ion exchange chromatography (UTEVA resin)                | ICP:MS-MC     |
| DELTA_U238      | 30        | MA3b_IE                 | HF/HNO3/HClO4, ion exchange chromatography (UTEVA resin)                                         | ICP:MS-MC     |
| DELTA_U238      | 29        | MA4_IE(TRUresin)        | HF/HCl/HNO3/HClO4, ion exchange separation (TRU resin)                                           | ICP:MS-MC     |
| DELTA_U238      | 27        | MA3_IE                  | HF/HNO3/HCl, ion exchange chromatography (UTEVA resin)                                           | ICP:MS-MC     |
| DELTA_U238      | 9         | CB_MA3d_2IE             | Combustion/ashing, HNO3/HF, aqua regia, ion exchange chromatography (x2)(UTEVA resin)            | ICP:MS-MC     |
| DELTA_U238_CARB | 193       | HNO3(1M)\_IE            | 1M HNO3, ion exchange chromatography (UTEVA resin)                                               | ICP:MS-MC     |
| DELTA_U238_CARB | 133       | NaOAc(1M)\_IE           | 1M sodium acetate, ion exchange chromatography (UTEVA resin)                                     | ICP:MS-MC     |
| DELTA_U238_CARB | 127       | HCl(1N)\_2IE            | 1N HCl, two-step ion exchange chromatography (UTEVA resin)                                       | ICP:MS-MC     |
| DELTA_U238_CARB | 112       | HCl(0.25N)\_2IE         | 0.25N HCl, two-step ion exchange chromatography (UTEVA resin)                                    | ICP:MS-MC     |
| DELTA_U238_CARB | 107       | HNO3(1M)\_2IE           | 1M HNO3, 2 x ion exchange chromatography (UTEVA)                                                 | ICP:MS-MC     |
| DELTA_U238_CARB | 83        | HCl(1N)\_IE             | 1N HCl, ion exchange chromatography (UTEVA resin)                                                | ICP:MS-MC     |
| DELTA_U238_CARB | 82        | HNO3(1M)\_IE/AIC        | 1M HNO3, ion exchange chromatography (UTEVA) + automated ion chromatography (DGA resin)          | ICP:MS-MC     |
| DELTA_U238_CARB | 78        | NH4Ac(1M)\_2IE(REresin) | NH4Ac(1M), ion exchange chromatography (RE resin)                                                | ICP:MS-MC     |
| DELTA_U238_CARB | 40        | HCl(0.1NSeq)\_2IE       | 0.1N HCl in 4hr, 2hr, 10min sequential steps, two-step ion exchange chromatography (UTEVA resin) | ICP:MS-MC     |
| DELTA_U238_CARB | 17        | AcOH(0.5M)\_AE/IE       | 0.5N acetic acid, anion exchange (AG1X8 resin) ion exchange chromatography (UTEVA resin)         | ICP:MS-MC     |
| DELTA_U238_AUTH | 146       | AR_IE(TRUresin)         | Aqua regia, ion exchange chromatography (TRU resin)                                              | ICP:MS-MC     |
| DELTA_U238_AUTH | 23        | NULL                    | NULL                                                                                             | CALC          |
