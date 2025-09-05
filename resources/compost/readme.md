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
- [How to deal with additional info in UoM](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/3), e.g. 'substrate' or 'fresh matter'? Shouldn't be in UoM, think actually goes to ObsProp, ideally we'd have I-ADOPT where this would be either the Matrix or a constraint.
- [Some of this info from comment is relevant, currently ignored](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/4)
- Various base URIs used in the examples, e.g. for [ObsProps](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/5), [Procedures](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/6), are missing
- Some numeric values, e.g. NO3_N, are [prefixed with a '<' sign](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/7), unclear if this is below threshold, as different values
- Currently the observational part of the CSVW JSON-LD doesn't have a FoI or [phenomenonTime](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/8), as this is available from previous columns. Do we leave it this way, or do we integrate this into each Observation column description?
- Do we also take the [administrative metadata](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/9) stored under meta_descriptive into account. If so, we need to find places for this
- At present, the [ObsProp is duplicated](https://github.com/soilwise-he/UC4-C2-resource-annotation/issues/10), stored once under "propertyUrl", once under "oms:observedProperty".
- To support both international and national/local standards under ObservingProcedure, we propose providing both, starting at the highest level (international, e.g. ISO), then using skos:narrower to link in national/local versions of these standards
  -  for discussion: we could also use skos:broader, or sameAs, or...?
