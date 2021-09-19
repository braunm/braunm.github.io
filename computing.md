---
layout: page
title: Computing
permalink: /computing/
---

I am the author of four packages for the R statistical programming language.  I also have a library of code snippets for R, emacs, and LaTeX that I will post from time to time, as I clean them up for public review.

## R packages

- [trustOptim](https://cran.r-project.org/package=trustOptim)

- [sparseHessianFD](https://cran.r-project.org/package=sparseHessianFD)

- [sparseMVN](https://cran.r-project.org/package=sparseMVN)

- bayesGDS (not currently maintained)

## My computing setup


* I write _everything_ in Emacs: code, reviews, manuscripts, lecture slides, and even recommendation letters.  Specifically, I use [Aquamacs Emacs](http://aquamacs.org), an emacs port for MacOS.  GNU Emacs has been around since 1985, so it is just plain __solid__, with a huge user base for support, and thousands of packages and modes that can do anything from syntax highlighting of your favorite programming language (`ess-r-mode`) to psychotherapy (`doctor`).  By using the same program for ever a fully-featured platform, I can use the same program (and thus, the same keybindings) for everything I do.

Emacs is easy to use.  If you do not know Lisp,  **configuring** Emacs can be hard.  Someday I will post my configuration file, which has evolved quite a bit over the last decade.

* For statistical computing, I code in the [R language](https://www.r-project.org), using Emacs with the  [ESS](https://ess.r-project.org)  package (__E__ macs __S__ peaks __S__ tatistics). ESS let's me have both my R source document and an active R session open at the same time, in the same Emacs session. It saves a lot of time to be able to send a chunk of source code directly into R with two keystrokes.

* Writing papers:  I write my research papers directly in Emacs, marked up with [LaTeX](www.latex-project.org). The [AuCTeX](https://www.gnu.org/software/auctex/) Emacs package provides lots of time-saving functions, macros, and keymaps that have become so automatic to me that I can just focus on the writing.
  - I compile my LaTeX documents with [LuaTeX](www.luatex.org) (instead of pdfTeX) for a few reasons:
	- With [fontspec](https://github.com/wspr/fontspec) and [unicode-math](https://github.com/wspr/unicode-math), I can create documents using any installed font, rather than being limited to fonts provided in LaTeX packages.
	- Sometimes there is a need to run calculations as part of the document, such as when drawing figures using tikZ.
	- Some LaTeX packages require LuaTeX.  An example is lua-check-hyphen, which generates a list of all hyphenated words in the document, so I can confirm that they are hyphenated at the right places.
   - The [preview-latex](https://www.gnu.org/software/auctex/manual/preview-latex.htmlpackage) (now included in AuCTeX) embeds compiled chunks of rendered LaTeX (e.g., math symbols and equations) directly in the emacs frame. That way I can see the all of the content -- text and math -- together in the same frame I am writing in, without having to glance to the output pdf.
   - Reference management:  I use [biber](http://biblatex-biber.sourceforge.net) and  [biblatex](https://ctan.org/pkg/biblatex?lang=en) to insert citations and create bibliographies. Biblatex is designed to be more flexible and customizable than bibtex,  but my references are stored in bibtex format. My bibtex database (which I maintain using [BibDesk](https://bibdesk.sourceforge.io) contains 1,800 references (and in most cases, pdfs) of academic papers I have downloaded, read, intend to read, intended to read, or otherwise needed for some reason, collected since I was a graduate student.

* I built this website with [Jekyll](https://www.jekyllrb.com), mainly for blig management. The HTML includes Bootstrap 5 classes.  As with everything else, I wrote both the site code (`web-mode`) and text content (`markdown-mode`) in Emacs.
