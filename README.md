
QCAV2015 Breast Article writing in Latex
==============

# What
--------------
look at the damn title. This repo contains the latex for the article.

## Summary Submission requests

Prospective authors must submit an extended summary of approximately 2,000 words (not including references) in English. Summaries must be single column and formatted to fit 8.5 in. x 11 in. page size.

# TODO List 
--------------------
Each submission should consist of:


```no-highlight
* [ ] Title of paper
* [ ] Author listing with principal author first including first and last name, affiliation, mailing address, telephone, facsimile, and e-mail address
* [ ] Preference for oral or poster presentation
* [x] Keywords (up to 5 descriptive words)
* [ ] Summary text (approximately 2000 words)
* [ ] Brief biography of principal author (approximately 50 words)
```

# How
--------------

## Structure
The primary file is called master.tex, and contains the bare essential and the abstract to get an idea of the content at a glance. The content is imported using include and input. Latex packages, acronyms, etc.. are called using input directly meanwhile the chapters (or sections) are called using include. If a chapter source requires from an external file, this is imported using input (in the further included chapter file).

The document structure is as follows

    .
    |____.gitattributes       % indicates git how to treat pdf and latex files
    |____.gitignore           % indicates git which files to ignore
    |____.git
    | |__ % Contains all the info regarding the repository
    |    
    |____master.pdf           % document output
    |____master.tex           % document source
    |____README.md            % this document you are reading.
    |
    |____content
    | |   % This folder contains any file related with the content of the 
    | |   % document. Each capter (or section) are stored in separated 
    | |   % folders, which contain a figures subdirectory. Other content
    | |   % refering to the whole document such as frontmatter, acronyms
    | |   % and bibliography can be found directly in this content folder.
    | |
    | |____acronym_definition.tex
    | |____frontmatter.tex
    | |____literature_review.bib
    | |
    | |____intro
    | | |____intro.tex
    | |____other
    | | |____figures
    | | | |____mcr3b.eps
    | | |____other_content.tex
    |
    |____latex
    | |   % This folder contains all the files regarding the behaviour of
    | |   % the document. Filesystem contains packages, styles, etc..
    | |   % If fonts or other resources are needed they must be found here
    | |
    | |____filesystem
    | | |____package.tex
    | | |____fileSetup.tex
    | |____fonts
    |

## Procedure
The master branch should be stay clean. Every conceptual increment (or todo item) should generate an issue. In order to address the issue a branch should be created and worked out. Once the issue is finished the master is checked out and the branch merged. If a issue needs to be reopen the issue is checked out, merged to master and reworked. Consider to open a new issue instead of reopening a previous one when possible.

# Important Note:
--------------
Keeping this file updated is important, it can help in further projects.

