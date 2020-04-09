# IWI-Citation
The content of this repository allows you to set up your latex project with the specific Industrial Management (IWI) citation style

## prerequisites
- must be used with biblatex
- german or english are the only supported languages
- necessary entry fields (.bib file) must be available
- continous foot note numbering via the "chngcntr" package

## include/input the preamble extension in your original preamble file
\input{chapters/00_preamble_iwi_citation} 

## use your corresponding reference list
\addbibresource{references.bib}

## change your language (main.tex), if necessary
\usepackage[english, german]{babel}
\selectlanguage{english} %citation can be used with german or english

## enable continous foot note numbering
\usepackage{chngcntr}

\counterwithout{footnote}{chapter}

## currently supported entry types
- @book -> book
- @incollection -> chapter in book
- @article -> journal paper
- @inprocedings -> conference
- @misc -> website

## examples
- \iwicite[Cf.][pp. 50-60, 234]{Test2016}
- \iwicites[Cf.][pp. 50-60, 234]{Test2016}[Cf.][pp. 50-60, 234]{Batini2006}
- \iwiurlcite[Cf.][]{Anaconda2019}
-	\iwiurlcites[Cf.][]{Anaconda2019}[Cf.][]{Vantara2018}
-	\footnote{[Note] It's a foot note \iwiciteintext[Cf.][p. 60]{Batini2006}.}

## caption (table/figure) examples
- use \footnotemark within the table/figure caption
- after the "table" or "figure" environment, use one of the following alternatives to declare your citation text
  - \iwicaptioncite[Cf.][p. 300, 234]{Feng2018a} for single citation
  - \iwicaptioncites[Cf.][p. 300, 234]{Feng2018a}[Cf.][p. 300, 234]{Feng2018a} for multiple citation
  - \footnotetext{[Note] you can use it even with additional text[Cf.][p. 300, 234]{Feng2018a}}

## known issues/workarounds 
- including both, Lughofer et al. (2017, DOI 10.1109/CCDC.2018.8407931) and Lughofer et al. (2018, DOI 10.1109/CYBConf.2017.7985808), in the reference.bib file leads to some strange behaviors while citing one them
- when using the in-text citation command (single source), one needs do explicitly specify the punctuation afterwards
