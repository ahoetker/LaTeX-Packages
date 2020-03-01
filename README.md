# LaTeX-Packages
My most commonly used preambles, packaged as .sty files.


# Rationale
I do essentially all of my schoolwork in LaTeX, and I have a set of common preambles I really like. In order to follow the advice given in https://www.overleaf.com/learn/latex/Management_in_a_large_project#Preamble_in_a_separate_file, I have created `.sty` package files from my favorite preambles. 

# Usage

Simply pick a style and use it like any other package. I recommend using this package towards the very top of your preamble, so that any changes below will override my defaults:

```latex
\documentclass[12pt,letterpaper]{article}
\usepackage{chehomework}
 
% Document-specific information
\title{Really Cool Chemical Engineering Homework}
\author{Andrew Hoetker}
\addbibresource{sources.bib}

% Packages that need to be loaded last
\usepackage{subfiles}

\begin{document}
    ...
\end{document}
```

See the [examples](/examples) folder for example documents.

# Requirements

A LaTeX installation is required to do anything useful with these. I use and recommend [TeX Live](https://tug.org/texlive/), which is distributed for Linux, macOS, and Windows. 

## LuaTeX and other TeX Engines

I use [LuaTeX](https://www.overleaf.com/learn/latex/Articles/An_Introduction_to_LuaTeX_(Part_1):_What_is_it%E2%80%94and_what_makes_it_so_different%3F) for all my typesetting needs. In case that is not an option for you, these packages will still compile under pdfLaTeX, thanks to the strategic use of [ifluatex.sty](https://www.ctan.org/pkg/ifluatex). 

## Fonts

If the document is built with LuaTeX, the [STIX](https://github.com/stipub/stixfonts) OpenType Unicode fonts will be used. If these fonts are not installed as part of your LaTeX distribution, please install them system-wide. 