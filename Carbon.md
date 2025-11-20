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

| analyte(s)                                        | count_res | code              | translation                                            | ana_method(s)                                                     |
| ------------------------------------------------- | --------- | ----------------- | ------------------------------------------------------ | ----------------------------------------------------------------- |
| TOC                                               | 28601     | NULL              | NULL                                                   | COUL, CS-EA, EA, EA-CF-IRMS, EA-IRMS, HAWK, N/A, REP, SRA, TC-TIC |
| TOC                                               | 16951     | HCl(decarb)       | Decarbonated with HCl                                  | CHNS-EA, CS-EA, EA, EA-CF-IRMS, EA-IRMS, IR, IRMS, N/A            |
| TOC                                               | 3039      | Decarb            | Decarbonated (no details provided, likely HCl or AcOH) | CS-EA, EA-CF-IRMS, EA-IRMS, REP                                   |
| TOC                                               | 701       | WO_H2SO4          | Wet oxidation with H2SO4 (CMIBS method)                | GRAV                                                              |
| TOC                                               | 383       | CB                | Combustion/ashing                                      | CHNS-EA, COUL, N/A, TC                                            |
| TOC                                               | 202       | HCl(decarb)\_MA2b | Decarbonated with HCl, HCl/HF                          | EA                                                                |
| TOC                                               | 130       | 500deg            | Heated to 500degC                                      | LOI                                                               |
| TOC                                               | 128       | Acid_CB           | Acidified before Dumas combustion technique            | VD                                                                |
| TOC                                               | 70        | H2SO3             | Sulfurous acid                                         | EA-CF-IRMS                                                        |
| TOC                                               | 26        | MA3               | HNO3/HCl/HF                                            | CS-EA                                                             |
| TOC                                               | 12        | Digest            | Unspecified digestion (CMIBS method)                   | ICP:MS                                                            |
| TIC                                               | 13574     | NULL              | NULL                                                   | COUL, CS-EA, EA, EA-IRMS, HAWK, N/A, TC-TOC, TTR, VOL             |
| TIC                                               | 1521      | HCl(decarb)       | Decarbonated with HCl                                  | CS-EA, IR, ML                                                     |
| TIC                                               | 726       | H3PO4             | Phosphoric acid                                        | CS-EA, EA, IRMS                                                   |
| TIC                                               | 360       | Decarb            | Decarbonated (no details provided, likely HCl or AcOH) | COUL, CS-EA, EA, ML                                               |
| TIC                                               | 313       | HClO4             | Perchloric acid                                        | COUL, COUL_TT                                                     |
| TIC                                               | 97        | CB                | Combustion/ashing                                      | EA, N/A                                                           |
| C                                                 | 12669     | NULL              | NULL                                                   | CS-EA, EA, EA-IRMS, GRAV, GRAV_FLUX, IR, N/A, REP                 |
| C                                                 | 12420     | CB                | Combustion/ashing                                      | CHNS-EA, COUL, CS-EA, IR, N/A, TC                                 |
| C                                                 | 6         | Digest            | Unspecified digestion (CMIBS method)                   | WC                                                                |
| **Organic carbon isotopes**                       |           |                   |                                                        |                                                                   |
| DELTA_C13_ORG                                     | 10204     | HCl(decarb)       | Decarbonated with HCl                                  | CF-IRMS, EA-CF-IRMS, EA-IRMS, IRMS                                |
| DELTA_C13_ORG                                     | 2178      | NULL              | NULL                                                   | EA-CF-IRMS, EA-IRMS, IRMS, N/A                                    |
| DELTA_C13_ORG                                     | 704       | Decarb            | Decarbonated (no details provided)                     | EA-CF-IRMS, EA-IRMS                                               |
| DELTA_C13_ORG                                     | 160       | HCl(decarb)\_MA2b | Decarbonated with HCl, HCl/HF                          | IRMS                                                              |
| DELTA_C13_ORG                                     | 104       | MA2b              | HCl/HF                                                 | EA-IRMS                                                           |
| DELTA_C13_ORG                                     | 79        | H2SO3             | Sulfurous acid                                         | EA-CF-IRMS                                                        |
| **Rock Eval Pyrolysis/HAWK/Source Rock Analysis** |           |                   |                                                        |                                                                   |
| S1, S2, S3, Tmax                                  | 26029     | NULL              | NULL                                                   | HAWK, REP, SRA, N/A                                               |
| S1, S2, S3, Tmax                                  | 7875      | Decarb            | Decarbonated (no details provided)                     | REP                                                               |
