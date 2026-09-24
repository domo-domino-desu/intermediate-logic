# Intermediate Logic

This fork uses the Chinese translation of the Open Logic Text as the
`OpenLogic` submodule. Clone it with all nested assets:

```sh
git clone --recurse-submodules https://github.com/domo-domino-desu/intermediate-logic.git
```

To pick up a newer Open Logic translation, update and commit the submodule
pointer:

```sh
git submodule update --remote --recursive OpenLogic
git add OpenLogic
```

The Chinese edition needs LuaLaTeX (the text is typeset with `ctex` and
New Computer Modern), so build it with `make`, which runs
`latexmk -lualatex`, rather than with `pdflatex`. Every push to
`master` builds `il-screen.pdf`, `il-print.pdf` and
`il-print-cover.pdf` in GitHub Actions and attaches them to a
[release](https://github.com/domo-domino-desu/intermediate-logic/releases).

![Book Cover](https://builds.openlogicproject.org/courses/intermediate-logic/il.png)

Textbook on basic set theory, first-order logic, and Gödel's
incompleteness theorems, developed for McGill's Intermediate Logic
course, based on the Open Logic Project.

Download the [PDF here](https://builds.openlogicproject.org/courses/intermediate-logic/il-screen.pdf).

This repository/directory only contains the LaTeX files and
illustrations needed to typeset the textbook _Intermediate logic_,
which in turn requires the _[Open Logic
Text](https://github.com/OpenLogicProject/OpenLogic/)_.

To install and compile:

- Download/install the _Open Logic Text_ from
  [GitHub](https://github.com/OpenLogicProject/OpenLogic/), including
  [photos](https://github.com/OpenLogicProject/photos) if you want those.
- Navigate to the subdirectory `courses/`
- Put the content of this repository into a subdirectory of it, say
  `courses/intermediate-logic`.

If you use `git`, this should do it:
```
# git clone https://github.com/OpenLogicProject/OpenLogic.git
# cd OpenLogic/courses
# git clone https://github.com/rzach/intermediate-logic.git
# cd ../assets
# git clone https://github.com/OpenLogicProject/portraits.git
# git clone https://github.com/OpenLogicProject/photos.git
```
Inside `courses/intermediate-logic`, you can now compile:
```
# pdflatex il-screen
```
or just `# make` if you have `latexmk` installed. (You'll also have to
do `bibtex il-screen` for the bibliography.)

The file `il-screen.tex` produces a color version of the text with
smaller margins for screen reading. `il-print` produces a
black-and-white version designed for printing on Crown Quarto stock
(without cover).

The file loads `ic.tex`, which contains the actual material. It
in turn includes other files, most of them from the `OpenLogic`
repository. So you won't get a complete book unless you download into
the right subdirectory of and compile from there.

[![Creative Commons License](https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png)](https://creativecommons.org/licenses/by/4.0/) 

_[Intermediate Logic](https://builds.openlogicproject.org/courses/intermediate-logic/)_ by [Richard
Zach](https://richardzach.org/) is licensed under a [Creative Commons
Attribution 4.0 International
License](https://creativecommons.org/licenses/by/4.0/).
