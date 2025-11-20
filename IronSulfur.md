### Iron and Sulfur

**Commonly cited method papers**

- Poulton and Canfield 2005 https://doi.org/10.1016/j.chemgeo.2004.09.003 (sequential iron)
- Canfield et al. 1986 https://doi.org/10.1016/0009-2541(86)90078-1 (pyrite, acid-volatile sulfur)
- Gill et al. 2008 https://doi.org/10.1016/j.gca.2008.07.001 (carbonate-associated sulfate)
- Wotte et al. 2012 https://doi.org/10.1016/j.chemgeo.2012.07.020 (carbonate-associated sulfate)
- Rice et al. 1993 https://doi.org/10.1016/0009-2541(93)90103-P (acid-volatile sulfur)
- _Others_: Lord 1982 (pyrite), Raiswell (1994, 2011), Berner 1970

**Notes**

In SGP the overwhelming majority of **sequential iron**/targeted iron extractions are done using the method of Poulton and Canfield 2005, (SeqA, SeqB, SeqC), along with **pyrite-iron** measurements sensu Canfield et al. 1986 (CRS).

In 2025, after the addition of “-carb” analytes (see Carbonate Proxies below) the analyte codes for sequentially extracted iron were changed to Fe-carb(seq), Fe-ox(seq), Fe-mag(seq), to avoid confusion between Fe-carb from SeqA method and Fe-carb from a light leach.

Published **FeHR, FeHR/FeT and Fe-py/FeHR** are stored in the proxy table. On the website, the presented values are calculated based on the component parts in the first instance (e.g. highly-reactive iron FeHR = Fe-carb(seq) + Fe-ox(seq) + Fe-mag(seq) + Fe-py) and published values are used if components are not available.

For **total iron** see [Elements](https://github.com/ufarrell/sgp_phase2/wiki/C.-Analyses#elements) section below.

Some studies have modified the SeqA method for Fe-carb extraction by time or temperature. In one case carbonate iron is defined based on the cold HCl method of Raiswell. Similarly, there is one modification of SeqB by time (6h instead of 2h).

Note that Pyrite-iron, pyrite, total sulfur and pyrite-sulfur are sometimes ambiguously named in tables and/or not mentioned in the methods e.g. tables with “pyrite” or “py” in a header where the value is for “Fe-py”, or a column for sulfur but no discussion of method, such that it could be S-py by CRS, or S measured along with carbon/other elements. Sometimes, therefore, an assumption has been made based on circumstantial evidence.

For discussion of **CAS** (carbonate-associated sulfate) methods see papers by Gill et al. 2008, and Wotte et al. 2012. Variations include repetition of the NaCl leach step, and the addition (or not) of bleach. In some cases CAS is determined stoichiometrically from the mass of the BaSO4 precipitate. In other cases SO4 is measured with ICP:MS or along with isotopes using EA-IRMS. S-org and S-SO4 values are mostly sourced from the USGS-NGDB database, with no associated methods.

The **reference standard** for sulfur isotopes is Vienna-Cañon Diablo Troilite (VCDT).

**Proxy Primer**

Dr. Maya Gomes, Sulfur Isotopes: https://www.youtube.com/watch?v=5nbf9JtEVlU

| analyte(s)                             | count_res | code                   | translation                                                         | ana_method(s)                                       |
| -------------------------------------- | --------- | ---------------------- | ------------------------------------------------------------------- | --------------------------------------------------- |
| **Iron**                               |           |                        |                                                                     |                                                     |
| Fe-carb(seq)                           | 15741     | SeqA                   | Sodium acetate extraction, 48hr, 50degC (Poulton and Canfield 2005) | AAS, FSP, ICP:ES, ICP:MS, N/A, Q-ICP:MS, QQQ-ICP:MS |
| Fe-carb(seq)                           | 135       | SeqA(24h)              | Sodium acetate extraction, 24hr                                     | AAS, Q-ICP:MS                                       |
| Fe-carb(seq)                           | 59        | SeqA(RoomTemp)         | Sodium acetate extraction, 48hr, room temperature                   | ICP:MS                                              |
| Fe-ox(seq)                             | 15613     | SeqB                   | Sodium dithionite extraction, 2hr (Poulton and Canfield 2005)       | AAS, FSP, ICP:ES, ICP:MS, N/A, Q-ICP:MS, QQQ-ICP:MS |
| Fe-ox(seq)                             | 201       | SeqB(6h)               | Sodium dithionite extraction, 6hr                                   | AAS                                                 |
| Fe-mag(seq)                            | 15719     | SeqC                   | Ammonium oxalate extraction, 6hr (Poulton and Canfield 2005)        | AAS, FSP, ICP:ES, ICP:MS, N/A, Q-ICP:MS, QQQ-ICP:MS |
| Fe-py                                  | 15273     | CRS                    | Chromous chloride reduction (Canfield et al. 1986)                  | EA-CF-IRMS, STOICH                                  |
| Fe-py                                  | 5         | Lord1982               | Pyrite sensu Lord 1982                                              | ICP:ES                                              |
| Fe-py                                  | 38        | CB                     | Combustion/ashing                                                   | STOICH                                              |
| Fe-AVS                                 | 10        | AVS_HCl(6N/hot)\_SnCl2 | Hot 6N HCl acid-volatile sulfur extraction (Rice et al. 1993)       | STOICH                                              |
| Fe-AVS                                 | 22        | AVS_HCl(6N)            | 6N HCl distillation for acid volatile sulfur                        | STOICH                                              |
| Fe-HCl, Fe-py                          | 698       | HCl(12N/1min/boil)     | Boiling 12N HCl for 1min (Berner 1970)                              | AAS, CAT, FSP, ICP:MS, N/A                          |
| Fe-AVS, Fe-HCl, Fe-py                  | 282       | NULL                   | NULL                                                                | CS-EA, N/A                                          |
| **Sulfur**                             |           |                        |                                                                     |                                                     |
| CAS                                    | 226       | NaCl(rep)/HCl/BaCl2    | NaCl (repeated leaches), HCl, BaCl2 (Wotte et al. 2012)             | EA-CF-IRMS, EA-IRMS, ICP:MS, STOICH                 |
| CAS                                    | 101       | NaCl/HCl/BaCl2         | NaCl (single leach), HCl, BaCl2                                     | STOICH                                              |
| CAS                                    | 94        | NaCl/NaOCl/HCl         | NaCl and NaOCl(bleach), HCl                                         | Q-ICP:MS                                            |
| CAS                                    | 69        | NaCl/NaOCl/HCl/BaCl2   | NaCl and NaOCl(bleach), HCl, BaCl2                                  | STOICH                                              |
| AVS, S_ORG, S_SO4                      | 1087      | NULL                   | NULL                                                                | N/A, TS-NAVS                                        |
| **Sulfur Isotopes**                    |           |                        |                                                                     |
| DELTA_S34_PY                           | 6965      | CRS                    | Chromous chloride reduction (Canfield et al. 1986)                  | CF-IRMS, EA-CF-IRMS, EA-IRMS, IRMS, N/A             |
| DELTA_S34                              | 420       | HCl(decarb)            | Decarbonization with HCl                                            | EA-IRMS                                             |
| DELTA_S34                              | 71        | CB                     | Combustion/ashing                                                   | EA-IRMS                                             |
| DELTA_S34_CAS                          | 245       | NaCl(rep)/HCl/BaCl2    | NaCl (repeated leaches), HCl, BaCl2 (Wotte et al. 2012)             | EA-CF-IRMS, EA-IRMS                                 |
| DELTA_S34_CAS                          | 194       | NaCl/NaOCl/HCl/BaCl2   | NaCl and NaOCl(bleach), HCl, BaCl2                                  | EA-IRMS                                             |
| DELTA_S34_CAS, DELTA_S34_GYP           | 72        | NaCl/HCl/BaCl2         | NaCl (single leach), HCl, BaCl2                                     | EA-IRMS                                             |
| DELTA_S34_CAS                          | 11        | NaOCl/HCl/BaCl2        | NaOCl(bleach), HCl, BaCl2 (summary in Gill et al. 2008)             | IRMS                                                |
| DELTA_S34_OBS                          | 66        | SeqOBS                 | Sequential sulfur extraction AVS/CRS/CB/BaCl2                       | EA-IRMS                                             |
| DELTA_S34, DELTA_S34_CAS, DELTA_S34_PY | 1188      | NULL                   | NULL                                                                | EA-CF-IRMS, EA-IRMS, IRMS, N/A                      |
