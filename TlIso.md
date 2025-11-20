#### Thallium isotopes

**Commonly cited method papers**

- Rehkämper and Halliday, 1999 https://doi.org/10.1016/S0016-7037(98)00312-3
- Nielsen et al., 2004 https://doi.org/10.1016/j.chemgeo.2003.11.006
- Nielsen et al. 2011 https://doi.org/10.1016/j.gca.2011.07.047
- Owens et al., 2017 http://dx.doi.org/10.1016/j.gca.2017.06.041
- Owens et al. 2019 https://doi.org/10.1017/9781108688697
- Wang et al. 2023 https://doi.org/10.1016/j.chemgeo.2023.121457 (a newer method - all SGP data entered so far are older than this paper)

**Notes**

For all studies in SGP the digestion procedure starts with a standard step: 2M HNO3 for 12hrs at 130deg. This is used to separate authigenic Tl bound to pyrite from detrital Tl. One study subsequently uses a HNO3/HF digest on the residue left from this step, in order to determine authigenic Tl.

The next steps to remove organics (from the supernatant) are variable, involving acids (e.g. HNO3/HCl/AR/reverse-AR in various combinations), ashing and/or microwave, and +/-H2O2. These steps are not included in the code.

In preparation for column chemistry a treatment with 1M HCl +/- brominated H2O is usually applied which is also not coded. This appears to be almost universal, although “brominated H2O” is not always mentioned.

The primary distinction in the purification step is between one or two columns:

- One-column - newer approach “shown to work well for high Tl and low Pb samples”
- Two-column - the standard older approach e.g. “thallium purification was accomplished using two separate columns, one large and one micro-column, using AG1X8 anion exchange resin from Biorad.” (Owens et al. 2017).

| analyte(s)           | count_res | code              | translation                                                              | ana_method(s)     |
| -------------------- | --------- | ----------------- | ------------------------------------------------------------------------ | ----------------- |
| Tl-auth, e205Tl-auth | 785       | HNO3(2M)\_AE      | 2M HNO3, one-column anion exchange chromatography (AG1X8 resin)          | ICP:MS-MC         |
| Tl-auth, e205Tl-auth | 296       | HNO3(2M)\_2AE     | 2M HNO3, two-column anion exchange chromatography (AG1X8 resin)          | ICP:MS, ICP:MS-MC |
| e205Tl-det           | 13        | HNO3(2M)\_MA2_2AE | 2M HNO3, HNO3/HF, two-column anion exchange chromatography (AG1X8 resin) | ICP:MS-MC         |
