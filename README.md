# Hierarchical Event Descriptors (HED)
HED is an evolving framework for the description and formal annotation of events 
identified in time series data. The HED ecosystem includes a structured vocabulary
together with tools for validation and for using HED annotations in data search, 
extraction, and analysis. While HED can be used to annotate any type of event, 
the current HED community focuses on annotation of events in human 
electrophysiological and behavioral data such as EEG, MEG, iEEG, eye-tracking, 
motion-capture, EKG, and audiovisual recording.
 
## HED schema
_HED schema_ is the structured vocabulary from which HED annotations base on. HED annotations consist of comma-separated path strings,
selected from the schema. In the newest versions of HED,
all individual nodes in the vocabulary are unique, so users can annotate
by simply giving the last node in the path string rather than the entire path
string: *Red* instead of *Attribute/Sensory/Visual/Color/CSS-color/Red-color/Red*.

This repository contains the HED schema specification, where discussions on schema terms and syntax are held via Github issue mechanism and where HED-supporting tools can find machine-readable format of the schema. The HED schema is available in MediaWiki and XML. The MediaWiki markdown format, stored in [`hedwiki`](https://github.com/hed-standard/hed-specification/tree/directory-reorg/hedwiki),
allows vocabulary developers to view and edit the vocabulary tree using a human-readable markdown 
language available in Wikis and on GitHub repositories. In addition, an expandable non-editable HTML viewer is available
to help users explore the vocabulary.

All analysis and validation tools operate on an XML translation of the vocabulary 
markdown document, stored in [`hedxml`](https://github.com/hed-standard/hed-specification/tree/directory-reorg/hedxml). 

## Viewing and using HED schema
The current generation of HED infrastructure is referred to as HED-3G 
(HED third generation). HED-3G schema is under beta release (HED8.0.0-beta.1), and the
<b>official release of HED-3G schema (HED8.0.0) is planned for July 15.</b> Users are
strongly recommended to use the latest version of the HED schema in doing their annotations.  

To become acquainted with the HED vocabulary, open the [**expandable view of HED**](http://www.hedtags.org/display_hed.html?version=8.0.0-beta.1).
The current version of the HED specification document is available as: 
 
> [HED-3G Hierarchical Event Descriptors specification-version beta.1](https://docs.google.com/document/d/1yGeGO6hpWmZYc8M_jyDyQ5clNhQRtV4i0wKx_12UJTI/view?usp=sharing). 

The following white papers give an overview of HED and how it is used.

> Robbins, K., Truong, D., Jones, A., Callanan, I., & Makeig, S. (2020, August 1).  
> Building FAIR functionality: Annotating event-related imaging data using Hierarchical Event Descriptors (HED).  
> https://doi.org/10.31219/osf.io/5fg73

> Robbins, K., Truong, D., Appelhoff, S., Delorme, A., & Makeig, S. (2021, May 7). 
> Capturing the nature of events and event context using Hierarchical Event Descriptors (HED). 
> BioRxiv, 2021.05.06.442841. 
> https://doi.org/10.1101/2021.05.06.442841

### HED-3G vocabulary views
The latest version of the redesigned HED vocabulary is 8.0.0-beta.1. This is a pre-release version 
pending community comments:

> [**Expandable html view of HED8.0.0-beta.1**](http://www.hedtags.org/display_hed.html?version=8.0.0-beta.1) 

> [**Readable mediawiki view of HED8.0.0-beta.1**](https://github.com/hed-standard/hed-specification/blob/master/hedwiki/HED-generation3-schema-8.0.0-beta.1.mediawiki) 

> [**XML view of HED8.0.0-beta.1**](https://github.com/hed-standard/hed-specification/blob/master/hedxml/HED8.0.0-beta.1.xml)  

An experimental pre-release is available in the hedxml-test directory
> [**HTML view of HED8.0.0-beta.2**](https://www.hedtags.org/display_hed_test.html?version=8.0.0-beta.2)  
> Note: this version is in the new XML format and has not officially been moved to the hedxml directory. The XML is in the hedxml-test directory.

### HED-2G vocabulary views

The latest version of HED-2G is 7.2.0:
> [**Expandable html view of HED7.2.0**](https://www.hedtags.org/display_hed.html?version=7.2.0)  

> [**Readable mediawiki view of HED7.2.0**](https://github.com/hed-standard/hed-specification/blob/master/hedwiki/HED-generation2-schema-7.2.0.mediawiki)

> [**XML view of HED7.2.0**](https://github.com/hed-standard/hed-specification/blob/master/hedxml/HED7.2.0.xml)  


## HED generations and schema versions 
The HED system has gone through two major restructurings since the original system
(HED-1G) was introduced. The following table shows the correspondence between 
HED version number and the design generation.

| version | release date | HED generation |
| --- | --- | --- |
| 1.0 | 2011-01-01 | HED-1G |
| 4.0.0 | 2016-02-25 | HED-2G |
| 8.0.0 | 2021-07-15? | HED-3G |

_? = release date tentative_

HED-1G introduced the basic ideas of annotation using path strings and is
still in use in the [HEADIT archive](https://headit.ucsd.edu). 

A major redesign of HED, HED-2G released in 2016 (4.0.0 <= HED version < 8.0.0), 
orthongonalized the vocabularly terms and introduced parentheses for grouping modifiers
with the terms they modify, resulting in much improved annotation. 

The second majoring restructuring, HED-3G (7.x.x < HED version), 
has resulted in a dramatic improvement in capabilities, including the 
introduction of annotations of condition variables and experimental 
design within the data as well as the ability to handle event context 
and events with temporal extent.
 

## Further documentation

The documentation on this page refers specifically to the HED vocabulary and supporting tools. Additional documentataion is available on:

> [**HED organization website**](https://www.hedtags.org)

All of the HED software is open-source and organized into various repositories on the HED standards organization website:

> [**HED organization github repository**](https://github.com/hed-standard)

### HED-3G document mapping to defined terms in existing ontologies

The following working document describes the origin of the descriptions associated with individual nodes in the HED-3G hierarchy. Many terms appear in the NCIT ontology (National Cancer Institute Thesaurus OBO edition).

> [**Google doc with mapping of HED-3G term descriptions to existing ontology terms**](https://drive.google.com/file/d/13y17OwwNBlHdhB7hguSmOBdxn0Uk4hsI/view?usp=sharing) 

## Tools to help with HED annotations
The GUI tool [_CTagger_](https://github.com/hed-standard/CTagger) is available to help users with the annotation process. CTagger can be used as a standalone application or can be called from EEGLAB via the [hedtools plug-in](https://github.com/hed-standard/hed-matlab) to annotate an EEGLAB dataset/STUDY directly. Please refer to the linked repositories for more documentation on how to start HED-tagging using CTagger.

## Web-based HED tools

The current web-based HED tools include an online validator of spreadsheets (Excel or tsv)
containing HED tags. Schema tools are available for converting HED schema specifications between `.mediawiki` and
`.xml` formats. Also available is a tool for checking for duplicate nodes in schema and for converting
HED annotations between short and long forms.  

The current web-based HED tools are located at [https://hedtags.ucsd.edu/hed](https://hedtags.ucsd.edu/hed).  

The tools can be run locally using the `runserver.py` function the hedweb module
of the [hed-python](https://github.com/hed-standard/hed-python) repository of 
[hed-standard](https://github.com/hed-standard).

## Stable links for HED validation

> [**Stable directory link for software requiring a HED schema for validation**](https://github.com/hed-standard/hed-specification/tree/master/hedxml)

> [**Stable  link for the latest version of the HED-generation2 schema**](https://raw.githubusercontent.com/hed-standard/hed-specification/master/hedxml/HEDLatest.xml)


## HED-3G library schema

HED-3G supports library schema, which are specialized vocabularies used in conjunction with the
base vocabulary to support annotation of specialized datasets. Communities may develop and submit
library schema.  HED library schema are hosted on the repository: 
[https://github.com/hed-standard/hed-schema-library](https://github.com/hed-standard/hed-schema-library)
