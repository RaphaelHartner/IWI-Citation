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
