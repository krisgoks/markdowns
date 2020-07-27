# Search medical codes for IMRD, Gold, Aurum, Cegedim and (soon) HES databases

Ever been in a situation where you had to create medical/drug codes for more than one EMR system? And worse, you had to do it individually for each database? Well, your worries are now over! With the help of this tool you can search for various medical codes and drug codes across different medical databases such as IMRD, CPRD Gold, CPRD Aurum and HES simultaneously.

# How to use?

First, click on ‘Medical codes’ or ‘Drug codes’ in the left sidebar to load codes you want to create today. The search can be conducted using various terms. If more than one field is populated at a time, then the app applies a logical OR operator between terms.

### Medical codes
To get medical codes you have the options to search any of the following fields. 
  
  |Search Field|Description|
  |--|--|
  |Medical Id| Medical Id is the actual term stored in the medical database that represents the code you are looking for, this might be a number, a short string or a hexadecimal value.  |
  |Description| This is the text description of the medical code|
  |Read code| Read Codes are a coded thesaurus of clinical terms. They have been used in the NHS since 1985. There are two versions: version 2 (v2) and version 3 (CTV3 or v3). Both versions provide a standard vocabulary for clinicians to record patient findings and procedures, in health and social care IT systems across primary and secondary care. <a href="https://digital.nhs.uk/services/terminology-and-classifications/read-codes" target="_blank">[1]</a> | 
  |SnomedCT code| SNOMED CT is a structured clinical vocabulary for use in an electronic health record. It is the most comprehensive and precise clinical health terminology product in the world. <a href="https://digital.nhs.uk/services/terminology-and-classifications/snomed-ct" target="_blank">[2]</a> |
  
### Drug codes
To get drug codes you have the options to search any of the following fields. 
  
  |Search Field|Description|
  |--|--|
  |Drug Id| Drug Id is the actual term stored in the drug database that represents the code you are looking for, this might be a number, a short string or a hexadecimal value.  |
  |Description| This is the text description of the drug code, this will also include (where available) the drug substance, strength, route of administration etc. |
  |BNF code| The BNF codes from this pseudo-classification are used in the prescribing dataset as a unique identifier to show what was prescribed. These BNF codes can tell you a lot about a drug or appliance. <a href="https://digital.nhs.uk/data-and-information/areas-of-interest/prescribing/practice-level-prescribing-in-england-a-summary/practice-level-prescribing-glossary-of-terms" target="_blank">[3]</a>|
  |ATC code| The Anatomical Therapeutic Chemical Classification System is a drug classification system that classifies the active ingredients of drugs according to the organ or system on which they act and their therapeutic, pharmacological and chemical properties. <a href="https://www.whocc.no/atc_ddd_index/" target="_blank">[4]</a>|
  
### Using Wildcard

Our tool supports the asterisk (\*) wildcard, it can be used to search for strings that are a subset of a bigger text. For example:
 - Searching medical codes descriptions with `*Type 1 diabetes` yields all the codes where the descriptions **ends with** the term 'Type 1 diabetes'
 - Similarly searching medical codes descriptions with `Type 1 diabetes*` yields all the codes where the descriptions **starts with** the term 'Type 1 diabetes'
 - Alternatively, you can just type `Type 1 diabetes` or you can use the asterisk operator as follows ```*Type 1 diabetes*``` to search for all medical codes whose description **contains** the term 'Type 1 diabetes'

# Downloading the file

To download the codes as a file make sure you have shortlisted the codes you are interested in and that these are populated in the second table, and then you can download the codes as csv files by providing a filename and clicking on the download button


---
# References
[1] https://digital.nhs.uk/services/terminology-and-classifications/read-codes

[2] https://digital.nhs.uk/services/terminology-and-classifications/snomed-ct 

[3] https://digital.nhs.uk/data-and-information/areas-of-interest/prescribing/practice-level-prescribing-in-england-a-summary/practice-level-prescribing-glossary-of-terms

[4] https://www.whocc.no/atc_ddd_index/
