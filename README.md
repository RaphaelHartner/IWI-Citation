# IWI-Citation
The content of this repository allows you to set up your latex project with the specific Industrial Management (IWI) citation style

## include/input the preamble extension in your original preamble file
\input{chapters/00_preamble_iwi_citation} 

## use your corresponding reference list
\addbibresource{references.bib}

## change your language (main.tex), if necessary
\selectlanguage{english} %citation can be used with german or english

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
