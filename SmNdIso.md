#### Samarium-Neodymium Isotopes

**Commonly cited method papers**

- Pin and Zalduegui 1997 https://doi.org/10.1016/S0003-2670(96)00499-0

**Notes**

Preparation for Sm-Nd isotopes generally involves a combustion/ashing step, strong multi-acid digest, usually heated, usually in multiple stages, and chromatography:

- anion exchange, AG1X8 resin to remove iron (not always mentioned)
- cation exchange, Eichrom TRU resin or Bio-Rad AG50W, to remove REE
- cation exchange, Eichrom LN resin, for Sm and Nd.

In one example (Maloney et al. 2024), the strong acid digest is preceded by treatment in acetic acid to remove carbonate. In another example (Mundl et al. 2018), the sample is digested using flux fusion, and only the last chromatography step is mentioned (cation with LN resin for Sm and Nd).

**εNd(0)** (aka εNd) is the present-day deviation of the sample from CHUR, defined as follows: εNd = [(143Nd/144Nd)sample – (143Nd/144Nd)CHUR] – 1 \* 10000

**εNd(t)**. As described in Maloney et al. 2024: "values are commonly presented as a function of age where both the sample and CHUR 143Nd/144Nd ratios are corrected for 143Nd ingrowth since the time the rocks were deposited.". The age used is stored in the database, but not yet available on the website - refer to original publications for details.

**εNdi** = Initial ɛNd at time of rock formation

| analytes                                         | count_res | code                      | translation                                                                                    | ana_methods    |
| ------------------------------------------------ | --------- | ------------------------- | ---------------------------------------------------------------------------------------------- | -------------- |
| Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0)         | 70        | MA2_2CE                   | HF/HNO3, two-step cation exchange chromatography (Sm Nd with LN resin)                         | ID-NTIMS, TIMS |
| Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(t)         | 30        | LTMF_CE                   | Lithium tetraborate/metaborate fusion, cation exchange chromatography (LN resin)               | ID-NTIMS, TIMS |
| Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0), eNd(t) | 72        | CB_AcOH_MA2_AR/HCl_AE/2CE | Ash, AcOH decarb, HF/HNO3, aqua regia, HCl, chrom. (anion AG1X8, cation TRU, cation LN)        | ICP:MS-MC      |
| Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0), eNd(t) | 168       | CB_MA2_HCl/HNO3_AE/2CE    | Combustion/ashing, HF/HNO3, HCl/HNO3, 3step chrom (anion AG1X8, cation TRU, cation LN)         | ICP:MS-MC      |
| Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNdi           | 250       | CB_MA3_AE/2CE             | Combustion/ashing, HF/HNO3, aqua regia, HCl, 3step chrom. (anion AG1X8, cation TRU, cation LN) | TIMS/ICP:MS-MC |
| Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0), eNd(t) | 90        | CB_MA2_HCl/HNO3_2CE       | Combustion/ashing, HF/HNO3, HCl/HNO3, cation ex. chrom x 2 (AG50W for REE, LN resin for Sm Nd) | ID-NTIMS, TIMS |
