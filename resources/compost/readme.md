# A compost research

this could be an interesting dataset to investigate how it best be published

## Material 

- a [dataset](https://ilvo.sharepoint.com/:x:/r/sites/HESoilWiseProject/_layouts/15/Doc.aspx?sourcedoc=%7B7FC4E1FC-2097-46C2-A200-5479A04FB5B3%7D&file=20250704_Soilcom_compost_database_Soilwise.xlsx&action=default&mobileredirect=true)
- a report

## Platform

- Zenodo/Open data portal/...

## Metadata

- Which metadata model (depends on platform?)
- which vocabulairy for subjects (keywords)
- can LLM be used to generate metadata from context (report/dataset)
- How to capture data model (column metadata) in metadata (or additional file)
- How can users benefit practically from the above efforts (better findability, better interoperability, ...)

## CSVW Approach
- CSV version of the xsl dataset (R_alles tab) above
- CSVW JSON-LD Metadata for this dataset
- CSV version of the xsl dataset (var_defs tab) above
- JSON Mapping file

Issues in this work:
- How to deal with additional info in UoM, e.g. 'substrate' or 'fresh matter'? Shouldn't be in UoM, think actually goes to ObsProp, ideally we'd have I-ADOPT where this would be either the Matrix or a constraint.
- Some of this info from comment is relevant, currently ignored
- Various base URIs used in the examples, e.g. for ObsProps, Procedures, are missing
- Some numeric values, e.g. NO3_N, are prefixed with a '<' sign, unclear if this is below threshold, as different values
- Currently the observational part of the CSVW JSON-LD doesn't have a FoI or phenomenonTime, as this is available from previous columns. Do we leave it this way, or do we integrate this into each Observation column description?
 
