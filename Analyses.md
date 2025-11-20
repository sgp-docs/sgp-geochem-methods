## Analytical Methods

The analytical method is the final step of the geochemical analysis - how the measurements were taken. The majority are straightforward well-established methods e.g. ICP-MS, XRF, XRD.

CALC or STOICH includes all calculated data (e.g. TC-TIC for organic carbon), and results calculated by stoichiometry (e.g. Fe-py after CRS).

## Preparation Methods

The first step in most geochemical analyses is to crush and powder the rock. This is usually accomplished in several stages:

- Initial reduction into small pieces using a rock saw or hammer. This step often specifically includes the removal of weathered surfaces.
- Further reduction in size (in some cases) using e.g. a jaw crusher.
- Ground to a powder using a either a mill/shatterbox, or by hand with a mortar and pestle.

In some studies a microdrill is used in order to target specific mineral phases, or avoid areas of alteration. In rare cases no crushing is required e.g. XRF on a polished rock surface.

The material used in this process can impact the geochemical measurements. In the SGP database it is usually the final grinding step that is recorded (e.g. Alumina (ceramic) ball mill). In the case of steel, note that it is most often 'hardened' steel of some kind that is used. The exact material is sometimes specified (e.g. chrome, carbon), but most are lumped together simply as steel.

Note that sometimes pieces of the same hand sample are crushed in different ways, and therefore one sample can be associated with multiple preparation types. Samples with a long history associated with multiple studies can be difficult to trace - therefore some samples may be associated with a preparation type for some analyses and have no preparation type for others, if it was not clear whether the same powder was used.

## Experimental Methods

This category describes any experimental methods applied before a sample is analyzed - for example, acid digestion before ICP:MS.

Creating unique, simple, yet informative codes, is particularly challenging in this case. As a result this dictionary has been extensively revised since Phase 1, prompted partly by the addition of new carbonate and metal isotope data, and based on discussions with collaborators most familiar with the data.

Further revision is anticipated as we continue these discussions and add new kinds of data. While we aim to maintain stability in our dictionary terms, improving data quality is the first priority — so users should be aware that this dictionary in particular may not remain static.

The aim is to create codes which summarize essential steps, in particular if there is some debate over the relative strength of one method over another. Creating codes for newer, less established methods is generally the most difficult, as small variations in procedure are tested by different researchers. Where possible method papers, which set out all the key steps in detail, are linked to the code in the database (e.g. Poulton and Canfield, 2005 is linked to SeqA, B and C for iron speciation).

The codes are designed to be somewhat human-readable, and they are used in a modular way - the same code is used again if it is part of a longer protocol.

Standardized separators are used:

- Sequential steps are separated by an underscore. Example: CB_MA3 (combustion/ashing followed by a three-acid digestion).
- Details about a single step are enclosed in brackets and presented in a fixed order. Example: HCl(0.5N/24h/hot) (acid treatment with hot 0.5N HCl for 24 hours).
- Multiple components of a single step are separated by a slash. Example: HCl/HNO3 (two-acid digestion using HCl and HNO3).

The experimental method dictionary has three columns (based on the schema from the British Geological Survey): the experimental_method_code, experimental_method_translation and experimental_method_desc. Each is slightly more detailed than the last. The code and translation are available on the website.

The sections below summarise methods based on the categories on the website. The tables are based around experimental methods which tend to be most specific to each category (whereas the analytical methods are more likely to be used across different groupings). Analytes and analytical method codes are grouped by category and then by experimental code, and usually sorted by number of results within a given category (the approach varies slightly depending what makes most sense for a given category).

These summaries are based on the studies that are included in SGP Phase 2, and therefore are not intended as a complete review or recommendation of methods, but rather to give a sense of the data currently available.

**Commonly cited papers** are subjectively taken from the methods sections of published papers, where we see the same citation turning up frequently - we note these are based on frequency and do not represent any suggestion/endorsement of a specific methodological approach.

Where SGP **Proxy Primers** are available, they are linked to the relevant section - these provide a detailed review of proxy use.

**Reference standards** for isotopic measurements refer to the standards currently associated with data in the SGP database; note these may not represent all standards commonly used in the broader field.

## Above/Below Detection

Abundance can only be empty (NULL) if a value is explicitly recorded as above or below detection. Where possible the detection limits are also stored. Note that since the Simple and Detailed searches will average results, measurements above or below detection limits will also be removed, as they cannot be averaged. This is important for studies of analytes whose abundances are near detection limits for common geochemical methodologies—in the case of low-abundance elements, most analyses (i.e., below detection) will be removed, and only anomalously ‘high’ analyses will be returned.

Values above detection are rare (0.3% of the total). Below detection values are more common (19.5% of the total). A large proportion of these come from the USGS-NGDB dataset. Summary tables of total counts and percents above and below detection for all data, and for each data source are linked below.

Miscellaneous useful references:

Balaram, V., & Subramanyam, K. S. V. (2022). Sample preparation for geochemical analysis: Strategies and significance. Advances in Sample Preparation, 1, 100010. https://doi.org/10.1016/j.sampre.2022.100010
