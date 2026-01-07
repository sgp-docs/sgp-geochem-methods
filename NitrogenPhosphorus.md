### Nitrogen and Phosphorus

**Phosphorus**

**Commonly cited method papers**

- Ruttenberg 1992 https://doi.org/10.4319/lo.1992.37.7.1460 (SEDEX)
- Anderson and Delaney 2000 https://doi.org/10.4319/lo.2000.45.2.0509 (SEDEX)
- Oxmann et al. 2008 https://doi.org/10.1111%2Fj.1365-2389.2008.01062.x (CONVEX)
- Thompson et al. 2019 https://doi.org/10.1016/j.chemgeo.2019.07.003 (SEDEX)
- Beil et al. 2020 https://doi.org/10.5194/cp-16-757-2020-supplement (CONVEX)

**Notes**

For **total phosphorus** see [Elements](https://github.com/ufarrell/sgp_phase2/wiki/C.-Analyses#elements) section below.

**SEDEX**

The majority of phosophorus speciation data in SGP is measured using some variation of "SEDEX" (Sedimentary Extraction).

In SGP we have no code for the first SEDEX step, which is for modern sediments, and thus far not used in any geological papers.

SGP codes for the older (Ruttenberg) method are

- SeqAphos (analyte: P-Fe1(seq))
- SeqBphos (analyte: P-auth(seq))
- SeqCphos (analyte: P-det(seq))
- SeqDphos (analyte: P-org(seq))

SGP codes for the newer (Thompson) method are

- SeqAphos (analyte: P-Fe1(seq))
- SeqBphos (analyte: P-auth(seq))
- SeqCphos (analyte: P-det(seq))
- SeqDphos(mod) (analyte: P-mag(seq))
- SeqEphos(mod) (analyte: P-Fe2(seq))
- SeqFphos(mod) (analyte: P-org(seq))

The first three steps are shared. SeqFphos(mod) is the same procedure as SeqDphos, but in a different place sequentially.

Beaty et al. 2025 combined early steps, refering to Anderson and Delaney 2000. This is described as follows: "Fe oxide-bound P (PFeOx) and authigenic or Ca-associated P (Pauth, including carbonate fluorapatite, carbonate-associated phosphate, and biogenic apatite) were co-extracted (reported as PFeOx+auth) using a 1.0 (+/-0.1) g of powdered sample to 60 mL solution ratio shaken in 1 M Na-acetate (pH = 4), 1 M MgCl2 (pH = 8), and DI water, respectively. [...]". From Beaty pers. comm.: explanation for how the data in the SI lines up with the SGP analyte codes: P_FeOx+auth = SecAphos + SecBphos (these were not measured individually).

In SGP we have therefore added this code:

- SeqABphos (analyte: P-Fe1+auth(seq))

Any sum of components is stored in the proxy table (and not presented on the website). These include:

- P-FeT = P-Fe1+P-mag+P-Fe2
- P-react = P-Fe+P-auth+P-org
- P-tot = P-Fe1+P-auth+P-mag+P-Fe2+P-det+P-org

- P-react(CONVEX) = P-Ca + P-AlFe

There is variability in how analytes are reported in papers, especially P-fe/Fe1 and P-det.

SGP uses **P-Fe1** for the analyte measured from the first step (SeqAPhos), _whether or not_ the new or old sequential method is used (i.e. there can be studies where “P-Fe1” was measured but “P-Fe2” was not).

SGP uses **P-det** for the analyte measured from the third step (SeqCPhos), _whether or not_ the new or old sequential method is used. P-cryst and Px1 are variations in the literature: Thompson et al. 2019 state that _“The Pdet step of the original SEDEX procedure has been redefined as Pcryst, and represents crystalline apatite which may include recrystallized CFA as well as detrital apatite of igneous or metamorphic origin”_. Creveling et al. 2014 (pre-dating Thompson) use the variation Px1, and their method is described as a “modified version of Ruttenberg”. Bowyer et al. 2020 and 2023 cite the Thompson method but use P-det as the name.

Some papers add a total digestion step to the end, in order to extract the most recalcitrant phases (**P-res**)

Guilbaud et al. 2020 describe this step as follows: "an additional HNO3-HF-HClO4-H3BO3-HCl extraction step (V) was performed on the residue to achieve near-complete P recovery."

Beaty et al. 2025 state: "post-extraction residues were digested and re-analyzed for P via ICP-MS to verify mass balance, following the same procedures as for pre-extraction powders. This fraction (Presidue) includes highly recalcitrant P phases remaining after Porg was extracted, presumably including P bound in crystalline Fe minerals such as hematite, magnetite, and Fe-rich silicates (Thompson et al. 2019).

Beaty pers. comm. 2025 explained this step in the context of SGP as follows: P_res is all P remaining in residue after the P_org extraction (=SeqDphos), extracted via total digestion of the dried residue via dissolution in HF+HNO3 followed by HNO3+HCl (=MA3), and measured on ICP-MS. This extraction is not included in the original SEDEX protocol (Ruttenberg, 1992) or the modified protocol for ancient sediments (Thompson et al., 2019), given the assumption that the P_org extraction step (ashing followed by 1 M HCl leach) removes all remaining P. However, we were concerned that some highly recalcitrant P remains after P_org extraction in our samples, and confirmed via total digestion of the post-P_org residue that P_res comprises approximately 5% of total P in our samples. The phases containing this P are unknown, but are likely highly crystalline detrital minerals that do not fully dissolve with 1 M HCl, and were therefore not extracted in the P_det (=SeqCphos) or P_org (=SeqDphos) pools.

The resulting SGP codes for these modifications include

- SeqResPhos - for the P extracted with a final total multi-acid (MA3) digest after sequential steps.

**CONVEX**
Some P data in SGP is measured using a modified "CONVEX" (Conversion Extraction) method, based on Oxmann et al. 2008. This is coded as two-steps, the first targetting Al∕Fe-oxyhydroxide-bound phosphorus and the second Ca-bound phosphorus.

- ConvexA (analyte: P-AlFe)
- ConvexB (analyte: P-Ca)

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
