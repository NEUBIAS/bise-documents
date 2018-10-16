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

------------------

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt>):

- **"MUST"**, **"REQUIRED"** or **"SHALL"** mean that the guideline is an absolute requirement of the specification.
- **"MUST NOT"** or **"SHALL NOT"** mean that the guideline is an absolute prohibition of the specification.
- **"SHOULD"** or **"RECOMMENDED"** mean that there may exist valid reasons in particular circumstances to ignore a particular guideline, but the full implications must be understood and carefully weighed before doing so.
- **"SHOULD NOT"** or the phrase **"NOT RECOMMENDED"** mean that there may exist valid reasons in particular circumstances when acting contrary to the geuideline is acceptable or even useful, but the full implications should be understood and the case carefully weighed before doing so.
- **"MAY** or **"OPTIONAL"** mean that the guideline is truly optional; you can choose to follow it or not.
    
# General guidelines
------------------
## Before you start

Consider the following *before* adding a software entry in BIII.eu

1. **Are one or more entries required to describe the software?**

   - Software with multiple implementations often require multiple entries. Example: SOAX - has 2 different ways of downloading it: One is the windows standalone executable and the second is the source code, which will require one to compile it in any OS (requiring ITK, VTK and Boost C++ libraries). In that case, the best way is to create two entries: one by location of download since it is actually two different software then, and evrey entry should have only one dowload page (has location). In one entry there is only windows as the supported platform, while in the other, any OS. 
   - Collections also often require multiple entries. Example: Simple Neurite Tracer (existing entry) is an ImageJ-Fiji plugin which has three workflow options availabl: 2 semi-automated and 1 fully automated. In this case, one would create one entry for Simple Neurite Tracer (the plugin) as a _Collection_, then one entry by example workflow, and specify the difference in the title. You will have one plugin, and 3 workflows requiring the plugin Simple Neurite Tracer.
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
