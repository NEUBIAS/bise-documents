# Guidelines to BIII.eu curators

BIII.eu is a web-based database that includes bioimage analysis tools, such as Software, Training material and Datasets. The guidelines here (under construction) presented will help confirmed taggers add and curate _software_ entries into BIII.eu only. The software entry of the webtool include from simple _components_, such as a gaussian filter, to image processing libraries (_collections_ of components) and _workflows_ (e.g. single particle tracking workflows). 

The detailed description of the types of tools that can be included in BIII.eu webtool are still under discussion. However, we ask curators and taggers to include only tools that can be used and relate to image analysis problems in biology (a.k.a bioimage analysis). 

The tools are described using two ontologies, [**BISE-core-ontology**](https://github.com/NeuBIAS/bise-core-ontology) and [**EDAM-Bioimaging**](https://github.com/edamontology/edam-bioimaging). **BISE-core-ontology** contains the structure of description of entries in BIII.eu, not only software, and includes entry properties such as author, reference publication, curator and so on. **EDAM-Bioimaging** is used as a source of terms to describe the entry with Bioimaging related vocabulary.  

>In BISE, a software entry describes a bioimage analysis tool, which can be classified as a _component_, a _collection_ or a _workflow_. A _component_ is an implementation of certain image processing / analysis algorithms. Each component alone does not solve a Bioimage Analysis problem. These problems can be addressed by combining such components into workflows. On the orhter hand, a _workflow_ is a set of components assembled in some specific order to process bioimages and estimate some numerical parameters relevant to the biological system under study. Workflows take image data as input and output either processed images or other type of data (usually numeric values). Workflows can be a combination of components from the same or different software packages. Finally, a _collection_ is a software that encapsulate a set of bioimage components and/or workflows, e.g. libraries such as **imglib2** and **scikit-image** or general purpose software such as **Fiji**, **Icy**.

OBSERVATION: These curation guidelines were inspired by [biotoolsDocs](https://github.com/bio-tools/biotoolsDocs/blob/master/github_projects.rst) documentation. Part of it has been adapted or used as is from the original **biotoolsDocs**. Thanks to Jon Ison for referencing biotools documentation efforts. 

If you wish to suggest changes or additions to this documentation, please raise an issue to begin the discussion. 

# How and what to curate? 

When you add a new content, you will notice that a similar named tools exist. Please check if it is the same tool(s) you wanted to tag, if not, name it differently (example: Erosion (Icy) vs Erosion (MorpholibJ)). The purpose is to have a unique title for each entry. Whenever possible, try to add both the _collection_ and an entry by _component_(s): e.g. MorpholibJ is an ImageJ plugin, and an entry by function (erosion in MorpholibJ, watershed in MorpholibJ etc... are all components inside MorpholibJ). The purpose is then to help analysts to find the component they need when constructing a bio image analysis workflow.

Try to fill as many fields as possible. If one field definition is unclear, report in the [BIII.eu forum](http://biii.eu/forum) or raise an issue in github [bise documents repository](https://github.com/NeuBIAS/bise-documents).


>The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt>):

>- **"MUST"**, **"REQUIRED"** or **"SHALL"** mean that the guideline is an absolute requirement of the specification.
>- **"MUST NOT"** or **"SHALL NOT"** mean that the guideline is an absolute prohibition of the specification.
>- **"SHOULD"** or **"RECOMMENDED"** mean that there may exist valid reasons in particular circumstances to ignore a particular guideline, but the full implications must be understood and carefully weighed before doing so.
>- **"SHOULD NOT"** or the phrase **"NOT RECOMMENDED"** mean that there may exist valid reasons in particular circumstances when acting contrary to the geuideline is acceptable or even useful, but the full implications should be understood and the case carefully weighed before doing so.
>- **"MAY** or **"OPTIONAL"** mean that the guideline is truly optional; you can choose to follow it or not.
    
# General guidelines
## Before you start

Consider the following *before* adding a software entry in BIII.eu

1. **Are one or more entries required to describe the software?**

   - Software with multiple implementations often require multiple entries. Example: SOAX - has 2 different ways of downloading it: One is the windows standalone executable and the second is the source code, which will require one to compile it in any OS (requiring ITK, VTK and Boost C++ libraries). In that case, the best way is to create two entries: one by location of download since it is actually two different software then, and evrey entry should have only one dowload page (has location). In one entry there is only windows as the supported platform, while in the other, any OS. 
   - Collections also often require multiple entries. Example: Simple Neurite Tracer (existing entry) is an ImageJ-Fiji plugin which has three workflow options available: 2 semi-automated and 1 fully automated. In this case, one would create one entry for Simple Neurite Tracer (the plugin) as a _Collection_, then one entry by example workflow, and specify the difference in the title. You will have one plugin, and 3 workflows requiring the plugin Simple Neurite Tracer.
   - tools with multiple interfaces (not described in bise-core-ontology) **SHOULD** be described by a single entry **unless** these interfaces provide fundamental functional differences. 
   - if in doubt, post in BIII.eu forum or contact confirmed taggers or admin.
     
2. **What if the software is already registered?** 

- if you are the rightful owner of the entry (*i.e.* the tool developer or provider of an online service) and you are a confirmed tagger, change the field _entry curator_ to your username. In case you are not a confirmed tagger, ask for modification in the BIII.eu forum. 

- if you are a normal user but wishes to suggest modifications to an existing entry, post in the BIII.eu forum and describe your suggestions.
     
3. **Are there version-specific considerations?**

   - as a rule, a software entry in BIII.eu **SHOULD** describe the *latest version* available at the time of registration and **SHOULD** be updated, as required, for subsequent releases.
   - if a new version has fundamental functional differences it **MAY** be registered as an entirely new entry.  In such cases, follow carefully the guidelines for entry **name** and **version** (under construction). 
   
4. **Plan** how to describe the entry functions (under construction). 
5. **Read** the general EDAM annotations guidelines (under construction). 

# Attribute Guidelines

The guidelines below are organized into sections as they appear in the _create software_ page in BIII.eu webtool. 

## Name (Software) 

Canonical software name assigned by the tagger, preferably the software developer or service provider, e.g. "Fiji"


**1.** **MUST** use name in common use, *e.g.* in the tool homepage or publication.

**2.** **MUST** use short form if available *e.g.* ``MaMuT`` **not** ``MaMuT: A Fiji plugin for the annotation of massive, multi-view data``.

**3.** **MUST NOT** include general or technical terms ("software", "application", "server", "service", "plugin", "app", "add-on" *etc.*) *unless* these are part of the common name

**4.** **MUST NOT** misappropriate the names of other tools, *e.g.* there are many _Erosion_ implementations; Calling any of them "Erosion" would be wrong

**5.** **MUST NOT** include version information *unless* this is part of common name (under discussion - there is still no field for version) 

**6.** **SHOULD** preserve capitalisation *e.g.* ``MaMuT`` **not** ``mamut``.

**7.** **SHOULD** follow the naming patterns (see below)

> ## Naming Patterns
>   For components that are part of a collection, use the pattern 
>       ``{collectionName} toolName``
>   For tools that simply wrap or provide an interface to some other tool (**NOTE: this is still uncommon in bioimage analysis and was a particular situation in biotools. It needs more discussion)**, use the pattern 

>``{collectionName} toolName {API|WS}{(providerName)}`` *e.g.* ``EMBOSS water API (ebi)``

>   where:
  
>   * ``collectionName`` is the name of library, main software in which the component is present natively or other collection the underlying tool is from (if applicable).
>   * ``toolName`` is the canonical name of the underlying tool
>   * use ``API`` for Web APIs or ``WS`` for Web services
>   * ``providerName`` is the name of the institute providing the online service (if applicable)

>   If in exceptional cases (*i.e.* when registering, as separate entries, versions of a tool with fundamental differences, substitute for ``toolName`` in the pattern above:
   
> ``toolname versionID`` *e.g.* ``ilastik 0.5``

   where ``versionID`` is the version number.
   
      
>> ** Tip: **
>>   - in case of mulitple related entries be consistent, *e.g.* ``Open PHACTS`` and ``Open PHACTS API``
>>   - be wary of names that are very long (>25 characters). If shortening the name is necessary, don't truncate it in a way (*e.g.* within the middle of a word) that would render it meaningless or unintuitive

## Description 
Textual description of the software, e.g. *"The neuTube is a collection of neuron reconstruction tools from fluorescence microscope images. It has an interactive system with a 3D viewer, which can be clicked in 3D and perform neuron tracing automatically and semi-automatically. It can automatically recognize branching points as junctions. Traced neurons can be exported to swc format, which could be imported by various software packages. neuTube has Win and Mac OS standalone executable builds and may also be installed by manual compilation. In addition, neuTube can be used as a plugin in Vaa3D."*

*example 2: "All-path-pruning 2.0 (APP2) is neuron tracing (fully automated) component of Vaa3D. APP2 prunes an initial reconstruction tree of a neuron’s morphology using a long-segment-first hierarchical procedure instead of the original termini-first-search process in APP. APP2 computes the distance transform of all image voxels directly for a gray-scale image, without the need to binarize the image before invoking the conventional distance transform. APP2 uses a fast-marching algorithm to compute the initial reconstruction trees without pre-computing a large graph. This method allows to trace large images. This method can be used with default parameters or user-defined parameters."*

**1.** **MUST** provide a concise summary of purpose / function of the tool

**2.** **MUST** begin with a capital letter and end with a period ('.') 

**4.** **SHOULD NOT** include any of the following, *unless* essential to distinguish the tool from other entries:

>  - general or technical terms ("software", "application", "plugin" *etc.*) 
>  - provenance information *e.g.* software provider, institute or person name

**5.** **SHOULD NOT** describe how good the software is (mentions of applicability are OK)

**6.** **SHOULD NOT** include URLs

## Author

**1.** Each author item **MUST** correspond to a single individual.

**2.** Each author item **MUST** follow the following pattern:
    ``LastName, FirstName``, where ``LastName`` **MUST NOT** be abbreviated and ``FirstName`` **SHOULD NOT** be abbreviated (usually when the first name is long it is **RECOMMENDED** to use full ``FirstName`` abbreviations or partial abbreviations (*e.g.* ``SCHOLZ, LEANDRO A. (orcid.org/0000-0002-2411-0429)``). 
    
**3.** **SHOULD** (if available) include the author's ORCID ID with the following template: ``LastName, FirstName (orcid.org/xxxx-xxxx-xxxx-xxxx)`` so they can be contacted more easily (to get the Orcid , google orcid + author name to get it. orcid.org/xxxx-xxxx-xxxx-xxxx). 

## Illustrative image 

An illustrative image that represents the main functionality of the software entry.

**1.** It **SHOULD** represent the main software functionality or a screenshot of the UI in use. In cases where a single image cannot show the main functionality of the software entry (usually happens for general purpose software and libraries) the illustrative image **SHOULD** be the logo. 

**NOTE:** The software entry will not be promoted on the front page without an illustrative image.

## License/Openness

There are only 4 discrete values for this attribute: ``Commercial``, ``Free and open source``, ``Free but not open source`` and ``I do not know``. 
 - ``Commercial`` is used when the software needs to be purchased in order to be used. 
  - ``Free and open source`` is selected when the source code is available and the software does not need to be purchased in order to be used``
  - ``Free but not open source`` is used when the source code is not available (closed source) but the software is free to be used. 
  - ``I do not know`` is used when the License/Openness is not know. This value **SHOULD** be avoided. 

**1.** If an entry has two versions with different License/Openness values (*e.g.* a commercial and a free version with fewer features), it **SHOULD** have both values selected.

## Entry curator

## Download page

*Homepage of the software, from which is possible to download the software or some URL that best serves this purpose, e.g. "http://icy.bioimageanalysis.org/"*

**1.** **MUST** resolve to a web page from the developer / provider that most specifically provides a downloadable version of the software or has a link to its source code.

**2.** **MUST** be restricted to ``http(s?)://[^\s/$.?#].[^\s]*``
  
**TIP:** In case a tool lacks its own website, a URL of its code repository is OK. Do not use a general URL such as an institutional homepage, unless nothing better is available.

## Reference publication

**1.** **MUST** resolve to a web page of a journal article or web page of a preprint server that most specifically links to a reference publication.

**2.** **SHOULD** preferably be a DOI link in the form  ``https://doi.org/``+``DOI`` (*e.g.*  ``https://doi.org/10.1371/journal.pbio.1002128``). Normal URL links to the reference publication are OK but discouraged. 

**3.** **SHOULD** preferably resolve to a publication where the tool was first introduced.

