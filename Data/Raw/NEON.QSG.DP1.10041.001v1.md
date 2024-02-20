# Mosquito pathogen status (DP1.10041.001)

## Measurement
Presence or absence of arboviruses in female mosquitoes within the families Bunyaviridae, Alphaviridae, and Flaviviridae. Pathogens tested for include West Nile virus, Eastern equine encephalitis virus, La Crosse virus, and more. Female mosquitoes that have been identified to species and occur in sufficient quantity at a site over a season are eligible for pathogen testing.

## Collection methodology
Tier 1 species (Aedes aegypti and Aedes albopictus) receive top testing priority and are tested from each site with a minimum of 100 specimens available in a year. The next two lower priority groups for testing include Tiers 2 (Culex tarsalis, Culex pipens, and Aedes triseriatus) and 3 (any other individual identified to species within genera Aedes or Culex). These are targeted for testing when a minimum of 200 individuals per site per year are collected. Groups of individuals for testing are assigned a testingID and grouped into pools of 10-50 by species and sampling bout. Because mosquito pathogens are rare, vials are first tested for infection at the genus-level for the three genera of interest (Flavivirus sp., Orthobunyavirus sp., Alphavirus sp.). If the vial tests positive for a given genus of pathogen, the pathogen-specific tests within that genus are performed.

For information about disturbances, land management activities, and other incidents that may impact data at NEON sites, see the [Site management and event reporting (DP1.10111.001)](https://data.neonscience.org/data-products/DP1.10111.001) data product.

## Data package contents
mos_pathogenqa: Mosquito pathogen testing quality assurance data from external labs  
mos_pathogenresults: Mosquito pathogen testing results from external labs  
mos_pathogenpooling: Mosquito pathogen pool size information from external labs  
variables: Description and units for each column of data in data tables  
readme: Data product description, issue log, and other metadata about the data product  
validation: Description of data validation applied at the points of collection and ingest  

## Data quality
The percentIdentity field in the mos_pathogenresults table reports the percentage match between the sample sequence and the reference sequence used to identify the pathogen. The lab quality assurance data in the mos_pathogenqa table, in the expanded data package contains data on controls included during PCR testing. Each plate contains a positive control to verify detection of known pathogens as well as two negative controls (one extraction control and one master mix control) to check for contamination. Samples are re-run if any controls fail. Beginning in 2021, the batchID field can be used to connect the pathogen data to the lab quality assurance data. 
  
## Standard calculations
For wrapper functions to download data from the API, and functions to merge tabular data files across sites and months, see the [neonUtilities R package](https://cran.r-project.org/web/packages/neonUtilities/index.html).

If the virus family test for a given sample is positive it will be tested at the species level. Additionally, the same testingVialID is tested for multiple pathogens. This means when calculating the denominator (number tested) for prevalence, the results must be filtered by testPathogenName.
  
## Table joining
|Table 1|Table 2|Join by field(s)|
|------------------------|------------------------|-------------------------------|
mos_pathogenpooling|mos_pathogenresults|testingVialID
mos_pathogenresults|mos_pathogenqa|Simple join not recommended. BatchIDs used for joining are replicated in both tables such that joining tables results in repeated records.  It is recommended to convert the pathogenqa table to wide format with multiple columns for controlType, then join by batchID.
mos_expertTaxonomistIDProcessed|mos_pathogenpooling|testingID
mos_expertTaxonomistIDRaw|mos_pathogenpooling|testingID
  
## Documentation
- [Laboratory of Medical Zoology Mosquito Testing Standard Operating Protocol. Ver 2.1. Modified Date: 3/3/2021](https://data.neonscience.org/api/v0/documents/LMZ_SOP_Mosquito_2.1_20210303)  
LMZ_SOP_Mosquito_2.1_20210303 | 1.2 MiB | PDF  
- [TOS Science Design for Mosquito Abundance, Diversity, and Phenology](https://data.neonscience.org/api/v0/documents/NEON.DOC.000910vC)  
NEON.DOC.000910vC | 532 KiB | PDF  
- [TOS Science Design for Vectors and Pathogens](https://data.neonscience.org/api/v0/documents/NEON.DOC.000911vC)  
NEON.DOC.000911vC | 1.9 MiB | PDF  
- [TOS Protocol and Procedure: MOS – Mosquito Sampling](https://data.neonscience.org/api/v0/documents/NEON.DOC.014049vM)  
NEON.DOC.014049vM | 2.5 MiB | PDF  
- [NEON User Guide to Mosquitos Sampled From CO2 Traps (DP1.10043.001) and Mosquito-borne Pathogen Status (DP1.10041.001)](https://data.neonscience.org/api/v0/documents/NEON_mosquito_userGuide_vE)  
NEON_mosquito_userGuide_vE | 244.6 KiB | PDF  

For more information on data product documentation, see:  
https://data.neonscience.org/data-products/DP1.10041.001  

## Citation
To cite data from Mosquito pathogen status (DP1.10041.001), see citation here:  
https://data.neonscience.org/data-products/DP1.10041.001  
For general guidance in citing NEON data and documentation, see the citation guidelines page:  
https://www.neonscience.org/data-samples/guidelines-policies/citing  
