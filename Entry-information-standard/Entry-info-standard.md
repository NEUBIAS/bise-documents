Entry information standard
===================================
BIII.eu software entry information standard 
----------------------------------
The standard described here (still under discussion) provides guidelines to support [BIII.eu webtool](http://www.biii.eu/) curators to monitor the webtool content and tagging. This standard was adapted from the [Tool information standard](https://github.com/bio-tools/biotoolsSchemaDocs/blob/master/information_standard.rst#biotools-information-standard) documentation from [ELIXIR bio.tools](https://github.com/bio-tools/). Thanks to [Jon Ison](https://github.com/joncison) for referencing this documentation. 

This standard comprises a list of entry attributes to be specified for a software entry to be classified in a 5 tier rating of entry completeness and quality in BIII.eu.

BIII.eu includes two ontologies on its framework: [Bise core ontology](https://github.com/NeuBIAS/bise-core-ontology) and [EDAM-Bioimaging](https://github.com/edamontology/edam-bioimaging>). 

In addition we provide curation guidelines describing how each attribute should be specified to ensure the quality of BIII.eu entries. These guidelines are not limited to the syntatic and semantic constraints defined by EDAM-bioimaging ontology and BISE-core-ontology

The standard provides a basis for monitoring of content and labelling of BIII.eu entries initially by: 

* **Entry completeness** (5 tiers being "SPARSE", "BASIC DETAILS", "DETAILED", "HIGHLY DETAILED" and "COMPREHENSIVE")

![](Table.png)
![](Table_groups.png)

The standard is applied to BIII.eu as follows (condensed information available from the tables): 

* **"SPARSE"**: Minimum information requirement for new entries. A SPARSE entry may be invisible in the webtool (and made it clear to the curator adding the entry in the UI) by default and will only show after aditional information is added (similar to what occurs in bio.tools). A sparse entry has a _Name_, _Description_, _Unique ID_ (automatically created) and _type_ (collection, component, worflow, don't know). This category may not conform to biii.eu curation guidelines and for curation purposes, such entries must be shown in the list of 'to be curated' of confirmed taggers somehow as 'high priority'
  
* **"BASIC DETAILS"**: Entries with basic details may be shown in the webtool searches and list of entries. In addition to the attributes from the sparse entry, an entry with 'Basic details' shall have _implementation type_ (Library, plugin, standalone, and web application), _Entry point_ (URL of the repository or 'official' website), an _illustrative image_ (preferably a screenshot of the UI, or the input/output results, but logo whenever it fits), _author_ ( in the form of `LastName, FirstName (ORCID ID)`) and at least one _function_ (EDAM-Bioimaging Operation Class, for example, model-based segmentation or object feature extraction). This category may not conform to biii.eu curation guidelines and for curation purposes, such entries must be shown in the list of 'to be curated' of confirmed taggers somehow as 'high priority'

* **"DETAILED"**: This is the mid-completeness category. In this category there must be at least one attribute from the _Accesibility_ and _Use information_ groups. In addition, the _programming language_ of the tool is defined as well as its _execution platform_ (Operating System). This category may not conform to biii.eu curation guidelines and for curation purposes, such entries must be shown in the list of 'to be curated' of confirmed taggers without any warning. 

* **"HIGHLY DETAILED"**: Higly detailed entries include at least one attribute from the _Documentation_ group, at least one _Topic_ (EDAM-Bioimaging Topic Class, for example, fluorescence microscopy, Single molecule localization miroscopy and machine learning). Highly detailed entries also must have at least one _biological term_ and the DOI of its implementation. Since DOIs of implementations are not the rule, this is an optional attribute (See also: [Making your code citable](https://guides.github.com/activities/citable-code/) and [DOI Registrations for software - DataCite Blog](https://blog.datacite.org/doi-registrations-software/)).

* **"COMPREHENSIVE"**: Such entries would provide relevant information to users of all backgrounds and are useful resources. The entry attributes will link to information such as a repository, reference publication, training material and will potentially have several related Biological terms, EDAM-Bioimaging Operations and Topics. 
