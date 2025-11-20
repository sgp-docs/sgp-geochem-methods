#### Iron Isotopes

**Commonly cited method papers**

- Weyer and Schwieters, 2003 https://doi.org/10.1016/S1387-3806(03)00078-2
- Arnold et al. 2004 https://doi.org/10.1021/ac034601v
- Schoenberg and von Blanckenburg 2005 https://doi.org/10.1016/j.ijms.2004.11.025
- Huang et al. 2011 https://doi.org/10.1016/j.gca.2011.03.036
- Swanner et al. 2015 https://doi.org/10.1016/j.gca.2015.05.024
- Kunzmann et al. 2017 http://dx.doi.org/10.1016/j.gca.2017.04.003

**Notes**

Standard method includes a total acid digest (usually with HF, usually with combustion/ashing first to remove organics), followed by anion exchange chromatography using AG1X8, AG1X4 or AGMP-1 resin.

An intermediate acid step (e.g. taken up in HCl + heated) to ensure "complete dissolution of fluoride compounds" is sometimes described but not included in the code.

The majority of studies use sample-standard bracketing (+/- in combination with an internal Cu "element spike"), with one exception using double-spike. The most commonly cited method paper is Arnold et al. 2004.

Fe-isotopes in pyrite were measured in two studies (Duan et al. 2010, Ostrander et al. 2022) after a sequential extraction. From Duan et al 2010: _"a sequential extraction was carried out to quantify the following three individual Fe pools and in preparation for iron isotope analysis of the pyrite (Raiswell et al., 1988; Canfield 1989; Huerta-Diaz and Morse, 1990; Raiswell et al., 1994 ): (1) Fe HCl : extracted using 12 N boiling HCl for 1 min to target all Fe oxides and some of the Fe in clays, followed by (2) Fe Si : 10 N HF for 16 h to extract all residual alumino-silicate Fe and (3) Fe Py : 16 N HNO 3 for 2h to extract all pyrite Fe"_.

The **reference standard** for iron isotopes is IRMM-14.

| analyte(s)      | count_res | code          | translation                                                                                          | ana_method(s) |
| --------------- | --------- | ------------- | ---------------------------------------------------------------------------------------------------- | ------------- |
| DELTA_Fe56      | 145       | CB_MA3_AR_AE  | Combustion/ashing, HNO3/HCl/HF, aqua regia, anion exchange (AG1X4 resin), sample-standard bracketing | ICP:MS-MC     |
| DELTA_Fe56      | 125       | CB_MA3_AE     | Combustion/ashing, HNO3/HCl/HF, anion exchange (AG1X8 resin), sample-standard bracketing             | ICP:MS-MC     |
| DELTA_Fe56      | 120       | MA3b_AR_AE    | HNO3/HF/HClO4, aqua regia, anion exchange chromatography (AGMP1 resin), sample-standard bracketing   | ICP:MS-MC     |
| DELTA_Fe56      | 100       | MA3_AE        | HNO3/HCl/HF, anion exchange chromatography (AG1X8 or AGMP1 resin), sample-standard bracketing        | ICP:MS-MC     |
| DELTA_Fe56      | 61        | CB_MA2_AE     | Combustion/ashing, HNO3/HF, anion exchange (AG1X8 or AGMP1 resin), sample-standard bracketing        | ICP:MS-MC     |
| DELTA_Fe56      | 30        | MA2_AE        | HF/HNO3, anion exchange chromatography (AG1X8 resin), sample-standard bracketing                     | ICP:MS-MC     |
| DELTA_Fe56      | 26        | CB_MA4_AE     | Combustion/ashing, HCl/HF, HClO4/HNO3, anion exchange (AGMP1 resin), sample-standard bracketing      | ICP:MS-MC     |
| DELTA_Fe56      | 16        | CB_MA2_AE(DS) | Combustion/ashing, HF/HNO3, anion exchange chromatography Fe double-spike (Swanner et al. 2015)      | ICP:MS-MC     |
| DELTA_Fe56_AUTH | 121       | NULL          | NULL                                                                                                 | CALC          |
| DELTA_Fe56_PY   | 19        | SeqPy_AE      | Seq extract of pyrite with HNO3, anion exchange (AGMP1 resin), sample-standard bracketing            | ICP:MS-MC     |
| DELTA_Fe56_PY   | 18        | CB_SeqPy_AE   | Combustion/ashing, seq extract py w/ HNO3, anion exchange (AG1X8 resin), sample-standard bracketing  | ICP:MS-MC     |

---
