#### Molybdenum Isotopes

**Commonly cited method papers**

- Barling et al. 2001 https://doi.org/10.1016/S0012-821X(01)00514-3
- Siebert et al. 2001 https://doi.org/10.1029/2000GC000124
- Anbar 2004 https://doi.org/10.2138/gsrmg.55.1.429
- Arnold et al. 2004 https://doi.org/10.1126/science.1091785
- Johnson et al. 2004 https://doi-org.stanford.idm.oclc.org/10.1515/9781501509360
- Pearce et al. 2009 https://doi.org/10.1111/j.1751-908X.2009.00012.x (single column method)
- Zhang et. al. 2009 (Zhang, Y.X., Wen, H.J. and Fan, H.F. (2009) Chemical Pretreatment Methods for Measurement of Mo Isotope Ratio on Geological Samples. Chinese Journal Anal. Chemistry, 37, 216-220.)
- Voegelin et al. 2009 https://doi.org/10.1016/j.chemgeo.2009.05.015 (carbonates)
- Duan et al., 2010 https://doi.org/10.1016/j.gca.2010.08.035
- Wen et al. 2011 https://doi.org/10.1130/G32055.1
- Greber et al. 2012 https://doi.org/10.1111/j.1751-908X.2012.00160.x
- Nägler et al. 2013 https://doi.org/10.1111/j.1751-908X.2013.00275.x (standards)
- Goldberg et al. 2013 https://doi.org/10.1039/c3ja30375f (standards)
- Wille et al. 2013 http://dx.doi.org/10.1016/j.chemgeo.2012.12.018
- Li et al. 2014: https://doi.org/10.1111/j.1751-908X.2013.00279.x
- Romaniello et al. 2016 https://doi.org/10.1016/j.chemgeo.2016.05.019 (carbonates)
- Thoby et al. 2019 https://doi.org/10.1130/G45706.1 (carbonates)

**Notes**

The majority of the molybdenum isotopes in SGP are from a total acid digest (with or without a combustion/ashing initial step), followed by a two-step chromatographic procedure: anion exchange (with AG1-X8 resin) and cation exchange (with AG50W-X8), referencing e.g. Barling et al. 2001 and Duan et al. 2010.

Scheller et al. 2018 (https://doi.org/10.1016/j.precamres.2017.12.009) use a reverse-aqua regia digest and a single-column approach, referencing Pearce et al. 2009.

Three studies - Luo et al. 2021, Hodgskiss et al. 2021, O'Sullivan et al. 2022 - have molybdenum isotopes from carbonate fractions, after a (relatively) light digest.

Most studies use a double-spike to correct for fractionation during chromatography and to correct for mass-bias. Some studies use sample-standard bracketing, and some compare both double-spike and sample-standard bracketing.

The **reference standards** used for molybdenum isotopes have been variable through time, with older studies tending to use a variety of in-house standards (e.g. RochMo2, various other Johnson Matthey (JMC) Specpure ICP Mo standard solutions). Most studies now report measurements relative to NIST SRM 3134 "where the standard NIST 3134 = 0.25permil". See Goldberg et al. 2013 and Nägler et al. 2013 for discussion. Five studies older than 2013 in SGP use RochMo2, JMC Specpure lot#702499I and JMC-Mo Sie lot#602332B.

| analyte(s)                  | count_res | code                  | translation                                                                                          | ana_method(s)   |
| --------------------------- | --------- | --------------------- | ---------------------------------------------------------------------------------------------------- | --------------- |
| DELTA_Mo98                  | 911       | CB_MA3_AE/CE          | Combustion/ashing, HNO3/HCl/HF, anion exchange (most AG1-X8 resin), cation exchange (AG50W-X8 resin) | ICP:MS-MC       |
| DELTA_Mo98                  | 180       | CB_MA2_AE/CE          | Combustion/ashing, HNO3/HF, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)          | ICP:MS-MC       |
| DELTA_Mo98                  | 161       | MA3_AE/CE             | HNO3/HCl/HF, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)                         | ICP:MS-MC       |
| DELTA_Mo98                  | 26        | CB_HCl(conc/boil)\_AE | Combustion/ashing, concentrated boiling HCl (3 times), anion exchange chromatography (AG1-X8 resin)  | ICP:MS-MC       |
| DELTA_Mo98                  | 21        | MA2_AE/CE             | HNO3/HF, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)                             | ICP:MS-MC       |
| DELTA_Mo98                  | 12        | ARrev_AE              | Reverse aqua regia digest, anion exchange chromatography (AG1-X8) (see Pearce et al. 2009)           | ICP:MS-MC       |
| DELTA_Mo98_CARB             | 148       | HCl(6N)\_AE/CE        | 6N HCl, anion exchange (AG1-X8 resin), cation exchange (AG50W-X8 resin)                              | ICP:MS-MC       |
| DELTA_Mo98_CARB             | 49        | HCl(6N)\_BHPA         | 6N HCl, BHPA resin chromatography (see Li et al. 2014)                                               | ICP:MS-MC       |
| DELTA_Mo98, DELTA_Mo98_AUTH | 236       | NULL                  | NULL                                                                                                 | CALC, ICP:MS-MC |
