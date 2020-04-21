# SENTiVENT Economic Event Annotation Guidelines
Annotation Guidelines for economic Events in the SENTiVENT project for economic news text mining.

The goal of this annotation scheme is to produce a gold-standard labeled dataset for enabling supervised event extraction in the company-specific news text domain.
The guidelines are based on the [Rich-ERE Guidelines][1] for [Events][2] and [Argument Fillers][3] but adapted to a corpus of business and financial news articles.
We exclusively annotate event structures, unlike Rich ERE which annotates Entities and Relations separately.

Version 1.1. of these Guidelines were used for SENTiVENT English Event 1.0 dataset release.

## Contents
This repository contains the original LaTeX files as well as the report in .pdf.

This Technical Report contains the Annotation Guidelines are described in detail.
Rationale is also given for the event taxonomy as well insights in the iterative annotation process.

1. Introduction: discusses the motivation behind the SENTiVENT project (sec. 1.1), as well as the annotator workflow (sec. 1.2), annotator training and annotation tools used (sec. 1.3.)
2. Terminology and Typography: explains basic concepts and Terminology.
3. Event Trigger and Type: defines event triggers and their attributes, rules for annotating event triggers and how they are realized.
4. Event Arguments: defines event arguments and specifies rules for annotation.
5. Event Coreference: specifies the annotation of event coreference.
6. Event Typology: describes the event typology/taxonomy. Describes event types and subtypes in detail with examples and potential sources of confusion.
7. Guidelines Improvement Plan: Describes issues encountered during annotation and mitigations for future refence. Guidelines were frozen for annotation at v1.0., this section was added in v1.1.
8. Bibliography

## References
[1]: Linguistic Data Consortium. (2016). Rich ERE Annotation Guidelines Overview V4.2, 1–14. Retrieved from http://www.nist.gov/tac/2016/KBP/guidelines/summary_rich_ere_v4.2.pdf on September 2018

[2]: Linguistic Data Consortium. (2015). DEFT Rich ERE Annotation Guidelines: Events V3.0, 1–14.

[3]: Linguistic Data Consortium. (2015). DEFT Rich ERE Annotation Guidelines: Argument Filler V2.3, 1–14.

## LaTeX Compilation
XeLaTeX engine recommended, LuaLatex and pdfLatex produce errors on Overleaf.com editor.

## Author contact
- Gilles Jacobs: GillesM.Jacobs@ugent.be, gilles@jacobsgill.es, gillesjacobs@pm.me
- Veronique Hoste: Veronique.Hoste@ugent.be

## Mirrors
This Technical Report is stored and mirrored in the following locations:
- Primary source: https://github.com/GillesJ/sentivent-event-annotation-guidelines (@commit:eb44075a329996691ea9c657c90b6f2a18bf9c87 on date of publication.)
- Mirror: osf.io/xqzw5

## How to cite
```
@techreport{jacobs2020sentiventeventguidelines,
    author = {{Gilles Jacobs}},
    title = {{SENTiVENT Event Annotation Guidelines v1.1}},
    year = {2020},
    month = {1},
    publisher = {{Language and Translation Technology Team, Ghent University}},
    url = {{https://osf.io/xqzw5}},
    pages = {69},
    doi = {10.17605/OSF.IO/XQZW5}
}
```