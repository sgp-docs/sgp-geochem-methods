## Analytes

The diagram below summarizes the count of individual results for each category of analytes. Categories are based on those used on our search website (http://sgp-search.io/).

![](https://github.com/ufarrell/sgp_phase2/blob/051737d444cc419108592b4af11729dbef9f189c/wiki_figs/phase2_anacat_bydatasource.png)

## Analytical Metadata

We store information in the database about

* the lab where analyses are run
* the instruments used
* the dates of the analyses
* the person running the experiment
* the person providing the data, especially if the data is unpublished 

These categories are variably populated depending on the source of the data (see [A. Database Description](https://github.com/ufarrell/sgp_phase2/wiki/A.-Database-description)).

![map of labs](https://github.com/ufarrell/sgp_phase2/blob/c2265337bb9b61a8ed73b027953d3003b3f1d9cf/wiki_figs/map_of_labs.png)

34% of all data and 81% of SGP-entered data are associated with a lab. Those with the most results are commercial laboratories, where large amounts of elemental data tend to be generated for each sample.

University labs, by count of results (top ten).
|Institution                            |Count Results|
|--------------------------------------|-------------|
|Stanford University                   |45855        |
|Arizona State University              |21293        |
|University of Maryland                |16084        |
|University of Cincinnati              |13701        |
|University of California, Riverside   |12677        |
|McGill University                     |12213        |
|Virginia Polytechnic Institute and State University|9438         |
|Harvard University                    |8874         |
|University of Texas Permian Basin     |8869         |
|Yale University                       |8603         |

Commercial labs/Geological Surveys/Analytical Centers by count of results (top ten)
|Institution                            |Count Results|
|--------------------------------------|-------------|
|Bureau Veritas Minerals Laboratories  |615055       |
|Intertek-Genalysis Laboratory         |138800       |
|SGS                                   |90910        |
|Activation Laboratories Ltd. (Actlabs)|49371        |
|AGAT Laboratories                     |32419        |
|Chemostrat                            |29601        |
|LabWest Minerals Analysis Pty Ltd.    |28995        |
|Geological Survey of Canada, Calgary  |19354        |
|Pôle Spectrométrie Océan              |16249        |
|GeoMark Research, Ltd., Texas         |13444        |

## Analytical Methods

The diagram below illustrates the proportion of individual results for each analytical method. Some methods have been simplified/concatenated for clarity. See [here](https://github.com/ufarrell/sgp_phase2/blob/af5ac8e7fc2bbea392fff6355b854b136856a79a/wiki_docs/phase2_ana_methods_all.csv) for a full list of analytical methods.

![](https://github.com/ufarrell/sgp_phase2/blob/ad7af87a585848ad3faca683059c5786d5aebd67/wiki_figs/phase2_ana_methods.png)
FSP = Ferrozine Spectrophotometry, NAA includes NAA, INAA and DNAA, Pyrol. includes SRA (source rock analysis), REP (Rock Eval pyrolysis, Vinci Technologies), and HAWK (Hydrocarbon Analysis With Kinetics, Wildcat Technologies). CALC/STOICH includes all calculated data (e.g. TC-TIC for organic carbon), and results calculated by stoichiometry (e.g. Fe-py after CRS).

## Preparation Methods

The first step in most geochemical analyses is to crush and powder the rock. This is usually accomplished in several stages: 
* Initial reduction into small pieces using a rock saw or hammer. This step often specifically includes the removal of weathered surfaces. 
* Further reduction in size (in some cases) using e.g. a jaw crusher. 
* Ground to a powder using a either a mill/shatterbox, or by hand with a mortar and pestle. 

In some studies a microdrill is used in order to target specific mineral phases, or avoid areas of alteration. In rare cases no crushing is required e.g. XRF on a polished rock surface.

The material used in this process can impact the geochemical measurements. In the SGP database it is usually the final grinding step that is recorded (e.g. Alumina (ceramic) ball mill). In the case of steel, note that it is most often 'hardened' steel of some kind that is used. The exact material is sometimes specified (e.g. chrome, carbon), but most are lumped together simply as steel. 

Note that sometimes pieces of the same hand sample are crushed in different ways, and therefore one sample can be associated with multiple preparation types. Samples with a long history associated with multiple studies can be difficult to trace - therefore some samples may be associated with a preparation type for some analyses and have no preparation type for others, if it was not clear whether the same powder was used.

The following diagram summarizes the proportion of results in the database grouped by material, the full dictionary can be found [here](https://github.com/ufarrell/sgp_phase2/blob/a90fe0d7cf310980a7823cc488396d248f1c9667/wiki_docs/phase2_prep_method.csv). 

![](https://github.com/ufarrell/sgp_phase2/blob/25fbd5a6d98483a744fe8a11d08a5b4326a43761/wiki_figs/phase2_prep_material.jpg)

## Experimental Methods

This category describes any experimental methods applied before a sample is analyzed - for example, acid digestion before ICP:MS.

Creating unique, simple, yet informative codes, is particularly challenging in this case. As a result this dictionary has been extensively revised since Phase 1, prompted partly by the addition of new carbonate and metal isotope data, and based on discussions with collaborators most familiar with the data.

Further revision is anticipated as we continue these discussions and add new kinds of data. While we aim to maintain stability in our dictionary terms, improving data quality is the first priority — so users should be aware that this dictionary in particular may not remain static.

The aim is to create codes which summarize essential steps, in particular if there is some debate over the relative strength of one method over another. Creating codes for newer, less established methods is generally the most difficult, as small variations in procedure are tested by different researchers. Where possible method papers, which set out all the key steps in detail, are linked to the code in the database (e.g. Poulton and Canfield, 2005 is linked to SeqA, B and C for iron speciation). 

The codes are designed to be somewhat human-readable, and they are used in a modular way - the same code is used again if it is part of a longer protocol. 

Standardized separators are used:
* Sequential steps are separated by an underscore. Example: CB_MA3 (combustion/ashing followed by a three-acid digestion).
* Details about a single step are enclosed in brackets and presented in a fixed order. Example: HCl(0.5N/24h/hot) (acid treatment with hot 0.5N HCl for 24 hours). 
* Multiple components of a single step are separated by a slash. Example: HCl/HNO3 (two-acid digestion using HCl and HNO3). 

The experimental method dictionary has three columns (based on the schema from the British Geological Survey): the experimental_method_code, experimental_method_translation and experimental_method_desc. Each is slightly more detailed than the last. The code and translation are available on the website. 

The sections below summarise methods based on the categories on the website. The tables are based around experimental methods which tend to be most specific to each category (whereas the analytical methods are more likely to be used across different groupings). Analytes and analytical method codes are grouped by category and then by experimental code, and usually sorted by number of results within a given category (the approach varies slightly depending what makes most sense for a given category). 

These summaries are based on the studies that are included in SGP Phase 2, and therefore are not intended as a complete review or recommendation of methods, but rather to give a sense of the data currently available. 

**Commonly cited papers** are subjectively taken from the methods sections of published papers, where we see the same citation turning up frequently - we note these are based on frequency and do not represent any suggestion/endorsement of a specific methodological approach.

Where SGP **Proxy Primers** are available, they are linked to the relevant section - these provide a detailed review of proxy use. 

**Reference standards** for isotopic measurements refer to the standards currently associated with data in the SGP database; note these may not represent all standards commonly used in the broader field.

***

### Iron and Sulfur

**Commonly cited method papers**
* Poulton and Canfield 2005 https://doi.org/10.1016/j.chemgeo.2004.09.003 (sequential iron)
* Canfield et al. 1986 https://doi.org/10.1016/0009-2541(86)90078-1 (pyrite, acid-volatile sulfur)
* Gill et al. 2008 https://doi.org/10.1016/j.gca.2008.07.001 (carbonate-associated sulfate)
* Wotte et al. 2012 https://doi.org/10.1016/j.chemgeo.2012.07.020 (carbonate-associated sulfate)
* Rice et al. 1993 https://doi.org/10.1016/0009-2541(93)90103-P (acid-volatile sulfur)
* _Others_: Lord 1982 (pyrite), Raiswell (1994, 2011), Berner 1970

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

|analyte(s)           |count_res|code      |translation                                             |ana_method(s)                                        |
|---------------------|---------|---------------------|-------------------------------------------------------------------|---------------------------------------------------|
|**Iron**      | | |                                        |                                    |
|Fe-carb(seq)         |15741    |SeqA                 |Sodium acetate extraction, 48hr, 50degC (Poulton and Canfield 2005)|AAS, FSP, ICP:ES, ICP:MS, N/A, Q-ICP:MS, QQQ-ICP:MS|
|Fe-carb(seq)         |135      |SeqA(24h)            |Sodium acetate extraction, 24hr                                    |AAS, Q-ICP:MS                                      |
|Fe-carb(seq)         |59       |SeqA(RoomTemp)       |Sodium acetate extraction, 48hr, room temperature                  |ICP:MS                                             |
|Fe-ox(seq)          |15613    |SeqB                 |Sodium dithionite extraction, 2hr (Poulton and Canfield 2005)      |AAS, FSP, ICP:ES, ICP:MS, N/A, Q-ICP:MS, QQQ-ICP:MS|
|Fe-ox(seq)           |201      |SeqB(6h)             |Sodium dithionite extraction, 6hr                                  |AAS                                                |
|Fe-mag(seq)          |15719    |SeqC                 |Ammonium oxalate extraction, 6hr (Poulton and Canfield 2005)       |AAS, FSP, ICP:ES, ICP:MS, N/A, Q-ICP:MS, QQQ-ICP:MS|
|Fe-py                |15273    |CRS                  |Chromous chloride reduction (Canfield et al. 1986)                 |EA-CF-IRMS, STOICH                                 |
|Fe-py                |5        |Lord1982             |Pyrite sensu Lord 1982                                             |ICP:ES                                             |
|Fe-py                |38       |CB                   |Combustion/ashing                                                  |STOICH                                             |
|Fe-AVS               |10       |AVS_HCl(6N/hot)_SnCl2|Hot 6N HCl acid-volatile sulfur extraction (Rice et al. 1993)      |STOICH                                             |
|Fe-AVS               |22       |AVS_HCl(6N)          |6N HCl distillation for acid volatile sulfur                       |STOICH                                             |
|Fe-HCl, Fe-py        |698      |HCl(12N/1min/boil)   |Boiling 12N HCl for 1min (Berner 1970)                             |AAS, CAT, FSP, ICP:MS, N/A                         |
|Fe-AVS, Fe-HCl, Fe-py|282      |NULL                 |NULL                                                               |CS-EA, N/A                                         |
|**Sulfur**    |||||
|CAS              |226      |NaCl(rep)/HCl/BaCl2 |NaCl (repeated leaches), HCl, BaCl2 (Wotte et al. 2012)|EA-CF-IRMS, EA-IRMS, ICP:MS, STOICH|
|CAS              |101      |NaCl/HCl/BaCl2      |NaCl (single leach), HCl, BaCl2                        |STOICH                             |
|CAS              |94       |NaCl/NaOCl/HCl      |NaCl and NaOCl(bleach), HCl                            |Q-ICP:MS                           |
|CAS              |69       |NaCl/NaOCl/HCl/BaCl2|NaCl and NaOCl(bleach), HCl, BaCl2                     |STOICH                             |
|AVS, S_ORG, S_SO4|1087     |NULL                |NULL                                                   |N/A, TS-NAVS                       |
|**Sulfur Isotopes**    ||     |                               |                  
|DELTA_S34_PY                          |6965|CRS                 |Chromous chloride reduction (Canfield et al. 1986)     |CF-IRMS, EA-CF-IRMS, EA-IRMS, IRMS, N/A|
|DELTA_S34                             |420 |HCl(decarb)         |Decarbonization with HCl                               |EA-IRMS                                |
|DELTA_S34                             |71  |CB                  |Combustion/ashing                                      |EA-IRMS                                |
|DELTA_S34_CAS                         |245 |NaCl(rep)/HCl/BaCl2 |NaCl (repeated leaches), HCl, BaCl2 (Wotte et al. 2012)|EA-CF-IRMS, EA-IRMS                    |
|DELTA_S34_CAS                         |194 |NaCl/NaOCl/HCl/BaCl2|NaCl and NaOCl(bleach), HCl, BaCl2                     |EA-IRMS                                |
|DELTA_S34_CAS, DELTA_S34_GYP          |72  |NaCl/HCl/BaCl2      |NaCl (single leach), HCl, BaCl2                        |EA-IRMS                                |
|DELTA_S34_CAS                         |11  |NaOCl/HCl/BaCl2     |NaOCl(bleach), HCl, BaCl2 (summary in Gill et al. 2008)|IRMS                                   |
|DELTA_S34_OBS                         |66  |SeqOBS              |Sequential sulfur extraction AVS/CRS/CB/BaCl2          |EA-IRMS                                |
|DELTA_S34, DELTA_S34_CAS, DELTA_S34_PY|1188|NULL                |NULL                                                   |EA-CF-IRMS, EA-IRMS, IRMS, N/A         |

***

### Carbon

**Notes**

Total organic carbon (**TOC**) is most commonly determined by elemental analysis (EA, CS-EA, or CHNS-EA - most specify LECO) after removal of carbonate with an acid treatment (usually HCl). 

In some cases the acid type is not specified, although HCl is most likely used - these cases are coded as "Decarb" only. A proportion of TOC measurements were determined by EA, without any acid treatment - note that, in at least some of these cases, it is quite possible that an acid treatment was used but not specifically mentioned. In particular, this applies to a subset of USGS-CMIBS data which has the following method:

 _"Forms of carbon and forms of sulfur by infrared detection after combustion; acid digestion may precede combustion for all but total C and total S"_. 

This method is considered to be the equivalent to the SGP method of CS-EA. In SGP the combustion is considered an integral part of the CS-EA process, and not coded separately.

If TOC is determined by difference (Total Carbon - Total Inorganic Carbon) no experimental step is included. 

Some CMIBS data comes with the following method description:
_"Total carbon, carbonate carbon and organic carbon by an unspecified detection method after combustion; acid digestion may precede combustion for all but total C and total S"_. These have the experimental method "CB" and no analytical method. 

Total Inorganic Carbon (TIC) is usually determined by difference (Total Carbon - Total Organic Carbon), by acid treatment and mass-loss/gravimetry (see also "Carbonate" in the next section), or by coulometry. Some TIC values have an acid experimental method "HCl(decarb)" and EA as the analytical method - note this is for direct EA with an acidification module (rather than HCl(decarb) and mass loss/stoichiometry).

Programmed pyrolysis data are most commonly analyzed using Rock Eval (Vinci Technologies), with some by HAWK (Wildcat Technologies) or Source Rock Analysis (Weatherford Labs TPH-TOC Workstation). A small minority of studies had no reported methods for programmed pyrolysis analytes, and Rock Eval was assumed based on circumstantial evidence (including factors such as the location of the analysis and the age of the study - Rock Eval being more likely for older studies).

The **reference standard** for carbon isotopes is Vienna Pee Dee Belemnite (VPDB).

**Proxy Primer**

Dr. Alex Zumberge, Programmed Pyrolysis (Rock Eval) https://www.youtube.com/watch?v=7yz0gi-rXL4

Dr. Selva Marroquin, Carbon isotopes and chemostratigraphy https://www.youtube.com/watch?v=xXdYWXP6hxU

|analyte(s)|count_res|code            |translation                                           |ana_method(s)                                                    |
|----------|---------|----------------|------------------------------------------------------|-----------------------------------------------------------------|
|TOC       |28601    |NULL            |NULL                                                  |COUL, CS-EA, EA, EA-CF-IRMS, EA-IRMS, HAWK, N/A, REP, SRA, TC-TIC|
|TOC       |16951    |HCl(decarb)     |Decarbonated with HCl                                 |CHNS-EA, CS-EA, EA, EA-CF-IRMS, EA-IRMS, IR, IRMS, N/A           |
|TOC       |3039     |Decarb          |Decarbonated (no details provided, likely HCl or AcOH)|CS-EA, EA-CF-IRMS, EA-IRMS, REP                                  |
|TOC       |701      |WO_H2SO4        |Wet oxidation with H2SO4 (CMIBS method)               |GRAV                                                             |
|TOC       |383      |CB              |Combustion/ashing                                     |CHNS-EA, COUL, N/A, TC                                           |
|TOC       |202      |HCl(decarb)_MA2b|Decarbonated with HCl, HCl/HF                         |EA                                                               |
|TOC       |130      |500deg          |Heated to 500degC                                     |LOI                                                              |
|TOC       |128      |Acid_CB         |Acidified before Dumas combustion technique           |VD                                                               |
|TOC       |70       |H2SO3           |Sulfurous acid                                        |EA-CF-IRMS                                                       |
|TOC       |26       |MA3             |HNO3/HCl/HF                                           |CS-EA                                                            |
|TOC       |12       |Digest          |Unspecified digestion (CMIBS method)                  |ICP:MS                                                           |
|TIC     |13574    |NULL            |NULL                                                  |COUL, CS-EA, EA, EA-IRMS, HAWK, N/A, TC-TOC, TTR, VOL            |
|TIC     |1521     |HCl(decarb)     |Decarbonated with HCl                                 |CS-EA, IR, ML                                                    |
|TIC     |726      |H3PO4           |Phosphoric acid                                       |CS-EA, EA, IRMS                                                  |
|TIC     |360      |Decarb          |Decarbonated (no details provided, likely HCl or AcOH)|COUL, CS-EA, EA, ML                                              |
|TIC     |313      |HClO4           |Perchloric acid                                       |COUL, COUL_TT                                                    |
|TIC     |97       |CB              |Combustion/ashing                                     |EA, N/A                                                          |
|C           |12669    |NULL            |NULL                                       |CS-EA, EA, EA-IRMS, GRAV, GRAV_FLUX, IR, N/A, REP                |
|C           |12420    |CB              |Combustion/ashing                          |CHNS-EA, COUL, CS-EA, IR, N/A, TC                                |
|C           |6        |Digest          |Unspecified digestion (CMIBS method)       |WC                                                               |
|**Organic carbon isotopes**|||||
|DELTA_C13_ORG|10204|HCl(decarb)     |Decarbonated with HCl              |CF-IRMS, EA-CF-IRMS, EA-IRMS, IRMS|
|DELTA_C13_ORG|2178|NULL            |NULL                               |EA-CF-IRMS, EA-IRMS, IRMS, N/A|
|DELTA_C13_ORG|704 |Decarb          |Decarbonated (no details provided)|EA-CF-IRMS, EA-IRMS           |
|DELTA_C13_ORG|160 |HCl(decarb)_MA2b|Decarbonated with HCl, HCl/HF      |IRMS                          |
|DELTA_C13_ORG|104 |MA2b            |HCl/HF                             |EA-IRMS                       |
|DELTA_C13_ORG|79  |H2SO3           |Sulfurous acid                     |EA-CF-IRMS                    |
|**Rock Eval Pyrolysis/HAWK/Source Rock Analysis**|    |                |                                   |                              |
|S1, S2, S3, Tmax  |26029|NULL            |NULL                               |HAWK, REP, SRA, N/A                |
|S1, S2, S3, Tmax           |7875|Decarb          |Decarbonated (no details provided) |REP                           |

***

### Carbonate proxies

In Phase 2, new analytes with the subscript "_carb" were added to accommodate carbonate data from a light acid leach, specifically targeting metals in the carbonate crystal lattice. These analyses usually involve a single-acid leach of various strengths. Some protocols used a relatively strong acid (e.g., a 6N HCl) which may leach elements from clay or detrital minerals compared to a lighter leach, but that are philosophically targeting the carbonate fraction. The acid strength is a key part of the experimental code in this instance (by contrast, see [Elements](https://github.com/ufarrell/sgp_phase2/wiki/C.-Analyses#elements), where strong acids are assumed).

**Carbonate** is sometimes short-handed as 'CaCO3' in data tables, even where methods used clearly could be extracting other carbonate types (iron carbonate, dolomite etc.). On the SGP website these are all presented as 'Carbonate'.

Outliers include 1) 'CaCO3' with a four-acid digest - CMIBS data, results from Lewis_2010 with the method _"Major and minor elements by inductively coupled plasma-atomic emission spectrometry after digestion with HF-HCl-HNO3-HClO4; Fe2O3 by computation FeTO3 less FeO"_. 2) CaCO3 from Stüecken et al after SeqA method: _"Calcium and Mg concentrations in the acetic acid fraction were used to determine the relative abundances of CaCO3 and MgCO3 end members in the samples"._

The overwhelming majority of carbonate-carbon and oxygen isotopes are determined by IRMS with an associated carbonate preparation device (e.g. Kiel III, Gasbench, NuCarb etc.) using phosphoric acid (H3PO4).

The **reference standard** for carbonate-carbon and -oxygen isotopes is Vienna Pee Dee Belemnite (VPDB).

#### Cerium anomalies

**Commonly cited method papers**

* Bau and Dulski, 1996 https://doi.org/10.1016/0301-9268(95)00087-9 ([Ce/Ce* = 2Ce/(La+Pr)])
* Shields and Stille 2001 https://doi.org/10.1016/S0009-2541(00)00362-4 ([Ce/Ce* = 3Ce/(2La+Nd)])
* Lawrence et al. 2006 https://doi.org/10.1007/s10498-005-4471-8 [Ce/Ce* = Ce/(Pr/Nd^2)]
* See Barrat et al. 2023 https://doi.org/10.1016/j.chemgeo.2022.121202 for discussion.

Cerium anomalies are reported in SGP as published and currently do not distinguish between calculation methods (i.e., whether and how Ce is compared to La, Pr, and Nd). 

From Dr. Rosalie Tostevin (pers. comm. 2024) "there are two common approaches in circulation: linear and geometric. Older papers, but some newer ones too, compare the concentration of Ce to its immediate neighbours, La and Pr [Ce/Ce* = 2Ce/(La+Pr)]. Because seawater has a positive La anomaly, this can result in a false negative Ce anomaly. To correct for this, these papers then cross plot Ce/Ce* against Pr anomalies to distinguish true Ce anomalies [Pr/Pr* = 2Pr/(Ce + Sm)]. Other papers calculate the Ce anomaly using the geometric formula [Ce/Ce* = Ce/(Pr/Nd^2)], which avoids comparison with La. [...] Note: all concentrations referred to in formulas above are PAAS-normalised. 

Of 24 studies in SGP with Ce/Ce* values
* 15 use the geometric formula [Ce/Ce* = Ce/(Pr/Nd^2)]
* 5 use the linear formula [Ce/Ce* = 2Ce/(La+Pr)]
* 1 uses the linear formula [Ce/Ce* = 3Ce/(2La+Nd)] 
* 3 are unknown.

**Proxy Primer**

Dr. Rosalie Tostevin, Cerium anomalies https://www.youtube.com/watch?v=TQ8lkd_w1qI

#### I/Ca and I/[Ca+Mg]

**Commonly cited method papers**

* Lu et al. 2010 https://doi.org/10.1130/G31145.1 (and other subsequent papers by the same author/authors)
* Zhou et al. 2015 http://dx.doi.org/10.1002/2014PA002741
* Wei et al. 2019 https://doi.org/10.1016/j.precamres.2019.01.007

**Proxy Primer**

Dr. Zunli Lu, I/Ca ratios https://www.youtube.com/watch?v=wkHys_KG91A


|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|**Carbonate isotopes**   || |||
|DELTA_C13_CARB, DELTA_O18_CARB|21369    |H3PO4           |Phosphoric acid                    |CF-IRMS, CRDS, EA-IRMS, GC-IRMS, IRMS|
|DELTA_C13_CARB, DELTA_O18_CARB|1401     |NULL            |NULL                               |EA-IRMS, IRMS, MassBal, N/A, SIMS|
|DELTA_C13_CARB, DELTA_O18_CARB|164      |Roast_380deg    |Roasted at 380degC                 |IRMS                          |
|DELTA_O18_CARB|115      |LaserFluor      |Laser fluorination                 |IRMS                          |
|**Carbonate**    |      |||                       |
|Carbonate|5390     |HCl(decarb)     |Decarbonated with HCl              |ML, VOL                       |
|Carbonate|1447     |NULL            |NULL                               |COUL, HAWK, N/A, STOICH       |
|CaCO3        |1407     |MA4             |HNO3/HClO4/HF/HCl                  |ICP:ES                        |
|Carbonate    |309      |Decarb          |Decarbonated (no details provided) |EA-CF-IRMS, ML                |
|CaCO3        |59       |SeqA            |Sodium acetate extraction, 48hr, 50degC (Poulton and Canfield 2005)|ICP:MS                        |
|**I/Ca** |     | | |        |
|I/Ca, I/[Ca+Mg]|910      |HNO3(3%)_TA     |HNO3, tertiary amine solution      |ICP:MS, Q-ICP:MS              |
|I/[Ca+Mg]    |47       |HNO3(3%)        |3% nitric acid                     |ICP:MS                        |
|**Carbonate-phase Elements** || ||              |
|Al-carb, As-carb, Ba-carb, Ca-carb, Cd-carb, Ce-carb, Co-carb, Cr-carb, Cs-carb, Cu-carb, Dy-carb, Er-carb, Eu-carb, Fe-carb, Ga-carb, Gd-carb, Ge-carb, Hf-carb, Ho-carb, La-carb, Li-carb, Lu-carb, Mg-carb, Mn-carb, Mo-carb, Nb-carb, Nd-carb, Ni-carb, P-carb, Pb-carb, Pr-carb, Rb-carb, Re-carb, Sb-carb, Sc-carb, Se-carb, Sm-carb, Sn-carb, Sr-carb, Ta-carb, Tb-carb, Th-carb, Ti-carb, Tl-carb, Tm-carb, U-carb, V-carb, W-carb, Y-carb, Yb-carb, Zn-carb, Zr-carb|15538    |AcOH(0.85N)     |0.85N acetic acid                  |ICP:MS-HR                     |
|Al-carb, Ca-carb, Ce-carb, Dy-carb, Er-carb, Eu-carb, Fe-carb, Gd-carb, Ho-carb, La-carb, Lu-carb, Mg-carb, Mn-carb, Nd-carb, Pr-carb, Sm-carb, Sr-carb, Tb-carb, Tm-carb, Y-carb, Yb-carb|9370     |HNO3(2%)        |2% nitric acid                     |ICP:ES, ICP:MS, Q-ICP:MS      |
|Al-carb, Ba-carb, Ca-carb, Ce-carb, Co-carb, Dy-carb, Er-carb, Fe-carb, Gd-carb, K-carb, La-carb, Mg-carb, Mn-carb, Mo-carb, Na-carb, Nd-carb, P-carb, Pr-carb, Rb-carb, Sm-carb, Sr-carb, Th-carb, Ti-carb, Tl-carb, U-carb, V-carb, Zn-carb|4219     |HCl(1N)         |1N hydrochloric acid               |ICP:ES, ICP:ES/MS, ICP:MS, Q-ICP:MS, QQQ-ICP:MS|
|Al-carb, Ca-carb, Eu-carb, Fe-carb, K-carb, Mg-carb, Mn-carb, Mo-carb, Na-carb, Nd-carb, P-carb, Rb-carb, Re-carb, Sr-carb, Th-carb, Ti-carb, U-carb, V-carb|3712     |HNO3(1M)        |1M nitric acid                     |Q-ICP:MS                      |
|Al-carb, Ca-carb, Ce-carb, Cr-carb, Dy-carb, Er-carb, Eu-carb, Gd-carb, HREE-carb, Ho-carb, LREE-carb, La-carb, Lu-carb, MREE-carb, Mg-carb, Mn-carb, Nd-carb, Pr-carb, Sc-carb, Sm-carb, Sr-carb, Tb-carb, Th-carb, Tm-carb, U-carb, Y-carb, Yb-carb|1597     |HCl(0.5N)       |0.5N hydrochloric acid             |ICP:ES, ICP:MS-HR, Q-ICP:MS   |
|Al-carb, Cu-carb, Mn-carb, Mo-carb, Ni-carb, U-carb, V-carb|973      |NaOAc(1M)       |1M sodium acetate (AcOH buffered)  |ICP:MS                        |
|Al-carb, Ca-carb, Ce-carb, Dy-carb, Er-carb, Eu-carb, Fe-carb, Gd-carb, Ho-carb, La-carb, Lu-carb, Mg-carb, Mn-carb, Nd-carb, Pb-carb, Pr-carb, Rb-carb, Sm-carb, Sr-carb, Tb-carb, Th-carb, Tm-carb, U-carb, Y-carb, Yb-carb|892      |HNO3(0.4M)      |0.4M nitric acid                   |Q-ICP:MS                      |
|Al-carb, Ce-carb, Dy-carb, Er-carb, Eu-carb, Gd-carb, Ho-carb, La-carb, Lu-carb, Mn-carb, Mo-carb, Nd-carb, Pr-carb, REY-carb, Sm-carb, Sr-carb, Tb-carb, Tm-carb, Y-carb, Yb-carb|880      |HCl(2N)         |2N hydrochloric acid               |ICP:MS                        |
|Ce-carb, Dy-carb, Er-carb, Eu-carb, Gd-carb, Ho-carb, La-carb, Lu-carb, Nd-carb, Pr-carb, Sm-carb, Tb-carb, Tm-carb, Y-carb, Yb-carb|585      |HCl(0.1NSeq)    |0.1N HCl in 4hr, 2hr, 10min sequential steps|ICP:MS                        |
|Al-carb, Ca-carb, Fe-carb, Mg-carb, Mn-carb, Sr-carb, U-carb|488      |HNO3(1M/conc)   |HNO3(1M) and HNO3(conc)            |Q-ICP:MS                      |
|Ce-carb, Dy-carb, Er-carb, Eu-carb, Gd-carb, Ho-carb, La-carb, Lu-carb, Nd-carb, Pr-carb, REE-carb, Sm-carb, Tb-carb, Th-carb, Tm-carb, Y-carb, Yb-carb|271      |AcOH            |Acetic acid                        |ICP:MS                        |
|Ce-carb, Dy-carb, Er-carb, Eu-carb, Gd-carb, Ho-carb, La-carb, Lu-carb, Nd-carb, Pr-carb, REY-carb, Sm-carb, Tb-carb, Tm-carb, Y-carb, Yb-carb|256      |HNO3(5%)        |5% nitric acid                     |Q-ICP:MS                      |
|Ca-carb, Mg-carb, Mn-carb, Sr-carb|168      |AcOH(1N)        |1N acetic acid                     |ICP:ES                        |
|Ca-carb, Fe-carb, Mg-carb, Mn-carb, Sr-carb|141      |HCl(3N)         |3N hydrochloric acid               |AAS                           |
|Al-carb, Ba-carb, Ca-carb, Cr-carb, Fe-carb, K-carb, Mg-carb, Na-carb, Sr-carb|117      |HCl(6N)         |6N hydrochloric acid               |ICP:MS                        |
|Fe-carb      |114      |HCl(24h/cold)   |Cold HCl (1M or 10%) for 24hr (Raiswell et al. 1994)|ICP:MS                        |
|Ca-carb      |79       |NH4Ac(1M)       |1M ammonium acetate                |ICP:MS                        |
|Pb-carb, Th-carb, U-carb|42       |HNO3(5%)_AE(HBr-HCl)|5% HNO3, converted with HBr, anion exchange chromatography|Q-ICP:MS                      |

***

### Nitrogen and Phosphorus

**Phosphorus**

**Commonly cited method papers**

* Ruttenberg 1992 https://doi.org/10.4319/lo.1992.37.7.1460
* Thompson et al. 2019 https://doi.org/10.1016/j.chemgeo.2019.07.003

**Notes**

See the papers above for detailed discussion and figures illustrating methodological steps for SEDEX ("Sedimentary Extraction"). 

For **total phosphorus** see [Elements](https://github.com/ufarrell/sgp_phase2/wiki/C.-Analyses#elements) section below.

In SGP we have no code for the first SEDEX step, which is for modern sediments.

SGP codes for the older (Ruttenberg) method are 
* SeqAphos
* SeqBphos
* SeqCphos
* SeqDphos

SGP codes for the newer (Thompson) method are
* SeqAphos
* SeqBphos
* SeqCphos
* SeqDphos(mod)
* SeqEphos(mod)
* SeqFphos(mod)

The first three steps are shared. SeqFphos(mod) is the same procedure as SeqDphos, but in a different place sequentially. 

Any sum of components is stored in the proxy table, not presented on the website in Phase2. These include: 

* P-FeT = P-Fe1+P-mag+P-Fe2
* P-react = P-Fe+P-auth+P-org
* P-tot = P-Fe1+P-auth+P-mag+P-Fe2+P-det+P-org

There is variability in how analytes are reported in papers, especially P-fe/Fe1 and P-det.

SGP uses **P-Fe1** for the analyte measured from the first step (SeqAPhos), _whether or not_ the new or old sequential method is used (i.e. there can be studies where “P-Fe1” was measured but “P-Fe2” was not).

SGP uses **P-det** for the analyte measured from the third step (SeqCPhos), _whether or not_ the new or old sequential method is used. P-cryst and Px1 are variations in the literature: Thompson et al. 2019 state that _“The Pdet step of the original SEDEX procedure has been redefined as Pcryst, and represents crystalline apatite which may include recrystallized CFA as well as detrital apatite of igneous or metamorphic origin”_. Creveling et al. 2014 (pre-dating Thompson) use the variation Px1, and their method is described as a “modified version of Ruttenberg”. Bowyer et al. 2020 and 2023 cite the Thompson method but use P-det as the name.

One outlier method “SeqC+Ephos_Guilbaud” was added to account for a modification of Guilbaud et al. 2020. This method code might be changed if other similar data is added - for now this is the only example.


|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|P-Fe1(seq)   |524      |SeqAphos        |CDB pH 7.6 8h (Ruttenberg 1992, Thompson et al. 2019)|ICP:ES                        |
|P-auth(seq)  |613      |SeqBphos        |Na Acetate pH 4.0 6h (Ruttenberg 1992, Thompson et al. 2019)|MolyB                         |
|P-det(seq)   |538      |SeqCphos        |1M HCl 16hr (Ruttenberg 1992, Thompson et al. 2019)|MolyB                         |
|P-org(seq)   |225      |SeqDphos        |Ash 550decC, HCl (Ruttenberg 1992).|MolyB                         |
|P-mag(seq)   |362      |SeqDphos(mod)   |Ammonium oxalate 6h (Thompson et al. 2019)|ICP:ES                        |
|P-Fe2(seq)   |364      |SeqEphos(mod)   |CDA ph 4.8 6h (Thompson et al. 2019)|ICP:ES                        |
|P-org(seq)   |364      |SeqFphos(mod)   |Ash 550degC, 1M HCl 6h (Thompson et al. 2019)|MolyB                         |
|P-inorg      |38       |HCl(decarb)     |Decarbonated with HCl              |UV-Vis                        |
|P-det(seq)   |74       |SeqC+Ephos_Guilbaud|SeqC_phos + MA_5 after SeqD_phos   |MolyB                         |


**Nitrogen**

The majority of nitrogen isotopes in SGP are run using well-established methods (usually no method paper is cited). See above for carbon, often measured alongside. C:N ratios are atomic. N is usually measured along with the isotopes, and included here but see Element section below for other measurements of total N. 

The **reference standard** for nitrogen isotopes is Air.

**Proxy primer**

Dr. Eva Stüeken, Nitrogen isotopes https://youtu.be/2cNkWSPqMo4?si=I7rGSO8dHmWNvRcX

|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|C:N, DELTA_N15, N|5972     |HCl(decarb)     |Decarbonated with HCl              |CHNS-EA, EA, EA-CF-IRMS, EA-IRMS, IRMS|
|DELTA_N15_KER|132      |MA2b_ZnBr       |HCl/HF,  heavy liquid separation in ZnBr|EA-IRMS                       |
|C:N, DELTA_N15, N|126      |HCl(decarb)_MA2b|Decarbonated with HCl, HCl/HF      |EA-IRMS                       |
|DELTA_N15_KER|111      |SOX(DCM)_MA3    |Soxhlet dichloromethane-extraction, HF/HCl/HNO3|EA-IRMS                       |
|DELTA_N15, DELTA_N15_KER, N|78       |Decarb          |Decarbonated (no details provided) |EA-CF-IRMS, IRMS              |
|DELTA_N15_KER|61       |HCl(decarb)_HF/BF3|Decarb. with HCl, HF and BF3 for kerogen extraction (see Robl and Davis 1993, Stüecken et al. 2015)|EA-CF-IRMS                    |
|DELTA_N15_KER|51       |SOX(DCM)_MA2b   |Soxhlet dichloromethane-extraction, HF/HCl|EA-CF-IRMS                    |
|C:N, DELTA_N15, DELTA_N15_KER, N|3072     |NULL            |NULL                               |EA-CF-IRMS, EA-IRMS, IRMS, N/A|


***

### Metal Isotopes

Metal isotope analysis generally includes
* leach/digestion step
* a purification step (chromatography)
* measurement by ICP:MS-MC or TIMS/NTIMS
* analytical correction (double-spike/standard sample bracketing)
 
In SGP the experimental code aims to capture the digestion and purification steps in as much relevant detail as possible. Thus far we do not include information in the code itself about analytical correction methods (e.g. mass-bias correction) such as double-spike or standard sample bracketing. For the most part the approach used tends to be standardized within a given isotopic system; in some instances double-spike and bracketing are used in combination.

Given the methodological complexity and the inconsistency in how procedures are reported across the literature, some degree of compromise has been necessary. These codes are a work in progress, and feedback is welcome.

**Digestion**

SGP uses the same codes for this step as for elemental digests (see below) e.g. CB_MA3. If the digest is partial or light the strength of the acid is included e.g. HCl(0.25N). 

Steps between the initial digest and purification are difficult to code in a standardized way. These may include e.g. +/- HClO₄ +/-H₂O₂, secondary acid treatments, and various additional heating steps (e.g., microwave, ashing*). While these intermediate treatments often serve the same purpose (e.g. to prevent issues such as fluoride precipitation or to oxidize organics) they can vary in order, composition, and intensity across labs and publications. In some cases, it is not clear if these steps were included but not explicitly mentioned (authors may link to a citation which is ambiguous, or cite papers several layers deep). Users should be aware, therefore, that these steps are often not included in the code and we recommend consulting the original publications for details. 

*Note that if combustion/ashing is part of the initial digest, we do aim to include it in the code - we refer here to steps between initial digest and chromatography

**Purification**

In addition to the acid digest, the code captures the use of ion exchange (IE) or more specifically anion exchange (AE), cation exchange (CE), or a combination of both.

Where possible, we also attempt to capture the number of purification steps or columns. However, terminology in the literature is inconsistently applied: the term "step" may refer to either multiple elution stages on a single column, or to multiple columns used in sequence. Similarly, "stage" can be ambiguous (e.g., “two-stage” vs. “two-step”), and usage varies across isotope systems, and sometimes within a single isotope system (albeit less common).

As a result, SGP includes a numerical prefix (e.g., "2AE") where publications consistently refer to the number of steps, stages, or columns, and particularly if a distinction is explicitly drawn between methods within one isotope system.

Resins and eluents are generally not included in the purification code, as most isotope systems use standard combinations. However, resins are noted in the full experimental method description. When a non-standard resin is used (e.g., TRU resin instead of UTEVA for uranium), this is included in the code to highlight significant deviations from the norm.

**Isotope Dilution**

Element concentrations are sometimes/often measured alongside isotopes by isotope dilution methods. We note that, on occasion, it can be difficult to tell in a data table whether an element has been measured with the isotopes, or with other elements by e.g. standard acid-digest and ICP:MS etc.  

***

#### Calcium and Magnesium Isotopes

**Commonly cited method papers**

* Blättler et al., 2015 http://dx.doi.org/10.1016/j.epsl.2015.03.006
* Husson et al., 2015 http://dx.doi.org/10.1016/j.gca.2015.03.012
* Higgins et al., 2018 https://doi.org/10.1016/j.gca.2017.09.046
* Chakrabarti et al. 2021 https://doi.org/10.1016/j.chemgeo.2021.120398

**Notes**

For calcium and magnesium isotope analysis in carbonates, automated ion chromatography (e.g., Dionex systems) is commonly used. Some studies use traditional gravity-flow columns. SGP experimental codes include a numerical prefix (e.g. 2AE), to reflect “two-stage” and/or “two sets of columns”, when explicitly stated. 

The majority of studies in SGP so far use ICP:MS-MC.

**BioRad AG MP-50** is the standard resin used (variably reported as e.g. “MP 50”, "AG MP-50" etc.) 

The reference standard for calcium isotopes is **seawater** for studies in SGP so far - but note that other reference standards can be used. The reference standard for magnesium isotopes is DSM3 (from Dead Sea Magnesium Ltd., Israel).

**Proxy Primer**

Dr. Anne-Sofie Ahm, Calcium Isotopes: https://youtu.be/nQf2ykhpgpk?si=7D6OBwe1mr_tlO4v

|analyte(s)|count_res|code |translation             |ana_method(s)                   |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Ca44_Ca40_CARB, DELTA_Mg26_CARB|518      |AcOH(dil)_AIC   |Dilute acetic acid (no strength specified),  automated ion chromatography|ICP:MS-MC                     |
|DELTA_Ca44_Ca40_CARB, DELTA_Mg26_CARB|318      |AcOH(0.1N)_AIC  |0.1N acetic acid, automated ion chromatography|ICP:MS-MC                     |
|DELTA_Mg26_CARB|125      |HCl(1N)_2CE     |1N HCl, two-step cation ion exchange chromatography (AGMP-50 resin) |ICP:MS-MC                     |
|DELTA_Mg26_CARB|69       |HCl(1N)_AIC     |1N HCl, automated ion chromatography |ICP:MS-MC                     |
|DELTA_Mg26_CARB|39       |HCl(0.5N)_2CE   |0.5N HCl, two-step cation exchange chromatography (AGMP-50 resin)|ICP:MS-MC                     |
|DELTA_Ca44_Ca40_CARB|34       |HCl(0.5N)_CE    |0.5N HCl, cation exchange chromatography (AGMP-50 resin)|TIMS                          |
|DELTA_Mg26_CARB|13       |HCl(6N)_CE      |6N HCl, cation exchange chromatography (AGMP-50 resin)|ICP:MS-MC                     |

***

#### Cadmium Isotopes

**Commonly cited method papers**

Frederiksen et al. 2022 https://doi.org/10.1016/j.scitotenv.2021.150565

**Notes**

Thus far cadmium isotopes in SGP are from one paper (Fernandes et al. 2025 https://doi.org/10.1016/j.chemgeo.2024.122548) and measured along with chromium isotopes (see below). The resin used is **AG-1X8**.

The **reference standard** for cadmium isotopes is NIST SRM 3108.

|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Cd114_CARB|13       |HNO3(0.5M)_3AE  |0.5M HNO3, three step anion exchange chromatography (AG-1X8 resin) |TIMS                          |

***

#### Chromium Isotopes

**Commonly cited method papers**

* Schoenberg et al. 2008 https://doi.org/10.1016/j.chemgeo.2008.01.009
* Reinhard et al. 2014 https://doi.org/10.1016/j.epsl.2014.09.024
* Ball and Bassett, 2000  https://doi.org/10.1016/S0009-2541(00)00189-3
* Frei et al. 2011 https://doi.org/10.1016/j.epsl.2011.10.009 (carbonate)
* Gilleaudeau et al. 2016 https://doi.org/10.7185/geochemlet.1618

**Notes**

One approach to purification for chromium isotopes is a “three-step” procedure, although depending on the details, separation goals are slightly different.  
 
Anion exchange with AG1-X8 resin
* removal of Fe from the samples (Bauer et al. 2021 (Copenhagen))

Anion exchange (sometimes microcolumns are specified) with AG1-X8 resin
* V and Ti removed (Bauer et al. 2021 (Copenhagen))
* Traces of Fe removed/remove all remaining Fe (Bauer et al. 2021 (Yale), Mänd et al. 2022 (Yale))

Cation exchange with AG50W-X8 resin
* Cr separated from major matrix elements such as Ca, Mg, Mn and Al as well as residual Fe  (Bauer et al. 2021 (Copenhagen))
* to ensure complete Ti and Cr separation/to remove Ti (Bauer et al. 2021 (Yale), Mänd et al. 2022 (Yale))

In most cases treatment with ammonium persulfate (NH4)2S2O8 is explicitly mentioned, which is used to oxidise Cr(III) to Cr(VI) for retention on the AG1-X8 resin. In one example (Bauer et al. 2021, samples run at Yale) potassium peroxidisulfate (K2S2O8) is used. This oxidizing step either takes place prior to the first anion exchange step, or prior to the second.

In other papers, a two-step approach is used - anion followed by cation exchange.

The **reference standard** for chromium isotopes is NIST SRM 979.


|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Cr53   |46       |LMF_2AE/CE      |Lithium metaborate flux, anion (x2) and cation exchange chromatography|ICP:MS-MC                     |
|DELTA_Cr53   |41       |CB_MA3_2AE/CE   |Combustion/ashing, HNO3/HCl/HF, anion (x2) and cation exchange chromatography|ICP:MS-MC                     |
|DELTA_Cr53   |35       |MA2h_AE/CE      |HF/AR, anion and cation exchange chromatography|TIMS                          |
|DELTA_Cr53_CARB|44       |HCl(2N)_AE/CE   |2N HCl, anion and cation exchange chromatography|TIMS                          |
|DELTA_Cr53_CARB|18       |HCl(0.5N)_2AE/CE|0.5N HCl, anion (x2) and cation exchange chromatography|ICP:MS-MC                     |
|DELTA_Cr53_CARB|14       |HNO3(0.5M)_(3AE)_AE/CE|0.5M HNO3, (anion exchange for Cd), anion and cation exchange chromatography|TIMS                          |
|DELTA_Cr53_AUTH|18       |NULL            |NULL                               |CALC                          |

 
***

#### Copper and Zinc Isotopes

**Commonly cited method papers**

* Marechal et al. 1999 https://doi.org/10.1016/S0009-2541(98)00191-0
* Zhu et al. 2000 https://doi.org/10.1016/S0009-2541(99)00076-5
* Albarède and Marechal, 2002 https://doi.org/10.1016/S0016-7037(01)00815-8
* Albarède 2004 https://doi.org/10.1515/9781501509360-015

**Notes**

Thus far Cu and Zn isotopes in SGP are from one paper (Le Boudec et al. 2014 https://doi.org/10.1002/2013GC005068), measured alongside iron isotopes (see below). Sample-standard bracketing is used.

The **reference standards** used are NIST SRM 976 for copper and JMC 3-0749 for zinc.


|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Cu65, DELTA_Zn66|52       |CB_MA4_AE       |Combustion/ashing, HCl/HF, HClO4/HNO3, anion exchange chromatography (AG MP-1 resin)|ICP:MS-MC                     |
 
***

#### Iron Isotopes

**Commonly cited method papers**

* Weyer and Schwieters, 2003 https://doi.org/10.1016/S1387-3806(03)00078-2
* Arnold et al. 2004 https://doi.org/10.1021/ac034601v
* Schoenberg and von Blanckenburg 2005 https://doi.org/10.1016/j.ijms.2004.11.025
* Huang et al. 2011 https://doi.org/10.1016/j.gca.2011.03.036
* Swanner et al. 2015 https://doi.org/10.1016/j.gca.2015.05.024
* Kunzmann et al. 2017 http://dx.doi.org/10.1016/j.gca.2017.04.003

**Notes**

Standard method includes a total acid digest (usually with HF, usually with combustion/ashing first to remove organics), followed by anion exchange chromatography using AG1X8, AG1X4 or AGMP-1 resin. 

An intermediate acid step (e.g. taken up in HCl + heated) to ensure "complete dissolution of fluoride compounds" is sometimes described but not included in the code. 

The majority of studies use sample-standard bracketing (+/- in combination with an internal Cu "element spike"), with one exception using double-spike. The most commonly cited method paper is Arnold et al. 2004.

Fe-isotopes in pyrite were measured in two studies (Duan et al. 2010, Ostrander et al. 2022) after a sequential extraction. From Duan et al 2010: _"a sequential extraction was carried out to quantify the following three individual Fe pools and in preparation for iron isotope analysis of the pyrite (Raiswell et al., 1988; Canfield 1989; Huerta-Diaz and Morse, 1990; Raiswell et al., 1994 ): (1) Fe HCl : extracted using 12 N boiling HCl for 1 min to target all Fe oxides and some of the Fe in clays, followed by (2) Fe Si : 10 N HF for 16 h to extract all residual alumino-silicate Fe and (3) Fe Py : 16 N HNO 3 for 2h to extract all pyrite Fe"_.

The **reference standard** for iron isotopes is IRMM-14. 

|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Fe56   |145      |CB_MA3_AR_AE    |Combustion/ashing, HNO3/HCl/HF, aqua regia, anion exchange (AG1X4 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |125      |CB_MA3_AE       |Combustion/ashing, HNO3/HCl/HF, anion exchange (AG1X8 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |120      |MA3b_AR_AE      |HNO3/HF/HClO4, aqua regia, anion exchange chromatography (AGMP1 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |100      |MA3_AE          |HNO3/HCl/HF, anion exchange chromatography (AG1X8 or AGMP1 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |61       |CB_MA2_AE       |Combustion/ashing, HNO3/HF, anion exchange (AG1X8 or AGMP1 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |30       |MA2_AE          |HF/HNO3, anion exchange chromatography (AG1X8 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |26       |CB_MA4_AE       |Combustion/ashing, HCl/HF, HClO4/HNO3, anion exchange (AGMP1 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56   |16       |CB_MA2_AE(DS)   |Combustion/ashing, HF/HNO3, anion exchange chromatography Fe double-spike (Swanner et al. 2015)|ICP:MS-MC                     |
|DELTA_Fe56_AUTH|121      |NULL            |NULL                               |CALC                          |
|DELTA_Fe56_PY|19       |SeqPy_AE        |Seq extract of pyrite with HNO3, anion exchange (AGMP1 resin), sample-standard bracketing|ICP:MS-MC                     |
|DELTA_Fe56_PY|18       |CB_SeqPy_AE     |Combustion/ashing, seq extract py w/ HNO3, anion exchange (AG1X8 resin), sample-standard bracketing|ICP:MS-MC                     |
 
***

#### Lithium Isotopes

**Commonly cited method papers**

* Moriguti and Nakamura 1998 https://doi.org/10.1016/S0009-2541(97)00163-0
* James and Palmer 2000 http://dx.doi.org/10.1016/S0009-2541(99)00217-X
* Rudnick et al. 2004 https://doi.org/10.1016/j.chemgeo.2004.08.008
* Pogge von Strandmann et al. 2011 https://doi.org/10.1016/j.gca.2011.06.026 (+other Pogge von Strandmann papers, and refs therein - carbonates)
* Li et al. 2022 https://doi.org/10.1016/j.sab.2021.106348 (see for summary diagram of steps)

**Notes**

Digestion and pre-treatment for shales is a total acid digest with HF/HNO3/HClO4 followed by HNO3/HCl, in one case perchloric acid is used "as needed". 

To target the carbonate fraction, there is some variability in approach including dilute HCl treatment, 1 M sodium acetate buffered to pH 5 with acetic acid, or leach with ammonium acetate followed by a sequential leach in 0.05M HCl. See papers by Pogge von Strandmann et al. for discussion/evaluation of different approaches.

Li et al. 2022 provide a summary of chromatographic methods. Most studies in SGP use a two-column cation exchange procedure, with AG50W-X12 resin, one study follows a three-step procedure.

The **reference standard** for lithium isotopes is LSVEC.

|analyte(s)|count_res|code |translation             |ana_method(s)                   |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Li7    |93       |MA3b_3CE        |HF/HNO3/HClO4, HCl/HNO3, three cation exchange chromatography|ICP:MS-MC                     |
|DELTA_Li7    |34       |MA3b_2CE        |HF/HNO3/HClO4, HCl/HNO3, two-step cation exchange chromatography  (AG50W-X12 resin)|ICP:MS-MC                     |
|DELTA_Li7_CARB|78       |HCl(0.1N)_2CE   |0.1N HCl, two-stage cation exchange chromatography  (AG50W-X12 resin)|ICP:MS-MC                     |
|DELTA_Li7_CARB|58       |NH4Ac(1M)_HCl(0.05NSeq)_CE|1M ammonium acetate, 0.05N HCl in 4hr/2hr/10min seq. steps, cation exchange (AG50W-X12 resin)|ICP:MS-MC                     |
|DELTA_Li7_CARB|48       |NaOAc(1M)_2CE   |1M sodium acetate (AcOH buffered), two stage cation exchange chromatography  (AG50W-X12 resin)|ICP:MS-MC                     |
|DELTA_Li7_CARB|3        |MeOH_2CE        |Methanol/ultrasonic cleaning, two-stage cation exchange chromatography (AG50W-X12 resin)|ICP:MS-MC                     |

#### Molybdenum Isotopes

**Commonly cited method papers**

* Barling et al. 2001 https://doi.org/10.1016/S0012-821X(01)00514-3
* Siebert et al. 2001 https://doi.org/10.1029/2000GC000124
* Anbar 2004 https://doi.org/10.2138/gsrmg.55.1.429
* Arnold et al. 2004 https://doi.org/10.1126/science.1091785
* Johnson et al. 2004 https://doi-org.stanford.idm.oclc.org/10.1515/9781501509360
* Pearce et al. 2009 https://doi.org/10.1111/j.1751-908X.2009.00012.x (single column method)
* Zhang et. al. 2009 (Zhang, Y.X., Wen, H.J. and Fan, H.F. (2009) Chemical Pretreatment Methods for Measurement of Mo Isotope Ratio on Geological Samples. Chinese Journal Anal. Chemistry, 37, 216-220.)
* Voegelin et al. 2009 https://doi.org/10.1016/j.chemgeo.2009.05.015 (carbonates)
* Duan et al., 2010 https://doi.org/10.1016/j.gca.2010.08.035
* Wen et al. 2011 https://doi.org/10.1130/G32055.1 
* Greber et al. 2012 https://doi.org/10.1111/j.1751-908X.2012.00160.x
* Nägler et al. 2013 https://doi.org/10.1111/j.1751-908X.2013.00275.x (standards)
* Goldberg et al. 2013 https://doi.org/10.1039/c3ja30375f (standards)
* Wille et al. 2013 http://dx.doi.org/10.1016/j.chemgeo.2012.12.018
* Li et al. 2014: https://doi.org/10.1111/j.1751-908X.2013.00279.x
* Romaniello et al. 2016 https://doi.org/10.1016/j.chemgeo.2016.05.019 (carbonates)
* Thoby et al. 2019 https://doi.org/10.1130/G45706.1 (carbonates)

**Notes**

The majority of the molybdenum isotopes in SGP are from a total acid digest (with or without a combustion/ashing initial step), followed by a two-step chromatographic procedure: anion exchange (with AG1-X8 resin) and cation exchange (with AG50W-X8), referencing e.g. Barling et al. 2001 and Duan et al. 2010. 

Scheller et al. 2018 (https://doi.org/10.1016/j.precamres.2017.12.009) use a reverse-aqua regia digest and a single-column approach, referencing Pearce et al. 2009.

Three studies - Luo et al. 2021, Hodgskiss et al. 2021, O'Sullivan et al. 2022 - have molybdenum isotopes from carbonate fractions, after a (relatively) light digest. 

Most studies use a double-spike to correct for fractionation during chromatography and to correct for mass-bias. Some studies use sample-standard bracketing, and some compare both double-spike and sample-standard bracketing. 

The **reference standards** used for molybdenum isotopes have been variable through time, with older studies tending to use a variety of in-house standards (e.g. RochMo2, various other Johnson Matthey (JMC) Specpure ICP Mo standard solutions). Most studies now report measurements relative to NIST SRM 3134 "where the standard NIST 3134 = 0.25permil".  See Goldberg et al. 2013 and Nägler et al. 2013 for discussion. Five studies older than 2013 in SGP use RochMo2, JMC Specpure lot#702499I and JMC-Mo Sie lot#602332B.



|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Mo98   |911      |CB_MA3_AE/CE    |Combustion/ashing, HNO3/HCl/HF, anion exchange (most AG1-X8 resin), cation exchange (AG50W-X8 resin)|ICP:MS-MC                     |
|DELTA_Mo98   |180      |CB_MA2_AE/CE    |Combustion/ashing, HNO3/HF, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)|ICP:MS-MC                     |
|DELTA_Mo98   |161      |MA3_AE/CE       |HNO3/HCl/HF, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)|ICP:MS-MC                     |
|DELTA_Mo98   |26       |CB_HCl(conc/boil)_AE|Combustion/ashing, concentrated boiling HCl (3 times), anion exchange chromatography (AG1-X8 resin)|ICP:MS-MC                     |
|DELTA_Mo98   |21       |MA2_AE/CE       |HNO3/HF, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)|ICP:MS-MC                     |
|DELTA_Mo98   |12       |ARrev_AE        |Reverse aqua regia digest, anion exchange chromatography (AG1-X8) (see Pearce et al. 2009)|ICP:MS-MC                     |
|DELTA_Mo98_CARB|148      |HCl(6N)_AE/CE   |6N HCl, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)|ICP:MS-MC                     |
|DELTA_Mo98_CARB|49       |HCl(6N)_BHPA    |6N HCl, BHPA resin chromatography (see Li et al. 2014)|ICP:MS-MC                     |
|DELTA_Mo98, DELTA_Mo98_AUTH|236      |NULL            |NULL                               |CALC, ICP:MS-MC               |

#### Selenium Isotope

**Commonly cited method papers**

* Stüeken et al. 2013 https://doi.org/10.1039/C3JA50186H

**Notes**

Most studies in SGP with selenium isotopes are based on the methods of Stüeken et al. 2013 - refer to that paper for detailed description and diagram of steps. 

|analyte(s)   |count_res|code            |translation                        |ana_method(s)                 |
|-------------|---------|----------------|-----------------------------------|------------------------------|
|DELTA_Se82_Se78|198      |MA3b_TCF_AR     |HF/HClO4/HNO3, TCF filter, Aqua Regia (Method E of Stüeken et al. 2013)|ICP:MS-MC                     |
|DELTA_Se82_Se78|100      |MA3b_TCF        |HF/HClO4/HNO3, TCF filter (Method D of Stüeken et al. 2013)|ICP:MS-MC                     |
|DELTA_Se82_Se78|4        |MA3b_TCF+/-AR   |HF/HClO4/HNO3, TCF filter +/- Aqua regia (Average of Method D and Method E of Stüeken et al. 2013)|ICP:MS-MC                     |

#### Uranium Isotopes

**Commonly cited method papers**

* Potter et al. 2005 https://doi.org/10.1016/j.ijms.2005.08.017
* Stirling et al. 2007 https://doi.org/10.1016/j.epsl.2007.09.019 
* Weyer et al. 2008 https://doi.org/10.1016/j.gca.2007.11.012 
* Brennecka et al., 2011 https://doi.org/10.1073/pnas.1106039108
* Kendall et al. 2013 https://doi.org/10.1016/j.chemgeo.2013.08.010
* Dang et al. 2016 https://doi.org/10.1021/acs.est.6b01459
* Lau et al. 2016 https://doi.org/10.1073/pnas.1515080113
* Wang et al. 2016 https://doi.org/10.2475/01.2016.02
* White et al. 2018 https://doi.org/10.1016/j.epsl.2018.09.020 (incl. 1M HNO3 leach)
* Clarkson et al. 2018  https://doi.org/10.1073/pnas.1715278115 (incl. ox-red cleaning procedure)
* Dang et al. 2018 https://doi.org/10.1016/j.scitotenv.2017.08.156
* Lau et al. 2019 https://doi.org/10.1017/9781108584142
* Clarkson et al. 2020  https://doi.org/10.1016/j.chemgeo.2019.119412 (carbonate)
* Zhang et al. 2020 https://doi.org/10.1016/j.gca.2020.05.011 (carbonate)
* Kalderon-Asael et al. 2021 https://doi.org/10.1038/s41586-021-03612-1 (leaching procedure for carbonates)
* Dang et al. 2022 https://doi.org/10.1016/j.chemgeo.2021.120644 (authigenic)

**Notes**

Uranium isotopes in SGP are relatively evenly divided between total/bulk and carbonate-specific measurements, with rare examples coded as authigenic. Bulk isotopes are determined after a strong acid digest (often with a combustion/ashing step) and carbonate isotopes (and one authigenic) after a light or moderate acid digest.

White et al. 2018, and subsequent related papers, describe a procedure where the "sample powder was digested at room temperature by adding 20 mL of 1M HNO3, followed by the slow addition of 3 mL of concentrated HNO3 to replace the acid neutralized by reaction with CaCO". This is coded simply as HNO3(1M).

Authigenic uranium isotopes in SGP come from two studies so far. Those from Lu et al. 2020 are calculated relative to PAAS. Those from Dang et al. 2022 are measured after an aqua regia leach - see Dang et al. 2022 for discussion of authigenic components generally.

_Additional steps not coded_
As discussed above, many protocols include pre-digest cleaning steps, intermediate treatments, or post-column-chemistry steps, often with similar aims, which are _not coded_ for. For example:
* a pre-digest cleaning step described in Tostevin et al. 2019, based on Clarkson et al. 2018: "two-step reductive and oxidative cleaning procedure to remove potential Mn-oxides and residual organic matter"
* an intermediate treatment described in Dang et al. 2022 (after initial acid digest): "Clear solutions were dried at 95degC before samples were redissolved in 4 mL HCl. The solutions were dried again and a second 4 mL of HCl were added. These steps were designed to dissolve any fluoride precipitate. If needed (brown-colored solutions), 0.5 to 2 mL of H2O2 was added in HCl acid media to oxidize any residual organic content"
* a similar intermediate treatment described in White et al. 2018, and related papers (after initial 1M HNO3 digest): " Spiked samples were subsequently dried down to equilibrate the spike mixture, and the residue was treated with a solution of 0.3 mL 32% H2O2 and 2 mL concentrated HNO3 at ~100°C for one hour to oxidize any residual organic carbon leached from the samples prior to column chemistry."
* a post-column chemistry step described in Lu et al. 2023: "After column chemistry, samples were treated with both concentrated HNO3 and 30% H2O2 (hydrogen peroxide) twice to break down any residual organic matter from the resin"

_Chromatography/Purification_

By far the most commonly used **resin** is Triskem/Eichrom UTEVA. Others use TRU or RE resins, these are specified in the code. 

In some cases, it is explicitly stated that two column steps/two column passes were used, and this is included in the code. In some cases, two steps are described with different resins, for example 
* anion exchange with AG1X8 resin, preceding ion exchange with UTEVA in Clarkson et al. 2021
* ion exchange with DGA resin ("to remove excess Na"), after ion exchange with UTEVA e.g. Cheng et al. 2020, Remirez et al. 2024.

Double-spike (usually IRMM-3636 236U-233U, sometimes in-house) is used to correct for U isotope fractionation during the column chemistry and instrumental mass bias. Sample-standard bracketing is also commonly used.

In SGP the **reference standard** used so far for uranium isotopes is CRM-145/CRM-112a, and in one instance NIST SRM 950a (Kendall et al. 2013 http://dx.doi.org/10.1016/j.chemgeo.2013.08.010, with the following noted: "We report the U isotope composition of each sample relative to the SRM950a standard as  δ238U [‰] = [238/235Usample / 238/235USRM950a − 1] × 1000. We have determined that standard CRM145 (also known as CRM112a; Telus et al., 2012) has a statistically identical U isotope composition compared to SRM950a (δ238U = 0.04 ± 0.06‰; 2SD, n = 38), in agreement with initial results reported by Weyer et al. (2008)."

**Proxy Primer**

Dr. Kimberly Lau, Uranium Isotopes https://www.youtube.com/watch?v=tg7Zf6hjaMI

|analyte(s)     |count_res|code                  |translation                                                                                     |ana_method(s)|
|---------------|---------|----------------------|------------------------------------------------------------------------------------------------|-------------|
|DELTA_U238     |252      |CB_MA3_IE             |Combustion/ashing, HNO3/HCl/HF digest, ion exchange chromatography (UTEVA resin)                |ICP:MS-MC    |
|DELTA_U238     |53       |CB_MA3d_IE            |Combustion/ashing, HNO3/HF, aqua regia, ion exchange chromatography (UTEVA resin)               |ICP:MS-MC    |
|DELTA_U238     |30       |MA3b_IE               |HF/HNO3/HClO4, ion exchange chromatography (UTEVA resin)                                        |ICP:MS-MC    |
|DELTA_U238     |29       |MA4_IE(TRUresin)      |HF/HCl/HNO3/HClO4, ion exchange separation (TRU resin)                                          |ICP:MS-MC    |
|DELTA_U238     |27       |MA3_IE                |HF/HNO3/HCl, ion exchange chromatography (UTEVA resin)                                          |ICP:MS-MC    |
|DELTA_U238     |9        |CB_MA3d_2IE           |Combustion/ashing, HNO3/HF, aqua regia, ion exchange chromatography (x2)(UTEVA resin)           |ICP:MS-MC    |
|DELTA_U238_CARB|193      |HNO3(1M)_IE           |1M HNO3, ion exchange chromatography (UTEVA resin)                                              |ICP:MS-MC    |
|DELTA_U238_CARB|133      |NaOAc(1M)_IE          |1M sodium acetate, ion exchange chromatography (UTEVA resin)                                    |ICP:MS-MC    |
|DELTA_U238_CARB|127      |HCl(1N)_2IE           |1N HCl, two-step ion exchange chromatography (UTEVA resin)                                      |ICP:MS-MC    |
|DELTA_U238_CARB|112      |HCl(0.25N)_2IE        |0.25N HCl, two-step ion exchange chromatography (UTEVA resin)                                   |ICP:MS-MC    |
|DELTA_U238_CARB|107      |HNO3(1M)_2IE          |1M HNO3, 2 x ion exchange chromatography (UTEVA)                                                |ICP:MS-MC    |
|DELTA_U238_CARB|83       |HCl(1N)_IE            |1N HCl, ion exchange chromatography (UTEVA resin)                                               |ICP:MS-MC    |
|DELTA_U238_CARB|82       |HNO3(1M)_IE/AIC       |1M HNO3, ion exchange chromatography (UTEVA) + automated ion chromatography (DGA resin)         |ICP:MS-MC    |
|DELTA_U238_CARB|78       |NH4Ac(1M)_2IE(REresin)|NH4Ac(1M), ion exchange chromatography (RE resin)                                               |ICP:MS-MC    |
|DELTA_U238_CARB|40       |HCl(0.1NSeq)_2IE      |0.1N HCl in 4hr, 2hr, 10min sequential steps, two-step ion exchange chromatography (UTEVA resin)|ICP:MS-MC    |
|DELTA_U238_CARB|17       |AcOH(0.5M)_AE/IE      |0.5N acetic acid, anion exchange (AG1X8 resin) ion exchange chromatography (UTEVA resin)        |ICP:MS-MC    |
|DELTA_U238_AUTH|146      |AR_IE(TRUresin)       |Aqua regia, ion exchange chromatography (TRU resin)                                             |ICP:MS-MC    |
|DELTA_U238_AUTH|23       |NULL                  |NULL                                                                                            |CALC         |

#### Vanadium Isotopes 

**Commonly cited method papers**

* Nielsen et al. 2011 https://doi.org/10.1111/j.1751-908X.2011.00106.x
* Nielsen et al. 2016 https://doi.org/10.1039/C5JA00397K
* Nielsen et al. 2019 https://doi.org/10.1016/j.epsl.2018.10.029

**Notes**

Thus far SGP contains data from one study, Heard et al. 2023 https://doi.org/10.1016/j.epsl.2023.118127, who used standard protocols from Woods Hole Oceanographic Institute. 

The **reference standard** used is Alfa Aesar (AA) V specpure standard.

|analyte(s)     |count_res|code                  |translation                                                                                     |ana_method(s)|
|---------------|---------|----------------------|------------------------------------------------------------------------------------------------|-------------|
|DELTA_V51_AUTH |18       |HNO3(2M)_CE/3AE       |2M HNO3, cation (AG50WX12 resin) and 3x anion exchange chromatography (AG1X8 resin). WHOI method.|ICP:MS-MC    |


#### Samarium-Neodymium Isotopes 

**Commonly cited method papers**

* Pin and Zalduegui 1997 https://doi.org/10.1016/S0003-2670(96)00499-0

**Notes**

Preparation for Sm-Nd isotopes generally involves a combustion/ashing step, strong multi-acid digest, usually heated, usually in multiple stages, and chromatography:
 
* anion exchange, AG1X8 resin to remove iron (not always mentioned)
* cation exchange, Eichrom TRU resin or Bio-Rad AG50W, to remove REE 
* cation exchange, Eichrom LN resin, for Sm and Nd.

In one example (Maloney et al. 2024), the strong acid digest is preceded by treatment in acetic acid to remove carbonate. In another example  (Mundl et al. 2018), the sample is digested using flux fusion, and only the last chromatography step is mentioned (cation with LN resin for Sm and Nd).

**εNd(0)** (aka εNd) is the present-day deviation of the sample from CHUR, defined as follows: εNd = [(143Nd/144Nd)sample – (143Nd/144Nd)CHUR] – 1 * 10000

**εNd(t)**. As described in Maloney et al. 2024: "values are commonly presented as a function of age where both the sample and CHUR 143Nd/144Nd ratios are corrected for 143Nd ingrowth since the time the rocks were deposited.". The age used is stored in the database, but not yet available on the website - refer to original publications for details. 

**εNdi** = Initial ɛNd at time of rock formation

|analytes                                        |count_res|code                     |translation                                                                                   |ana_methods   |
|------------------------------------------------|---------|-------------------------|----------------------------------------------------------------------------------------------|--------------|
|Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0)        |70       |MA2_2CE                  |HF/HNO3, two-step cation exchange chromatography (Sm Nd with LN resin)                        |ID-NTIMS, TIMS|
|Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(t)        |30       |LTMF_CE                  |Lithium tetraborate/metaborate fusion, cation exchange chromatography (LN resin)              |ID-NTIMS, TIMS|
|Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0), eNd(t)|72       |CB_AcOH_MA2_AR/HCl_AE/2CE|Ash, AcOH decarb, HF/HNO3, aqua regia, HCl, chrom. (anion AG1X8,  cation TRU, cation LN)      |ICP:MS-MC     |
|Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0), eNd(t)|168      |CB_MA2_HCl/HNO3_AE/2CE   |Combustion/ashing, HF/HNO3, HCl/HNO3, 3step chrom (anion AG1X8,  cation TRU, cation LN)       |ICP:MS-MC     |
|Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNdi          |250      |CB_MA3_AE/2CE     |Combustion/ashing, HF/HNO3, aqua regia, HCl, 3step chrom. (anion AG1X8, cation TRU, cation LN)|TIMS/ICP:MS-MC|
|Nd, Nd143_Nd144, Sm, Sm147_Nd144, eNd(0), eNd(t)|90       |CB_MA2_HCl/HNO3_2CE      |Combustion/ashing, HF/HNO3, HCl/HNO3, cation ex. chrom x 2 (AG50W for REE, LN resin for Sm Nd)|ID-NTIMS, TIMS|

#### Rhenium-Osmium Isotopes

**Commonly cited method papers**

* Creaser et al. 2002 https://doi.org/10.1016/S0016-7037(02)00939-0
* Selby and Creaser 2003 https://doi:10.1016/S0009-2541(03)00199-2
* Selby 2007 (Norwegian Journal of Geology, vol. 87, pp. 291-299)
* Kendall et al. 2004 https://doi:10.1016/j.epsl.2004.04.004
* Xu et al. 2009 https://doi.org/10.1016/j.epsl.2009.10.022
* Georgiev et al. 2012 https://doi.org/10.1016/j.chemgeo.2012.01.003
* Cumming et al. 2013 https://doi.org/10.1130/G34299.1
* Puchtel et al. 2014 https://doi.org/10.1016/j.gca.2013.10.013

**Notes**

Selby and Creaser (2003) is the most commonly cited paper, see for detailed description of methods. The standard protocol involves Carius-tube digestion with 185Re and 190Os spike/tracer in CrVIO3-H2SO4 solution. Osmium is purified by solvent extraction using chloroform then back-extracted into concentrated HBr and then further purified by micro-distillation. Rhenium is purified using anion exchange chromatography. Re and Os are then analysed by NTIMS (Ni filament for Re, Pt filament for Os).

One exception is Chen et al. 2016, measuring Re-Os isotopes alongside PGE. In that case, digestion was "conducted in a mixture of 2.5 mL of triple-distilled, concentrated HCl and 5 mL triple-distilled, concentrated HNO3". 

Os187_Os188(I) (on the website as "Osi") = initial 187Os/188Os isotope ratio

**Proxy Primer**

Dr. Alan Rooney, Re-Os geochronology and Os isotopes https://www.youtube.com/watch?v=pFRMgyohXbo

|analytes                                        |count_res|code                     |translation                                                                                   |ana_methods   |
|------------------------------------------------|---------|-------------------------|----------------------------------------------------------------------------------------------|--------------|
|192Os, Os, Os187_Os188, Re, Re187_Os188         |1011     |Carius(CrVI-H2S04)_SE/MD/AE|Carius tube digest CrVI-H2SO4, solvent extract./microdist./anion ex. chrom. (Selby and Creaser 2003)|ICP:MS, ID-NTIMS, NTIMS|
|Os, Os187_Os188, Re, Re187_Os188                |104      |Carius(HCl/HNO3)_SE/MD/AE|Carius tube digest HCl/HNO3, solvent extract./microdist/anion exchange chromatography         |ICP:MS, NTIMS |
|Osi                                  |219      |NULL                     |NULL                                                                                          |CALC          |

#### Strontium Isotopes

**Commonly cited method papers**

* Horwitz et al. 1992  https://doi.org/10.1080/07366299208918107
* Frei et al. 2011 https://doi.org/10.1016/j.epsl.2011.10.009
* Erban Kochergina et al. 2022 http://dx.doi.org/10.3190/jgeosci.357

**Notes**

Many studies do not cite a method paper, so the selection above may be limited. See Chen et al. 2023 https://doi.org/10.1111/ggr.12531 and the Proxy Primer linked below for in-depth discussion of methodology and leaching protocols in particular. 

**Proxy Primer**

Dr. Graham Shields and Dr. Ying Zhou https://youtu.be/kVmntRYaap8?si=ohzDhT7iWXS18MSw


|analyte(s)                                        |count_res|code                     |translation                                                                                   |ana_method(s)   |
|------------------------------------------------|---------|-------------------------|----------------------------------------------------------------------------------------------|--------------|
|Sr87_Sr86                                       |86       |HCl(1N)_CE               |1N HCl, cation exchange chromatography (AG 50W X12 resin)                                     |TIMS          |
|Sr87_Sr86                                       |65       |HCl(0.6N)_CE             |0.6N HCl, cation exchange chromatography (AG 50W X12 resin)                                   |TIMS          |
|Sr87_Sr86                                       |62       |MeOH_NH4OAc(0.2M)_AcOH(0.5M)_CE|Methanol, 0.2M ammonium acetate, 0.5M acetic acid, cation exchange (Sr Spec resin)            |TIMS          |
|Sr87_Sr86                                       |44       |NH4Ac(0.2M)_AcOH(0.5M)_CE|0.2M ammonium acetate, 0.5M acetic acid, cation exchange (Sr Spec resin)                      |TIMS          |
|Sr87_Sr86                                       |44       |HCl(2N)_CE               |2N HCl, cation exchange chromatography (Sr Spec resin)                                        |TIMS          |
|Sr87_Sr86                                       |14       |HNO3(0.5M)_CE   |0.5M HNO3, cation exchange chromatography (Sr Spec resin)                            |TIMS          |
|Sr87_Sr86                                       |11       |NULL                     |NULL                                                                                          |TIMS          |

#### Thallium isotopes

**Commonly cited method papers**

* Rehkämper and Halliday, 1999 https://doi.org/10.1016/S0016-7037(98)00312-3
* Nielsen et al., 2004 https://doi.org/10.1016/j.chemgeo.2003.11.006
* Nielsen et al. 2011 https://doi.org/10.1016/j.gca.2011.07.047
* Owens et al., 2017 http://dx.doi.org/10.1016/j.gca.2017.06.041
* Owens et al. 2019 https://doi.org/10.1017/9781108688697
* Wang et al. 2023 https://doi.org/10.1016/j.chemgeo.2023.121457 (a newer method - all SGP data entered so far are older than this paper)

**Notes**

For all studies in SGP the digestion procedure starts with a standard step: 2M HNO3 for 12hrs at 130deg. This is used to separate authigenic Tl bound to pyrite from detrital Tl. One study subsequently uses a HNO3/HF digest on the residue left from this step, in order to determine authigenic Tl.

The next steps to remove organics (from the supernatant) are variable, involving acids (e.g. HNO3/HCl/AR/reverse-AR in various combinations), ashing and/or microwave, and +/-H2O2. These steps are not included in the code.

In preparation for column chemistry a treatment with 1M HCl +/- brominated H2O is usually applied which is also not coded. This appears to be almost universal, although “brominated H2O” is not always mentioned.

The primary distinction in the purification step is between one or two columns:
* One-column - newer approach “shown to work well for high Tl and low Pb samples”
* Two-column - the standard older approach e.g. “thallium purification was accomplished using two separate columns, one large and one micro-column, using AG1X8 anion exchange resin from Biorad.” (Owens et al. 2017).


|analyte(s)                                        |count_res|code                     |translation                                                                                   |ana_method(s)   |
|------------------------------------------------|---------|-------------------------|----------------------------------------------------------------------------------------------|--------------|
|Tl-auth, e205Tl-auth                            |785      |HNO3(2M)_AE              |2M HNO3, one-column anion exchange chromatography (AG1X8 resin)                               |ICP:MS-MC     |
|Tl-auth, e205Tl-auth                            |296      |HNO3(2M)_2AE             |2M HNO3, two-column anion exchange chromatography (AG1X8 resin)                               |ICP:MS, ICP:MS-MC|
|e205Tl-det                                      |13       |HNO3(2M)_MA2_2AE         |2M HNO3, HNO3/HF, two-column anion exchange chromatography (AG1X8 resin)                      |ICP:MS-MC     |


### Elements 

Analysis of elemental concentrations by ICP:MS, ICP:ES or XRF make up the majority of data in SGP.

#### ICP:MS/ICP:ES/Other

**Notes**

Many of these analyses are run using standard procedures at commercial laboratories, and some of the initial experimental codes were based on those protocols (e.g MA4 for a four-acid digest from Bureau Veritas Labs). The digestion protocol chosen will depend on the rock type, target elements and analytical method. 

_Combustion/ashing_

The code ‘CB’ (previously ‘CBST’) has been used as a catch-all for combustion or ashing at a range of temperatures, and is a common prefix for multi-acid digests, indicating a heating step used to oxidize organics. The most common temperature is around 500/550 degrees C, which should perhaps more accurately be called ashing, especially since it is the ash powder that is used for the next step of the analysis. However, there are also examples of treatment up to 900 degrees C, or acid treatment after “LOI”, and for now all of these are lumped in together. ‘Calcination’ is also sometimes specified, and lumped in with the ‘CB’ code.

_Fusion_

Flux **fusion** (usually with lithium borate of some description) is a common digestion method. Note that the base codes for fusion digestion methods are generally the same, whether or not a glass bead is prepared for XRF (see below) or a subsequent acid digestion is used to prepare the sample for ICP:MS. (One exception specifies the HNO3 digest prior to ICP:MS, since the information was available).

_Multi-acid digestion_

The other common experimental method is **multi acid digestion**. The specific acids used are listed in the exp_method_translation. The acid-digestion steps described here are generally aiming for **total or near-total digestion**, and the use of strong acids is assumed  - by contrast, see Carbonate Proxies above where the acid strength is an important component of the experimental code.

Note that the experimental codes allow for the distinction between multiple sequentially administered acid digestion steps, separated by an underscore, but these steps may be short-handed elsewhere as e.g. "a standard X-acid digestion". This can lead to a mix of specific and general classifications, depending on how the procedures were described in the original publications. The choice of code/code creation has been a balance between a) distinguishing meaningfully different methods where possible, and b) speed of data entry - sometimes it is easier to code individual steps if they are specified, and lump them in with a "standard" procedure later.

As an example, all of the following methods are currently coded as "CB_MA3", but note the difference in steps, combinations of acids, and specificity. Previously some of these were coded as "CB_MA2_AR_HCl", where MA2 corresponds to HNO3/HF a common two-acid digestion used elsewhere.

* Approximately 100 mg of powder was ashed overnight at 550°C to oxidize organic matter. Ashed powders were digested at 110°C in 2.5 ml concentrated HNO3 and 0.5 ml concentrated HF for 48 h, followed by digestion in 4 ml aqua regia for 48 h and finally in 2 ml concentrated HCl for 24 h (Kunert and Kendall 2023). 
* Finely powdered samples were first ashed at 550°C overnight to remove volatiles, and the loss on ignition was recorded and used later to correct elemental abundances for the original sample weight. 10-20 mg of ashed sample was then dissolved using a **standard multi-acid (HNO3-HCl-HF) digestion** (Kendall et al., 2010). The digestion procedure involved progressive acid treatments at ~150°C in Savillex Teflon bombs with HF-NHO3, aqua regia (HNO3-HCl), and finally, HCl. A subset of samples was processed using perchloric acid (HClO4) to digest organic matter, rather than loss on ignition (Guilleaudeau and Kah 2013).
* Powdered sample splits were ashed for 8-10 h at 550°C and dissolved by HF-HNO3-HCl acid digestion (Sahoo et al. 2016). 
* In short, powdered samples were ashed overnight in a muffled furnace at 550°C to help rid samples of organic material. Then, each sample was transferred to a trace metal clean lab and subjected to multiple rounds of concentrated acid digestion using trace metal grade hydrofluoric, hydrochloric, and nitric acid (Ostrander et al. 2020).
* Concentrations of total Fe (FeT) and Mo were measured using **a standard multi-acid digestion (HNO3-HCl-HF)** as follows. Distilled HNO3 and HCl and trace-metal grade HF reagents were used in all cases. An aliquot of powdered sample was weighed into a porcelain crucible, ashed at 850°C for 12 h, and weighed again after cooling. The mass lost on ignition (LOI) was recorded and used later for correction of the elemental abundances. About 100 mg of ashed sample were weighed accurately in a 15 ml Savillex Teflon bomb equipped with a screw cap. The sample was first digested by adding ~0.2 ml water and ~ 1 ml concentrated HNO3 and heated at 200°C for 2 h. The sample was then transferred to a sterile 15 ml centrifuge tube after cooling and spun at 6,000 r.p.m. for 5 min. The supernatant was removed and retained, while the residual undigested sample was returned to the Teflon bomb. The purpose of this step was to remove cations such as Ca2+ (primarily from carbonates) that can form insoluble fluoride precipitates during reaction with HF. This step was repeated for carbonate-rich samples (usually >30pct). The sample residue was further digested by adding ~0.2 ml water and ~ 1 ml HNO3/HF (1:2) and heated at 200°C for at least 24 h. The sample was subsequently dried down in order to evaporate the acids. The last digestion was in ~0.2 ml water and ~1 ml concentrated HCl, which was heated at 200°C for at least 2 h. If the rock powders were not completely digested after this treatment, additional rounds of digestion were performed (Li et al. 2012).




|analyte(s)                                      |count_res|code                     |translation                                                                                   |ana_method(s) |
|------------------------------------------------|---------|-------------------------|----------------------------------------------------------------------------------------------|--------------|
|Ag, Al, As, Au, B, Ba, Be, Bi, Ca, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Hg, Ho, In, K, La, Li, Lu, Mg, Mn, Mo, Na, Nb, Nd, Ni, Pb, Pr, Rb, Re, Sb, Sc, Se, Si, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|488707   |Tot_digest               |Total digestion (NGDB method)                                                                 |COLOR, ICP:ES, ICP:MS, N/A|
|Ag, Al, Al2O3, As, Au, B, Ba, Be, Bi, Ca, CaO, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Hg, Ho, In, K, K2O, LREE, La, Li, Lu, MREE, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Pr, REY, Rb, Re, Sb, Sc, Se, Si, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|473173   |MA4                      |HNO3/HClO4/HF/HCl                                                                             |ICP:ES, ICP:ES/MS, ICP:MS, Q-ICP:MS, QQQ-ICP:MS|
|Ag, Al, Al2O3, Ba, Be, Ca, CaO, Ce, Co, Cr, Cr2O3, Cs, Cu, Dy, Er, Eu, Ga, Gd, Hf, Ho, K, K2O, La, Lu, Mg, MgO, Mn, MnO, Na, Na2O, Nb, Nd, Ni, Pb, Pr, Rb, Sc, Si, SiO2, Sm, Sn, Sr, Ta, Tb, Th, Ti, TiO2, Tm, U, V, W, Y, Yb, Zn, Zr|125067   |LTF                      |Lithium tetraborate (aka lithium borate) fusion                                               |ICP, ICP:ES, ICP:MS|
|Ag, Al, As, Au, B, Ba, Be, Bi, Ca, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Hg, Ho, In, K, La, Li, Lu, Mg, Mn, Mo, Na, Nb, Nd, Ni, Pb, Pd, Pr, Pt, Rb, Re, Sb, Sc, Se, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|117786   |AR                       |Aqua regia (3:1 HCl:HNO3)                                                                     |AAS, ICP:ES/MS, ICP:MS|
|Ag, Al2O3, As, Ba, Be, CaO, Cd, Ce, Co, Cr, Cr2O3, Cs, Cu, Dy, Er, Eu, Ga, Gd, Hf, Ho, K2O, La, Lu, MgO, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Pr, Rb, Sb, Sc, SiO2, Sm, Sn, Sr, Ta, Tb, Th, TiO2, Tm, U, V, W, Y, Yb, Zn, Zr|93758    |LMF_HNO3(5%)             |Lithium metaborate fusion, 5% HNO3 (see e.g. Bureau Veritas method 4A-4B)                     |ICP, ICP:ES, ICP:ES/MS, ICP:MS|
|Ag, Al, Al2O3, As, B, Ba, Be, Bi, Ca, CaO, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, In, K, K2O, La, Li, Lu, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Pr, REE, Rb, Re, Sb, Sc, Se, Si, SiO2, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|61417    |Na2O2Fus                 |Sodium peroxide sinter/fusion                                                                 |ICP:ES, ICP:ES/MS, ICP:MS|
|Ag, Al, Al2O3, As, Au, B, Ba, Be, Bi, Ca, CaO, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Hg, Ho, In, K, K2O, La, Li, Lu, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Pd, Pr, Pt, Rb, Re, Sb, Sc, Se, Si, SiO2, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|34429    |Digest                   |Unspecified digestion (CMIBS method)                                                          |AAS, COUL, DCP-OES, FLOUR, ICP:ES, ICP:MS, ICP:MS-ID, WC|
|Al, Al2O3, Ba, Be, Ca, CaO, Ce, Co, Cr, Cr2O3, Cs, Cu, Dy, Er, Eu, Ga, Gd, HREE, Hf, Ho, K2O, LREE, La, Lu, MREE, Mg, MgO, Mn, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Pr, Rb, Re, Sc, Si, SiO2, Sm, Sn, Sr, Ta, Tb, Th, Ti, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|33902    |LMF                      |Lithium metaborate (LiBO2) fusion                                                             |DCP-OES, ICP, ICP:ES, ICP:MS, Q-ICP:MS|
|Ag, Al, Al2O3, As, Ba, Be, Bi, Ca, CaO, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, In, K, K2O, La, Li, Lu, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Pr, Rb, Sb, Sc, Si, SiO2, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|32874    |Fusion digestion         |Fusion digestion (CMIBS method)                                                               |AAS, COLOR, EM, ICP:MS|
|Ag, Al2O3, As, Ba, BaO, Be, Bi, CaO, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, In, K2O, La, Lu, MgO, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Pr, REE, Rb, Sb, Sc, SiO2, Sm, Sn, Sr, Ta, Tb, Th, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|26290    |LTMF_HNO3(5%)            |Lithium tetraborate/metaborate fusion, 5% HNO3                                                |ICP:ES, ICP:MS|
|Al, Al2O3, As, B, Ba, Be, Bi, CaO, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, In, K2O, La, Li, Lu, MgO, Mn, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Pr, Rb, Sb, Sc, SiO2, Sm, Sn, Sr, Ta, Tb, Th, Ti, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|19273    |MA2                      |HNO3/HF                                                                                       |ICP:ES, ICP:ES/MS, ICP:MS, ICP:MS-HR, Q-ICP:MS, SN-ICP:MS|
|Ag, As, Ba, Be, Bi, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Hg, Ho, In, La, Li, Lu, Mo, Nb, Nd, Ni, Pb, Pr, Rb, Re, Sb, Sc, Se, Sm, Sn, Sr, Ta, Tb, Te, Th, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|19176    |M_MA4                    |Microwave + acid digest (Labwest method)                                                      |ICP:ES/MS     |
|Al, Al2O3, As, Ba, Ca, CaO, Cd, Ce, Co, Cr, Cu, Hf, K, K2O, La, Mg, MgO, Mn, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Rb, Re, Sc, Si, Sr, Th, Ti, TiO2, Tl, U, V, W, Zn, Zr|22995 |CB_MA3                   |Combustion/ashing, HNO3/HCl/HF                                                                |DS_ID, ICP:ES, ICP:MS, ICP:MS-HR, Q-ICP:MS, QQQ-ICP:MS|
|Ag, Al, As, Au, B, Ba, Be, Bi, Ca, Cd, Ce, Co, Cr, Cu, K, La, Li, Mg, Mn, Mo, Na, Nb, Ni, Pb, Sb, Sn, Sr, Ti, U, V, W, Y, Zn, Zr|18490    |Part_digest              |Partial digestion (NGDB method)                                                               |COLOR, ICP:ES, N/A|
|Ag, Al, As, Ba, Be, Bi, Ca, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, In, K, LREE, La, Li, Lu, MREE, Mg, Mn, Mo, Na, Nb, Nd, Ni, Pb, Pr, REY, Rb, Re, Sb, Sc, Sm, Sn, Sr, Tb, Th, Ti, Tl, Tm, U, V, Y, Yb, Zn, Zr|17937    |MA3                      |HNO3/HCl/HF                                                                                   |ICP:ES, ICP:MS, Q-ICP:MS|
|Al, As, Ba, Be, Bi, Ca, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Hf, Ho, In, K, La, Li, Lu, Mg, Mn, Mo, Na, Nb, Nd, Ni, Pb, Pr, Rb, Re, Sb, Sc, Si, Sm, Sn, Sr, Ta, Tb, Te, Th, Ti, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|17162    |CB_MA3b                  |Combustion/ashing, HF/HNO3/HClO4                                                              |ICP:ES, ICP:MS, Q-ICP:MS|
|Ag, Al, Al2O3, As, Ba, Be, Bi, CaO, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Hf, Ho, K2O, La, Li, Lu, MgO, Mn, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Pr, REE, Rb, Sc, Sm, Sn, Sr, Ta, Tb, Th, Ti, TiO2, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|8432     |MA3b                     |HF/HNO3/HClO4                                                                                 |AAS, ICP, ICP:ES, ICP:MS, N/A, Q-ICP:MS|
|Ba, Be, Bi, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Hf, Ho, La, Li, Lu, Mn, Mo, Nb, Nd, Ni, Pb, Pr, Rb, Sc, Sm, Sn, Sr, Ta, Tb, Th, Ti, Tm, U, V, W, Y, Yb, Zn, Zr|7824     |CB_MA5                   |Combustion/ashing, HNO3/HClO4/HF/H3BO3/HCl                                                    |ICP:MS        |
|As, Ba, Ce, Cr, Cs, Dy, Er, Eu, Gd, Hf, Ho, La, Lu, Nb, Nd, Pb, Pr, Rb, Sc, Sm, Sr, Ta, Tb, Th, Tm, U, Y, Yb, Zr|5394     |MA3b_AR                  |HNO3/HF/HClO4, AR                                                                             |ICP:MS        |
|Al, Ba, Ca, Ce, Cr, Cu, Dy, Er, Eu, Gd, Ho, K, La, Lu, Mg, Mn, Mo, Na, Nd, Ni, Pr, Re, Sm, Sr, Tb, Ti, Tm, U, V, Yb, Zn|5130     |MA3b_H3BO3               |HNO3/HF/HClO4 digest, H3BO3                                                                   |ICP:ES, ICP:MS|
|Ag, Al, Ba, Ca, Cd, Co, Cr, Cu, K, Mg, Mn, Mo, Ni, Sr, Th, Ti, Tl, U, V, Zn|4480     |NaOAc(1M)_MA3b           |Sum of extract first with sodium acetate, followed by HF/HNO3/HClO4 digestion                 |Q-ICP:MS      |
|Al, Al2O3, Ca, CaO, Co, Cr, Cu, K, K2O, Mg, MgO, Mn, MnO, Mo, Na2O, Ni, Pb, Si, SiO2, TiO2, Zn|3040     |MA_HF                    |Multi-acid digestion with HF (CMIBS method)                                                   |AAS, COUL     |
|Al, As, B, Ba, Be, Ca, Cd, Ce, Co, Cr, Cu, K, La, Li, Mg, Mn, Mo, Na, Ni, Pb, Sc, Si, Sr, Ti, V, Y, Zn, Zr|2800     |HNO3(7N)                 |7N nitric acid                                                                                |ICP:ES        |
|Ag, Al, As, Au, B, Ba, Bi, Ca, Cd, Co, Cr, Cu, Ga, Hg, K, La, Li, Mg, Mn, Mo, Na, Ni, Pb, Sb, Sc, Se, Sr, Te, Th, Ti, Tl, U, V, W, Zn|2744     |AR_part                  |Partial digestion with aqua regia (CMIBS method)                                              |AAS, ICP:MS   |
|Ba, Ce, Cs, Dy, Er, Eu, Gd, Hf, Ho, La, Lu, Nb, Nd, Pb, Pr, REE, Rb, Sc, Sm, Sr, Ta, Tb, Th, Tm, U, Y, Yb, Zr|2467     |LTF_MA3b                 |Lithium tetraborate fusion, HNO3/HF/HClO4 digest                                              |ICP:MS        |
|Al, Mn, Mo, Re, U                               |2435     |CB_MA3b_H3BO3            |Combustion/ashing, HNO3/HF/HClO4, H3BO3                                                       |ICP:ES, ICP:MS, Q-ICP:MS|
|Al2O3, CaO, Ce, Co, Cr, Dy, Er, Eu, Gd, Ho, K2O, La, Lu, MgO, MnO, Na2O, Nd, Ni, Pr, Sc, SiO2, Sm, Tb, Th, TiO2, Tm, Y, Yb|2416     |LTMF_HNO3(dil)           |Lithium tetraborate/metaborate fusion, dilute HNO3                                            |ICP:ES/MS, ICP:MS|
|Al, As, Ba, Ca, Co, Cr, Cu, Hg, K, La, Mg, Mn, Mo, Na, Ni, Sc, Si, Sr, Ti, V, Y, Zn, Zr|2349     |MA                       |Multi-acid digestion, details unknown                                                         |AAS, ICP:MS   |
|Ag, Al2O3, Ba, Be, CaO, Ce, Cu, Dy, Er, Eu, Gd, Ge, Hf, Ho, K2O, La, Lu, MgO, MnO, Na2O, Nb, Nd, Ni, Pr, Rb, SiO2, Sm, Sr, Tb, Th, TiO2, Tl, Tm, U, V, Y, Yb, Zn, Zr|1755     |LTMF                     |Lithium tetraborate/metaborate fusion                                                         |ICP:MS        |
|Ag, Au, Pd, Pt                                  |1663     |FA                       |Fire assay chemical separation                                                                |GRAV, ICP:MS  |
|Al, As, Ca, Cd, Co, Cr, Cu, K, Mg, Mn, Mo, Na, Ni, Re, Ti, U, V, Zn|1586     |CB_MA2_AR                |Combustion/ashing, HNO3/HF, aqua regia                                                        |ICP:MS        |
|Ba, Be, Bi, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, In, La, Li, Lu, Mn, Mo, Nb, Nd, Ni, Pb, Pr, Rb, Sb, Sc, Sm, Sn, Sr, Ta, Tb, Th, Tl, Tm, U, V, W, Y, Yb, Zr|1571     |NH4HF2                   |Digestion with NH4HF2                                                                         |ICP:MS-HR     |
|Al2O3, Ba, CaO, Cr2O3, K2O, MgO, MnO, Na2O, SiO2, TiO2|1250     |LMF_MA2c                 |Lithium metaborate fusion, HF/HClO4 digest                                                    |ICP:ES        |
|Ba, Ce, Cu, Eu, Gd, La, Nd, Ni, Sm, Sr, V, Zn, Zr|1141     |MA4_IE                   |HF/HCl/HNO3/HClO4 and ion exchange separation.                                                |ICP:ES        |
|Ag, Bi, Cd, Pb                                  |1019     |KClO3(part)              |Partial digestion with potassium chlorate (CMIBS method)                                      |ICP:ES        |
|Al, Mn, Mo, Ti, Tl, V                           |904      |M_MA3                    |Microwave digest, HNO3/HCl/HF                                                                 |ICP:MS        |
|Al, Mo, U, V                                    |809      |MA5                      |HNO3/HClO4/HF/H3BO3/HCl                                                                       |ICP:ES, ICP:MS|
|Al2O3, CaO, K2O, MgO, MnO, Na2O, SiO2, TiO2     |792      |LTMF_HNO3(2%)            |Lithium tetraborate/metaborate fusion, 2% HNO3                                                |ICP:ES        |
|Al, Ba, Ca, Co, Cr, Cu, K, Mg, Mn, Mo, Na, Ni, Sc, Sr, Th, U, V, Zn|749      |CB_MA3_AR                |Combustion/ashing, HNO3/HCl/HF, AR                                                            |ICP:ES, Q-ICP:MS|
|Ba, Cu, Mo, Ni, Re, U, V, Zn                    |573      |CB_MA4                   |Combustion/ashing, HCl/HF/HClO4/HNO3                                                          |ICP:ES/MS, ICP:MS|
|Al, Cr, Mo, Ni, U, V, Zr                        |553      |CB_MA2                   |Combustion/ashing, HNO3/HF                                                                    |ICP:ES, ICP:MS, Q-ICP:MS|
|Au, Ir, Os, Pd, Pt, Re                          |532      |NiS_FA                   |NiS fire assay chemical separation. (CMIBS method)                                            |ICP:MS        |
|Cr, Li, V                                       |455      |MA2e                     |HClO4/H3PO4                                                                                   |AAS           |
|Co, Cu, La, Mo, Nd, Sc, U, V                    |368      |CB_MA4seq                |Combustion/ashing, seq acid digest HF, AR, ARrev, HNO3 (Kunzmann et al. 2015, Maloney et al. 2024)|ICP:MS        |
|Ce, Dy, Er, Eu, Gd, Ho, La, Lu, Nd, Pr, Sc, Sm, Tb, Tm, Y, Yb|367      |Sinter                   |Sinter, unspecified (CMIBS method)                                                            |IC            |
|Al2O3, CaO, MgO, SiO2                           |343      |CB_MA2_H3BO3             |Combustion/ashing, HF/HNO3, H3BO3 to neutralize                                               |ICP:ES        |
|Ce, Dy, Er, Eu, Gd, Ho, La, Lu, Nd, Pr, Sm, Tb, Tm, Y, Yb|330      |HNO3(10%)_CB_HNO3(10%)   |10% HNO3, combustion/ashing, second leach in 10% HNO3                                         |ICP:MS        |
|Al, Ce, Cu, Dy, Er, Eu, Gd, Ho, La, Lu, Mn, Mo, Nd, Ni, Pr, Sm, Tb, Tm, U, V, Yb, Zn|308      |LTF_HNO3                 |Lithium tetraborate fusion, HNO3                                                              |ICP:ES, Q-ICP:MS|
|Ca, Mg, Mn, Sr                                  |287      |NaCl/NaOCl/HCl           |NaCl and NaOCl(bleach), HCl                                                                   |Q-ICP:MS      |
|Ca, Mg                                          |178      |HCl(24h/cold)            |Cold HCl (1M or 10%) for 24hr (Raiswell et al. 1994)                                          |ICP:MS        |
|Al, Mn, Mo, U, V                                |164      |M_MA3_H202               |Microwave digest, HNO3/HCl/HF, H2O2                                                           |ICP:MS        |
|Al, As, B, Ba, Be, Bi, Cd, Ce, Co, Cr, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Ho, La, Li, Lu, Mn, Mo, Nb, Nd, Ni, Pb, Pr, Rb, Sb, Sc, Sm, Sn, Sr, Ta, Tb, Th, Ti, Tl, Tm, U, V, W, Y, Yb, Zn, Zr|155      |HCl(decarb)_MA2          |Decarbonated with HCl, HNO3/HF                                                                |Q-ICP:MS      |
|Cd, Co, Cu, Li, Mn, Ni, Pb, Rb, V, Zn           |142      |HF                       |Hydrofluoric acid                                                                             |AAS           |
|Co, Cu, Mo, Ni, Pb, Sc, V, Zn                   |101      |MA3_H2O2                 |HNO3/HCl/HF, H2O2                                                                             |ICP:MS        |
|Al2O3, SiO2                                     |78       |Pressed pellet           |Pressed powder pellet                                                                         |SEM-EDS       |
|Ce, Dy, Er, Eu, Gd, Ho, La, Lu, Nd, Pr, Sm, Tb, Tm, Yb|38       |RC                       |Radiochemical separation (CMIBS method)                                                       |INAA          |
|Tl-auth, V-auth                                 |36       |HNO3(2M)                 |2M nitric acid                                                                                |ICP:MS        |
|Hg                                              |14       |Acid                     |Acidification/acid treatment, details not provided                                            |AAS           |
|Ir, Pd, Pt                                      |13       |PbO_FA                   |PbO fire assay chemical separation (CMIBS method)                                             |AAS           |
|Ce, Dy, Er, Eu, Gd, Nd, Sm, Yb                  |8        |HNO3(part)               |HNO3 partial digest (no strength specified)                                                   |ICP:MS        |
|Ag, Al, Al2O3, As, Au, B, Ba, Be, Bi, Ca, CaO, Cd, Ce, Co, Cr, Cr2O3, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, HREE, Hf, Hg, Ho, In, Ir, K, K2O, LREE, La, Li, Lu, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, Os, Pb, Pd, Pr, Pt, REE, REY, Rb, Re, Sb, Sc, Se, Si, SiO2, Sm, Sn, Sr, SrO, Ta, Tb, Te, Th, Ti, TiO2, Tl, Tm, U, V, V2O5, W, Y, Yb, Zn, Zr|1367856  |NULL                     |NULL                                                                                          |AAS, COLOR, CVAAS, DNAA, DNC, ED-XRF, EDEM, ES, ES_Q, ES_SQ, FA, FLOUR, GR, GR-INAA, HgAna, ICP:ES, ICP:ES/MS, ICP:MS, ICP:MS-ID, ICP:MS-LA, ICP:MS-MC, INAA, LC-INAA, LQS, N/A, NAA, NIR, Q-ICP:MS, SC-INAA, SSMS|


#### XRF

**Commonly cited method papers**
* Norrish and Hutton, 1969 https://doi.org/10.1016/0016-7037(69)90126-4
* Johnson et al. 1999 Advances in X-ray Analysis 41 (1999): 843-867. (https://pdxscholar.library.pdx.edu/cgi/viewcontent.cgi?filename=1&article=7598&context=open_access_etds&type=additional)

**Notes**

Sometimes it is explicitly stated that the sample was ashed prior to making fused beads or LOI was measured separately and adjustments made later. In contrast to the multi-acid methods, however, “CB” (for combustion/ashing) has not been included in the code, even for cases where a combustion/ashing step is clearly stated.

It is not always clear whether “lithium borate” is used in the strict sense (i.e. Li2B4O7), or whether sometimes it is assumed to mean a mix of lithium borate (aka tetraborate) and lithium metaborate. The latter seems likely. A distinction is made in the experimental code where the methods are explicit, but note therefore that “LTF” is likely more of a ‘waste-basket’ code than the more precise LTMF. The generic code 'fused beads' is used for cases with no further detail provided, but it is likely to mean lithium borate/metaborate fusion of some description.

Temperature and time of flux fusion is sometimes explicitly stated, but not considered in these codes.

All pressed pellet methods are lumped together, but note that there are variations within - for example, Ansari et al. 2021: “pressed pellets were prepared from the oven dried powdered samples and boric acid (in 6:4 ratio) following the method described by Takahashi (2015).”

Some samples were analyzed via Handheld XRF (HHXRF), although these represent a minority of analyses analyzed by broader XRF methods. The accuracy of HHXRF measurements can vary widely by instrument and by element (see Rowe et al., 2013 https://doi.org/10.1016/j.chemgeo.2011.12.023 and Dahl et al., 2013 http://dx.doi.org/10.1016/j.chemgeo.2013.10.022).


|analyte(s)     |count_res|code                  |translation                                                                                     |ana_method(s)|
|---------------|---------|----------------------|------------------------------------------------------------------------------------------------|-------------|
|Al, Al2O3, As, Ba, Ca, CaO, Ce, Co, Cr, Cu, Ga, K, K2O, La, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Ni, Pb, Rb, Sb, Sc, Si, SiO2, Sn, Sr, Th, Ti, TiO2, U, V, Y, Zn, Zr|1517     |MA2                   |HNO3/HF                                                                                         |XRF          |
|Al, Al2O3, As, Ba, BaO, Ca, CaO, Ce, Cr, Cr2O3, Cu, Ga, K2O, La, Mg, MgO, Mn, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Rb, Sc, Si, SiO2, Sr, Th, Ti, TiO2, U, V, Y, Zn, Zr|22842    |LTF                   |Lithium tetraborate (aka lithium borate) fusion                                                 |XRF          |
|Al2O3, CaO, Cr2O3, K2O, MgO, MnO, Na2O, SiO2, TiO2|909      |Na2O2Fus              |Sodium peroxide sinter/fusion                                                                   |XRF          |
|Al, Al2O3, As, Ba, BaO, Ca, CaO, Ce, Co, Cr, Cr2O3, Cs, Cu, Ga, Hf, K2O, La, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Pr, Rb, Re, Sc, Si, SiO2, Sm, Sr, Ta, Th, Ti, TiO2, U, V, Y, Zn, Zr|4656     |Fused beads           |Fused beads                                                                                     |XRF          |
|Al, Al2O3, Ba, Ca, CaO, Ce, Co, Cr, Cu, Ga, K, K2O, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Ni, Pb, Rb, Sc, Si, SiO2, Sr, Th, Ti, TiO2, V, Y, Zn, Zr|52739    |LMF                   |Lithium metaborate (LiBO2) fusion                                                               |XRF          |
|Al2O3, As, Ba, CaO, Ce, Co, Cr, Cu, Ga, K2O, La, MgO, MnO, Mo, Na2O, Nb, Nd, Ni, Pb, Rb, Sc, SiO2, Sr, Th, Ti, TiO2, U, V, Y, Zn, Zr|11159    |Pressed pellet        |Pressed powder pellet                                                                           |XRF          |
|Al, Al2O3, As, Ba, Ca, CaO, Ce, Co, Co3O4, Cr, Cr2O3, Cu, CuO, K, K2O, La, Mg, MgO, Mn, MnO, Mo, Na, Na2O, Nb, Nd, Ni, NiO, Pb, Rb, Sc, Si, SiO2, Sr, Ti, TiO2, V, V2O5, W, Y, Zn, Zr|8109     |LTMF                  |Lithium tetraborate/metaborate fusion                                                           |XRF          |
|Al, As, Ca, Co, Cr, Cu, K, K2O, Mn, MnO, Mo, Ni, Pb, Rb, Si, Sr, Ti, TiO2, U, V, Y, Zn, Zr|6474     |Raw powder            |Raw powder                                                                                      |HHXRF        |
|Al2O3, Ca, CaO, K2O, Mn, Mo, Ni, Rb, SiO2, Sr, TiO2, U, V, Zr|8440     |Rock surface          |Rock surface (cut, sometimes polished)                                                          |HHXRF        |
|Ag, Al, Al2O3, As, Au, B, Ba, BaO, Be, Bi, Ca, CaO, Cd, Ce, Co, Cr, Cr2O3, Cs, Cu, Dy, Er, Eu, Ga, Gd, Ge, Hf, Hg, Ho, In, K, K2O, La, Li, Lu, Mg, MgO, Mn, MnO, MnO2, Mo, Na, Na2O, Nb, Nd, Ni, Pb, Pd, Pr, Rb, Re, Sb, Sc, Se, Si, SiO2, Sm, Sn, Sr, SrO, Ta, Tb, Te, Th, Ti, TiO2, Tl, Tm, U, V, V2O5, W, Y, Yb, Zn, Zr|345454   |NULL                  |NULL                                                                                            |ED-XRF, HHXRF, XRF|

### Mineralogy/Composition

**XRD**

For the majority of XRD data no method paper is cited. Details of sample preparation are generally not included. See for example https://pubs.usgs.gov/of/2001/of01-041/htmldocs/methods.htm for some details about preparation that could be considered. For the most part we report analytes as presented in data tables.

 
|analyte(s)     |count_res|code                  |translation                                                                                     |ana_method(s)|
|---------------|---------|----------------------|------------------------------------------------------------------------------------------------|-------------|
|Albite, Anatase, Anhydrite, Ankerite, Apatite, Berthierine, Calcite, Chamosite, Chlorite, Dolomite, Fe/Mg-mica, Glauconite, Gypsum, Halite, Hematite, Illite, K-Feldspar, K/Al-mica, K/Mg-mica, Kaolinite, Magnesite, Magnetite, Mica, Montmorillonite, Plagioclase, Pyrite, Pyrrhotite, Quartz, Rutile, Siderite, Talc|9019     |Random mount          |Random/unoriented mount                                                                         |XRD          |
|Calcite, Chlorite, Feldspar, Illite, Illite_Smectite, Kaolinite, Pyrite, Quartz, Total_Clay|423      |Oriented mount        |Oriented mount                                                                                  |XRD          |
|1:1 clays, 2:1 clays, Detritals, Glauconite, K-Feldspar, Pyrite, Quartz, Total_Clay|391      |HCl(decarb)_RandomMount|Decarbonated with HCl, random mount                                                             |XRD          |
|Albite, Analcime, Anatase, Anhydrite, Ankerite, Anorthite, Apatite, Aragonite, Barite, Berthierine, Biotite, Calcite, Chamosite, Chlorite, Clinochlore, Cristobalite, Dolomite, Dolomite_Iron_Dolomite, Dolomite_Siderite, Feldspar, Fluorapatite, Gypsum, Halite, Hematite, Hydroxylapatite, Illite, Illite_Mica, Illite_Montmorillonite, Illite_Muscovite, Illite_Smectite, Ilmenite, Jarosite, K-Feldspar, Kaolinite, Magnesite, Magnetite, Marcasite, Microcline, Mixed_Layer_Clays, Montmorillonite, Muscovite, Nontronite, Orthoclase, Plagioclase, Pyrite, Quartz, Quartz_Christobalite, Rhodochrosite, Rutile, Sanidine, Siderite, Smectite, Sphalerite, Sum, Talc, Total_Carbonate, Total_Clay, Total_NonClay|17773    |NULL                  |NULL                                                                                            |XRD          |

**LOI/Sum/Insol**

These are values that tend to be associated with batches of data from other methods e.g. XRF, ICP.

* Sum = sum of components
* Insol = acid-insoluble residue
* LOI = loss on ignition

LOI also has the analytical code "LOI", the experimental code is used to give a temperature, if it is provided e.g. 1000deg, 1050deg.


**CIA**

CIA is the Chemical Index of Alteration, generally defined as follows (using Li et al. 2021 as example): "CIA is equal to [Al2O3/(Al2O3 + CaO* + Na2O + K2O)] × 100, where all oxide values are molar quantities, and CaO* represents CaO content in silicate minerals only (Nesbitt and Young, 1984), therefore, the CaO contents of carbonate and phosphate must be deducted from total CaO." Note there are differences in how this is accomplished; see original publications for any variations on the method.


***

## Above/Below Detection

Abundance can only be empty (NULL) if a value is explicitly recorded as above or below detection. Where possible the detection limits are also stored. Note that since the Simple and Detailed searches will average results, measurements above or below detection limits will also be removed, as they cannot be averaged. This is important for studies of analytes whose abundances are near detection limits for common geochemical methodologies—in the case of low-abundance elements, most analyses (i.e., below detection) will be removed, and only anomalously ‘high’ analyses will be returned. 

Values above detection are rare (0.3% of the total). Below detection values are more common (19.5% of the total). A large proportion of these come from the USGS-NGDB dataset. Summary tables of total counts and percents above and below detection for all data, and for each data source are linked below. 





Miscellaneous useful references: 

Balaram, V., & Subramanyam, K. S. V. (2022). Sample preparation for geochemical analysis: Strategies and significance. Advances in Sample Preparation, 1, 100010. https://doi.org/10.1016/j.sampre.2022.100010

