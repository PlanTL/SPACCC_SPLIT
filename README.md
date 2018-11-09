# SPACCC_SPLIT: : Spanish Clinical Case Corpus - Sentence Splitting

## Introduction

This repository contains the sentence splitting annotations in the Spanish Clinical Case Corpus that have been 
carried out by means of the Spanish Clinical Case Corpus Part-of-Specch Tagger based on FreeLing3.1 
(SPACCC_POS-TAGGER, https://github.com/PlanTL/SPACCC_POS-TAGGER).


## Repository structure

<pre>
corpus/
Original, development, validation and automatically annotated corpus, both in tabular format and BRAT 
standoff format.

guidelines/
Annotation guidelines.

IAA/
Inter-annotator agreement report, along with the data and the scripts used to calculate it. 

script/
Script to convert FreeLing3.1 tabular output format into BRAT standoff format.
</pre>


## Document selection

he SPACCC corpus was created after collecting 1,000 clinical cases from SciELO (Scientific Electronic Library Online), 
an electronic library that gathers electronic publications of complete full text articles from scientific journals of 
Latin America, South Africa and Spain (http://www.scielo.org).

A clinician classified those cases into those that were similar to real clinical texts in terms of structure and content
and those that were not suitable for this task. Figure legends were automatically removed and in case multiple clinical 
cases were listed, these were split into single clinical cases.


## Annotation format

Annotations created in SPACCC_SPLIT are provided in BRAT standoff format; i.e. the annotations are stored separately 
(in an `.ann` file) from the document text, which is never modified by the tool. 
These two files are associated by their base name; their file name without suffix is the same: 
`es-S0004-06142005000200009-1.ann` contains the annotations for the file `es-S0004-06142005000200009-1.txt`. 
See http://brat.nlplab.org/standoff.html for further details on the brat standoff format. 

This annotation format is produced by running an script that converts the output of SPACC_POS-TAGGER, a 
CoNLL-like column format where columns are:

* `FORM`: word form.
* `LEMMA`: word lemma.
* `TAG`: complete POS tag.
* `PROBABILITY`: probability of the chosen tag.


## Corpus predictions

|                        | Split  | 
| ---------------------- | ------ |
| A1 vs A2               | 99,79% | 
| A1 vs FL               | 99,37% | 
| A2 vs FL               | 99,58% | 
| Required minimum level | 99%    | 


|                        | Split  | 
| ---------------------- | ------ |
| GS vs FL               | 99,37% | 
| Required minimum level | 99%    | 


See the inter-annotator agreement report (Informe_interagreement_CNIO_PlanTL_SEAD.pdf) included in folder `iaa`in this 
repository for further details.

## Annotation guidelines

The annotation guidelines describe the criteria that have been followed to annotate the corpus, along with illustrative 
examples. They describe FreeLing default resources, the criteria that have been followed in the manual annotation and the 
implementations that solve these criteria in automatic annotation. The guidelines also compare the criteria followed in 
this project with those followed by the Apache CTAKES NLP system (http://ctakes.apache.org/) and the the GENIA Sentence 
Splitter (http://www.nactem.ac.uk/y-matsu/geniass/), as well as the criteria followed in the development of the GENIA corpus (https://github.com/spyysalo/genia-pos).

Guidelines have been written and developed in Spanish and are only available in Spanish.


## Corpus consistency


## Annotation schema


## Contact

Montserrat Marimon (montserrat.marimon@bsc.es)


## License

MIT License

Copyright (c) 2018 Secretaría de Estado para el Avance Digital (SEAD)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
