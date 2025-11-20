### Nitrogen and Phosphorus

**Phosphorus**

**Commonly cited method papers**

- Ruttenberg 1992 https://doi.org/10.4319/lo.1992.37.7.1460
- Thompson et al. 2019 https://doi.org/10.1016/j.chemgeo.2019.07.003

**Notes**

See the papers above for detailed discussion and figures illustrating methodological steps for SEDEX ("Sedimentary Extraction").

For **total phosphorus** see [Elements](https://github.com/ufarrell/sgp_phase2/wiki/C.-Analyses#elements) section below.

In SGP we have no code for the first SEDEX step, which is for modern sediments.

SGP codes for the older (Ruttenberg) method are

- SeqAphos
- SeqBphos
- SeqCphos
- SeqDphos

SGP codes for the newer (Thompson) method are

- SeqAphos
- SeqBphos
- SeqCphos
- SeqDphos(mod)
- SeqEphos(mod)
- SeqFphos(mod)

The first three steps are shared. SeqFphos(mod) is the same procedure as SeqDphos, but in a different place sequentially.

Any sum of components is stored in the proxy table, not presented on the website in Phase2. These include:

- P-FeT = P-Fe1+P-mag+P-Fe2
- P-react = P-Fe+P-auth+P-org
- P-tot = P-Fe1+P-auth+P-mag+P-Fe2+P-det+P-org

There is variability in how analytes are reported in papers, especially P-fe/Fe1 and P-det.

SGP uses **P-Fe1** for the analyte measured from the first step (SeqAPhos), _whether or not_ the new or old sequential method is used (i.e. there can be studies where “P-Fe1” was measured but “P-Fe2” was not).

SGP uses **P-det** for the analyte measured from the third step (SeqCPhos), _whether or not_ the new or old sequential method is used. P-cryst and Px1 are variations in the literature: Thompson et al. 2019 state that _“The Pdet step of the original SEDEX procedure has been redefined as Pcryst, and represents crystalline apatite which may include recrystallized CFA as well as detrital apatite of igneous or metamorphic origin”_. Creveling et al. 2014 (pre-dating Thompson) use the variation Px1, and their method is described as a “modified version of Ruttenberg”. Bowyer et al. 2020 and 2023 cite the Thompson method but use P-det as the name.

One outlier method “SeqC+Ephos_Guilbaud” was added to account for a modification of Guilbaud et al. 2020. This method code might be changed if other similar data is added - for now this is the only example.

| analyte(s)  | count_res | code                | translation                                                  | ana_method(s) |
| ----------- | --------- | ------------------- | ------------------------------------------------------------ | ------------- |
| P-Fe1(seq)  | 524       | SeqAphos            | CDB pH 7.6 8h (Ruttenberg 1992, Thompson et al. 2019)        | ICP:ES        |
| P-auth(seq) | 613       | SeqBphos            | Na Acetate pH 4.0 6h (Ruttenberg 1992, Thompson et al. 2019) | MolyB         |
| P-det(seq)  | 538       | SeqCphos            | 1M HCl 16hr (Ruttenberg 1992, Thompson et al. 2019)          | MolyB         |
| P-org(seq)  | 225       | SeqDphos            | Ash 550decC, HCl (Ruttenberg 1992).                          | MolyB         |
| P-mag(seq)  | 362       | SeqDphos(mod)       | Ammonium oxalate 6h (Thompson et al. 2019)                   | ICP:ES        |
| P-Fe2(seq)  | 364       | SeqEphos(mod)       | CDA ph 4.8 6h (Thompson et al. 2019)                         | ICP:ES        |
| P-org(seq)  | 364       | SeqFphos(mod)       | Ash 550degC, 1M HCl 6h (Thompson et al. 2019)                | MolyB         |
| P-inorg     | 38        | HCl(decarb)         | Decarbonated with HCl                                        | UV-Vis        |
| P-det(seq)  | 74        | SeqC+Ephos_Guilbaud | SeqC_phos + MA_5 after SeqD_phos                             | MolyB         |

**Nitrogen**

The majority of nitrogen isotopes in SGP are run using well-established methods (usually no method paper is cited). See above for carbon, often measured alongside. C:N ratios are atomic. N is usually measured along with the isotopes, and included here but see Element section below for other measurements of total N.

The **reference standard** for nitrogen isotopes is Air.

**Proxy primer**

Dr. Eva Stüeken, Nitrogen isotopes https://youtu.be/2cNkWSPqMo4?si=I7rGSO8dHmWNvRcX

| analyte(s)                       | count_res | code                | translation                                                                                         | ana_method(s)                          |
| -------------------------------- | --------- | ------------------- | --------------------------------------------------------------------------------------------------- | -------------------------------------- |
| C:N, DELTA_N15, N                | 5972      | HCl(decarb)         | Decarbonated with HCl                                                                               | CHNS-EA, EA, EA-CF-IRMS, EA-IRMS, IRMS |
| DELTA_N15_KER                    | 132       | MA2b_ZnBr           | HCl/HF, heavy liquid separation in ZnBr                                                             | EA-IRMS                                |
| C:N, DELTA_N15, N                | 126       | HCl(decarb)\_MA2b   | Decarbonated with HCl, HCl/HF                                                                       | EA-IRMS                                |
| DELTA_N15_KER                    | 111       | SOX(DCM)\_MA3       | Soxhlet dichloromethane-extraction, HF/HCl/HNO3                                                     | EA-IRMS                                |
| DELTA_N15, DELTA_N15_KER, N      | 78        | Decarb              | Decarbonated (no details provided)                                                                  | EA-CF-IRMS, IRMS                       |
| DELTA_N15_KER                    | 61        | HCl(decarb)\_HF/BF3 | Decarb. with HCl, HF and BF3 for kerogen extraction (see Robl and Davis 1993, Stüecken et al. 2015) | EA-CF-IRMS                             |
| DELTA_N15_KER                    | 51        | SOX(DCM)\_MA2b      | Soxhlet dichloromethane-extraction, HF/HCl                                                          | EA-CF-IRMS                             |
| C:N, DELTA_N15, DELTA_N15_KER, N | 3072      | NULL                | NULL                                                                                                | EA-CF-IRMS, EA-IRMS, IRMS, N/A         |

---
