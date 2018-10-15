Guidelines to BIII.eu curators
==============================
BIII.eu is a web-based database that includes bioimage analysis tools, such as Software, Training material and Datasets. The guidelines here presented will help confirmed taggers add and curate _software_ entries into BIII.eu only. The software entry of the webtool include from simple _components_, such as a gaussian filter, to image processing libraries (_collections_ of components) and _workflows_ (e.g. single particle tracking workflows). 

The detailed description of the types of tools that can be included in BIII.eu webtool are still under discussion. However, we ask curators and taggers to include only tools that can be used and relate to image analysis problems in biology (a.k.a bioimage analysis). 

The tools are described using two ontologies, [**BISE-core-ontology**](https://github.com/NeuBIAS/bise-core-ontology) and [**EDAM-Bioimaging**](https://github.com/edamontology/edam-bioimaging). **BISE-core-ontology** contains the structure of description of entries in BIII.eu, not only software, and includes entry properties such as author, reference publication, curator and so on. **EDAM-Bioimaging** is used as a source of terms to describe the entry with Bioimaging related vocabulary.  

>In BISE, a software entry describes a bioimage analysis tool, which can be classified as a _component_, a _collection_ or a _workflow_. A _component_ is an implementation of certain image processing / analysis algorithms. Each component alone does not solve a Bioimage Analysis problem. These problems can be addressed by combining such components into workflows. On the orhter hand, a _workflow_ is a set of components assembled in some specific order to process bioimages and estimate some numerical parameters relevant to the biological system under study. Workflows take image data as input and output either processed images or other type of data (usually numeric values). Workflows can be a combination of components from the same or different software packages. Finally, a _collection_ is a software that encapsulate a set of bioimage components and/or workflows, e.g. libraries such as **imglib2** and **scikit-image** or general purpose software such as **Fiji**, **Icy**.

# How and what to curate? 

When you add a new content, you will notice that a similar named tools exist. Please check if it is the same tool(s) you wanted to tag, if not, name it differently (example: Erosion (Icy) vs Erosion (MorpholibJ)). The purpose is to have a unique title for each entry. Whenever possible, try to add both the _collection_ and an entry by _component_(s): e.g. MorpholibJ is an ImageJ plugin, and an entry by function (erosion in MorpholibJ, watershed in MorpholibJ etc... are all components inside MorpholibJ). The purpose is then to help analysts to find the component they need when constructing a bio image analysis workflow.

Try to fill as many fields as possible. If one field definition is unclear, report in the [BIII.eu forum](http://biii.eu/forum) or raise an issue in github [bise documents repository](https://github.com/NeuBIAS/bise-documents).

