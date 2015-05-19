QCAV2015 Breast Article writing in Latex
========================================

What ?
------
look at the damn title. This repo contains the latex for the article.

### Summary Submission requests

Prospective authors must submit an extended summary of approximately 2,000 words (not including references) in English. Summaries must be single column and formatted to fit 8.5 in. x 11 in. page size.

### TODO List 
Each submission should consist of:


```no-highlight
* [ ] Title of paper
* [x] Author listing with principal author first including first and last name, affiliation, mailing address,  and e-mail address
   |  [ ] telephone, facsimile,
* [ ] Preference for oral or poster presentation
* [x] Keywords (up to 5 descriptive words)
* [ ] Summary text (approximately 2000 words)
* [ ] Brief biography of principal author (approximately 50 words)
```

How ?
-----

### Structure
The primary file is called master.tex, and contains the bare essential and the abstract to get an idea of the content at a glance. The content is imported using include and input. Latex packages, acronyms, etc.. are called using input directly meanwhile the chapters (or sections) are called using include. If a chapter source requires from an external file, this is imported using input (in the further included chapter file).

The document structure is as follows
```
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
        content/
    | |   % This folder contains any file related with the content of the 
    | |   % document. Each capter (or section) are stored in separated 
    | |   % folders, which contain a figures subdirectory. Other content
    | |   % refering to the whole document such as frontmatter, acronyms
    | |   % and bibliography can be found directly in this content folder.
    | |
    | ├── acronym_definition.tex
    | ├── frontmatter.tex
    | ├── lit_review.bib
    | │
    | ├── features
    | │   └── features.tex
    | │
    | ├── intro
    | │   ├── figures
    | │   │   │   % folder containing figures
    | │   │   └──
    | │   └── intro.tex
    | │
    | ├── method
    | │   ├── figures
    | │   │   │   % folder containing figures
    | │   │   └──
    | │   └── method.tex
    | │
    | └── results
    |    ├── figures
    |    │   │   % folder containing figures
    |    │   └──
    |    └── results.tex
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
```

### Latex Packages
The cross indicates, that they have a usage example in this template.

* [ ] [biblatex](http://www.ctan.org/pkg/biblatex) using a biber backend
* [x] graphicx
* [x] newclude
* [x] acro using marcos=true, which allow for \myTriger instead of \ac{myTriger}
* [x] hyperref
* [x] cleveref

### Procedure
The master branch should be stay clean. Every conceptual increment (or todo item) should generate an issue. In order to address the issue a branch should be created and worked out. Once the issue is finished the master is checked out and the branch merged. If a issue needs to be reopen the issue is checked out, merged to master and reworked. Consider to open a new issue instead of reopening a previous one when possible.

### LaTeX Copmpilation

* Usual latex run

  ```
  latex master
  biber master
  latex master
  latex master
  ```

* Automated compilation with preview (my choice, using *latexmk* and *xelatex*)

  ```
  latexmk --xelatex -pvc --pdf master.tex
  ```

### Important Note:
Keeping this file updated is important, it can help in further projects.

### Similar Projects:

* https://github.com/asm-products/Dissertate
* https://github.com/bamos/latex-templates

TODO
----
(Stuff to get done, either in the project or the template, that would depend :))

* [ ] Create a better cleveref example
* [ ] Some compilation erros for the nested acronyms
* [ ] Place a snapshot of each template linking to its *branch*
* [ ] Task 1
* [ ] Task 2
