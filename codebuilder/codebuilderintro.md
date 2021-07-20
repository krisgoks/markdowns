
# Search medical codes for IMRD, Gold, Aurum, Cegedim and HES databases

Ever been in a situation where you had to create medical/drug codes for more than one EMR system? And worse, you had to do it individually for each database? Well, your worries are now over! With the help of this tool, you can search for various medical codes and drug codes across different medical databases such as IMRD, CPRD Gold, CPRD Aurum and HES simultaneously.

# How to use?

Click on ‘Medical codes’ or ‘Drug codes’ in the left sidebar to load codes you want to create today. The search can be conducted using various terms. If more than one field is populated at a time, then the app applies a logical OR operator between terms. 

### Naming convention 

This tool documents the email id of the person who created the code list and the date time of creation, so the name of the code lists you create should only need to include a clinical term. For example, a code list for Interstitial Lung Disease could simply be named ILD. We encourage you to select a simple, generic name without adding any personal trinkets. Remember, the goal is to help and reach a wider audience.

All the codes you create must have a unique name. You cannot have more than one code list with the same name under your account. The name you assign can only contain alphanumeric characters with optional underscore. No white spaces allowed or any other special symbols.

### Medical codes
To get medical codes you have the options to search any of the following fields. 
  
  |Search Field|Description|
  |--|--|
  |Medical Id| Medical Id is the actual term stored in the medical database that represents the code you are looking for, this might be a number, a short string, or a hexadecimal value.  |
  |Description| This is the text description of the medical code. |
  |Medical code| This field may either represent ICD-10 codes or Read codes. ICD-10 is the 10th revision of the International Statistical Classification of Diseases and Related Health Problems, a medical classification list by the World Health Organization [1](https://en.wikipedia.org/wiki/ICD-10). Read Codes are a coded thesaurus of clinical terms. They have been used in the NHS since 1985. It provides a standard vocabulary for clinicians to record patient findings and procedures, in health and social care IT systems across primary and secondary care. [2](https://digital.nhs.uk/services/terminology-and-classifications/read-codes) | 
  |SnomedCT code| SNOMED CT is a structured clinical vocabulary for use in an electronic health record. It is the most comprehensive and precise clinical health terminology product in the world. [3](https://digital.nhs.uk/services/terminology-and-classifications/snomed-ct) |
  
### Drug codes
To get drug codes you have the options to search any of the following fields. 
  
  |Search Field|Description|
  |--|--|
  |Drug Id| Drug Id is the actual term stored in the drug database that represents the code you are looking for, this might be a number, a short string, or a hexadecimal value.  |
  |Description| This is the text description of the drug code, this will also include (where available) the drug substance, strength, route of administration etc. |
  |BNF code| The BNF codes from this pseudo-classification are used in the prescribing dataset as a unique identifier to show what was prescribed. These BNF codes can tell you a lot about a drug or appliance. [4](https://digital.nhs.uk/data-and-information/areas-of-interest/prescribing/practice-level-prescribing-in-england-a-summary/practice-level-prescribing-glossary-of-terms)|
  |ATC code| The Anatomical Therapeutic Chemical Classification System is a drug classification system that classifies the active ingredients of drugs according to the organ or system on which they act and their therapeutic, pharmacological, and chemical properties. [5](https://www.whocc.no/atc_ddd_index/)|
  
### Using Wildcard

Our tool supports following wildcards, asterisk (\*), underscore (\_) and percentage (\%). Using these operators you can search for strings that are a subset of a bigger text. For example:
 - Searching medical codes descriptions with `*Type 1 diabetes` yields all the codes where the descriptions **end with** the term 'Type 1 diabetes'
 - Similarly searching medical codes descriptions with `Type 1 diabetes*` yields all the codes where the descriptions **start with** the term 'Type 1 diabetes'
 - Alternatively, you can just type `Type 1 diabetes` or you can use the asterisk operator as follows ```*Type 1 diabetes*``` to search for all medical codes whose description **contains** the term 'Type 1 diabetes'
 - (\_) underscore represents a single character to match; For example, if we search `Type _ diabetes` our results will include a range of terms such as, Type `1` diabetes, Type `2` diabetes, Type `I` diabetes, etc.
 - (\%) percentage operator matches zero, one or more characters; searching for `hyp%tion` would yeild results such as Hyp`erkinetic reac`tion, Hyp`ersecre`tion, Hyp`erpigmenta`tion, hyp`erten`tion, and so on...

### Filtering codes

You will be filtering the table to either delete the codes you do not need or to select just those few that are important to you, either way, codes can be filtered in two ways. One option is to use the search bar which performs an overall keyword search as you type across all columns of the table. Another option is to use the filtering functionality to apply keyword filters on columns you are interested. The former is handy when the table size is < ~15K lines, please use the later if the number items in the table is > ~15K.

### Downloading the code lists as files

To download the codes as files, make sure you have shortlisted the codes you are interested in and that these are populated in the second table, and then you can download the codes as .csv files by providing a filename and clicking on the download button. You can also download existing code lists from the library.

### Saving the code lists 

Saving codes in the database is like the download process, but here you will press the save button instead of download. If the database contains a code-list with the same name as the current one, then an overwrite prompt will be presented to you. You can choose to overwrite existing data or press no and change the name and try saving it again. 

*please see naming convention section on how to name your code-lists.*

### Viewing code lists in the library 

In the library tab you can view the codes you have previously created and search for codes created by other users. There is an option to download the code list here as well.


### Editing code lists 

You can load any code list from the library to the medical codes or drug codes page regardless of who the owner is and add or remove codes according to your interest. Although you cannot overwrite somebody else's code you can save a copy of it for yourself. Or if you are editing your own code-list you can save it as a new object by giving it a new name or choose to overwrite the current object (by not changing its current name and pressing save).

*please see naming convention section on how to name your code-lists.*

### Uploading code lists - beta version

You can upload existing code lists stored in .csv files into the appropriate library. To access this, click on the 'Upload a file' tab. The expectation is that the .csv file has a **header**, and the codes are in the first column. The software assumes you are uploading the actual medical/drug ids as present in the medical/drug tables in the database. Depending on the database this might be a number, a short string, a hexadecimal value, or may be terms from a clinical coding system. Once you upload the file the software will read the first column (**after skipping the first line**) and look for those codes in the current version of dictionary, if found it will be listed with descriptions and database name. It will also shortlist any codes which may not be present in the dictionary, these will be ignored and cannot be added as of now.

*If you come across a clinical code which you found somewhere else and this code is not present in our dictionary please contact the admin. Please state where you found the code, specify dictionary version to which the code belongs to, and if possible, evidence that this code actually exists in the underlying medical database.*

You can add codes from multiple files to one list, for example you may have lung disease codes for CPRD Aurum, CPRD Gold, IMRD and ICD10 stored in separate .csv files and you wish to upload these codes to the system but store it under one code list named "LungDisease" rather than create 4 disparate lists. To do this, first choose the appropriate database option and then upload the corresponding file and repeat this process till you have added all other related files to this list and in the end press save.


# External code browsers and tools to look for code lists

- [OpenSAFELY Codelists](https://codelists.opensafely.org/)
- [Caliber code list](https://caliberresearch.org/portal/codelists)
- [QoF](https://digital.nhs.uk/data-and-information/data-collections-and-data-sets/data-collections/quality-and-outcomes-framework-qof/quality-and-outcome-framework-qof-business-rules/quality-and-outcomes-framework-qof-business-rules-v37-0)
- [Manchester code list (optional)](https://clinicalcodes.rss.mhs.man.ac.uk/medcodes/articles/)
- [Cambridge code list](https://www.phpc.cam.ac.uk/pcu/research/research-groups/crmh/cprd_cam/codelists/v11/)
- [SnomedCT code browser SNOMEDCT - Clinical finding](https://www.termbrowser.nhs.uk)
- [ICD-10 browser](https://icd.who.int/browse10/2019/en#/)
- [NHS medication browser tool](https://applications.nhsbsa.nhs.uk/DMDBrowser/DMDBrowser.do#)



# Dictionary update

The following table provides information on when was the last time the source dictionaries were updated and what was the source of the dictionary.

  |Database| Current Version | Previously Updated On | Source | 
  |--|--|--|--|
  |Medical - (IQVIA)IMRD and/or (Cegedim)THIN | 29 Jun 2021 | 22 Feb 2021 | Cegedim Feb 2021 Read code data dictionary |
  |Medical - (CPRD)Gold | 8 Feb 2021 | - | CPRD Gold Jan 2021 medical code dictionary |
  |Medical - (CPRD)Aurum| 19 Jul 2021 | Aug 2020 | CPRD Aurum July 2020 medical code dictionary |
  |Medical - (HES)ICD10 | Apr 2020 | | [NHS ICD-10 5th Edition data files](https://isd.digital.nhs.uk/trud3/user/authenticated/group/0/pack/1/subpack/258/releases) |
  |Drug - (IQVIA)IMRD | 29 Jun 2021 | Sept 2019 | IMRD Sept 2019 drug code dictionary |
  |Drug - (Cegedim)THIN | 22 Feb 2021 | - | Cegedim Feb 2021 drug code dictionary |
  |Drug - (CPRD)Gold | 8 Feb 2021 | - | CPRD Gold Jan 2021 drug code dictionary |
  |Drug - (CPRD)Aurum| 19 Jul 2021 | Aug 2020 | CPRD Aurum July 2020 drug code dictionary |

# Feedback

If you have any feedback or suggestions, please write to me at [k.m.gokhale@bham.ac.uk](mailto:k.m.gokhale@bham.ac.uk), mention 'TheOneCodeBuilder - feedback/suggestion' in the subject. If you are reporting any bugs please mention 'TheOneCodeBuilder - bugs' in the subject and please do send a [Minimal, Reproducible Example](https://stackoverflow.com/help/minimal-reproducible-example).

# Roadmap

The following are some of the new features we are experimenting. However, these features may change significantly before they are incorporated into the app or it may not be implemented after all. 

- Advanced Search.
