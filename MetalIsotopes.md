### Metal Isotopes

Metal isotope analysis generally includes

- leach/digestion step
- a purification step (chromatography)
- measurement by ICP:MS-MC or TIMS/NTIMS
- analytical correction (double-spike/standard sample bracketing)

In SGP the experimental code aims to capture the digestion and purification steps in as much relevant detail as possible. Thus far we do not include information in the code itself about analytical correction methods (e.g. mass-bias correction) such as double-spike or standard sample bracketing. For the most part the approach used tends to be standardized within a given isotopic system; in some instances double-spike and bracketing are used in combination.

Given the methodological complexity and the inconsistency in how procedures are reported across the literature, some degree of compromise has been necessary. These codes are a work in progress, and feedback is welcome.

**Digestion**

SGP uses the same codes for this step as for elemental digests (see below) e.g. CB_MA3. If the digest is partial or light the strength of the acid is included e.g. HCl(0.25N).

Steps between the initial digest and purification are difficult to code in a standardized way. These may include e.g. +/- HClO₄ +/-H₂O₂, secondary acid treatments, and various additional heating steps (e.g., microwave, ashing\*). While these intermediate treatments often serve the same purpose (e.g. to prevent issues such as fluoride precipitation or to oxidize organics) they can vary in order, composition, and intensity across labs and publications. In some cases, it is not clear if these steps were included but not explicitly mentioned (authors may link to a citation which is ambiguous, or cite papers several layers deep). Users should be aware, therefore, that these steps are often not included in the code and we recommend consulting the original publications for details.

\*Note that if combustion/ashing is part of the initial digest, we do aim to include it in the code - we refer here to steps between initial digest and chromatography

**Purification**

In addition to the acid digest, the code captures the use of ion exchange (IE) or more specifically anion exchange (AE), cation exchange (CE), or a combination of both.

Where possible, we also attempt to capture the number of purification steps or columns. However, terminology in the literature is inconsistently applied: the term "step" may refer to either multiple elution stages on a single column, or to multiple columns used in sequence. Similarly, "stage" can be ambiguous (e.g., “two-stage” vs. “two-step”), and usage varies across isotope systems, and sometimes within a single isotope system (albeit less common).

As a result, SGP includes a numerical prefix (e.g., "2AE") where publications consistently refer to the number of steps, stages, or columns, and particularly if a distinction is explicitly drawn between methods within one isotope system.

Resins and eluents are generally not included in the purification code, as most isotope systems use standard combinations. However, resins are noted in the full experimental method description. When a non-standard resin is used (e.g., TRU resin instead of UTEVA for uranium), this is included in the code to highlight significant deviations from the norm.

**Isotope Dilution**

Element concentrations are sometimes/often measured alongside isotopes by isotope dilution methods. We note that, on occasion, it can be difficult to tell in a data table whether an element has been measured with the isotopes, or with other elements by e.g. standard acid-digest and ICP:MS etc.
