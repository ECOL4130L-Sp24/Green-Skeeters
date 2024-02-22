# Rodent pathogen status, hantavirus (DP1.10064.001)

## Measurement
Results of pathogen tests on small mammal blood samples collected from 2014-2019. Samples were tested for seropositivity to Hantaviruses. 

## Collection methodology
Blood samples are collected using the submandibular method from target species in the families Cricetidae, Muridae, and Dipodidae if the individual meets criteria of good physical condition and weighs more than 10 grams. Blood samples are only collected on pathogen grids and only collected once per individual per bout. Once samples are collected, they are immediately labeled and stored on dry ice in the field and transferred to the -80 °C freezer in the laboratory. Up to 20 blood samples are collected per plotID per collectDate from the targeted families.  

For information about disturbances, land management activities, and other incidents that may impact data at NEON sites, see the [Site management and event reporting (DP1.10111.001)](https://data.neonscience.org/data-products/DP1.10111.001) data product.

## Data package contents
rpt_bloodtesting: Rodent pathogen antibody data from external lab  
variables: Description and units for each column of data in data tables  
readme: Data product description, issue log, and other metadata about the data product  
validation: Description of data validation applied at the points of collection and ingest  

## Data quality
The sampleCondition field indicates the condition of the sample at the time of pathogen testing. Lot numbers for controls and sample diluent are included in the expanded data package, as well as data regarding dilution of controls and/or samples, and the raw optical density data from the test.  

## Table joining
|Table 1|Table 2|Join by field(s)|
|-----------------|----------------|-------------|
rpt_bloodtesting|mam_pertrapnight|bloodSampleID|  

## Documentation
- [TOS Protocol and Procedure: MAM – Small Mammal Sampling](https://data.neonscience.org/api/v0/documents/NEON.DOC.000481vO)  
NEON.DOC.000481vO | 3.4 MiB | PDF  
- [TOS Science Design for Vectors and Pathogens](https://data.neonscience.org/api/v0/documents/NEON.DOC.000911vC)  
NEON.DOC.000911vC | 1.9 MiB | PDF  
- [TOS Science Design for Small Mammal Abundance and Diversity](https://data.neonscience.org/api/v0/documents/NEON.DOC.000915vC)  
NEON.DOC.000915vC | 1.6 MiB | PDF  
- [NEON User Guide to Rodent Pathogen Status, hantavirus (DP1.10064.001)](https://data.neonscience.org/api/v0/documents/NEON_rodentPathogen_userGuide_vD)  
NEON_rodentPathogen_userGuide_vD | 340.5 KiB | PDF  
- [VRL Enzyme Linked Immunosorbant Assay (ELISA) Description](https://data.neonscience.org/api/v0/documents/VRL_Pathogen_Testing_040603-2006-01)  
VRL_Pathogen_Testing_040603-2006-01 | 149.6 KiB | PDF  

For more information on data product documentation, see:  
https://data.neonscience.org/data-products/DP1.10064.001  

## Citation
To cite data from Rodent pathogen status, hantavirus (DP1.10064.001), see citation here:  
https://data.neonscience.org/data-products/DP1.10064.001  
For general guidance in citing NEON data and documentation, see the citation guidelines page:  
https://www.neonscience.org/data-samples/guidelines-policies/citing  
