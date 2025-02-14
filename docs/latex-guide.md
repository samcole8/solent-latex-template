# Usage Guide

This section provides guidance on how to use common LaTeX features. For more complex usage, see [Other Elements](#other-elements).

**Table of Contents**

- [Usage Guide](#usage-guide)
  - [1. Headings](#1-headings)
  - [2. Paragraphs](#2-paragraphs)
  - [3. Images](#3-images)
  - [4. Referencing \& Citations](#4-referencing--citations)
    - [4.1. Supported Sources](#41-supported-sources)
    - [4.2. References](#42-references)
    - [4.3. Citations](#43-citations)
  - [5. Code Blocks](#5-code-blocks)
  - [6. List of Definitions \& List of Abbreviations](#6-list-of-definitions--list-of-abbreviations)
  - [7. Other Elements](#7-other-elements)

## 1. Headings

You can define headings at levels one through four, as follows:

1. `/chapter{chapter name}`
2. `/section{section name}`
3. `/subsection{subsection name}`
4. `/subsubsection{subsubsection name}`

## 2. Paragraphs

Write paragraphs in plaintext, separated by newlines:

```tex
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam auctor diam augue, at fermentum mauris cursus eget.

Fusce mauris dolor, egestas quis molestie ac, semper et libero. Pellentesque varius eros in dui porta suscipit.
```

## 3. Images

To insert an image, use the following code block:

```tex
\begin{center}

    \includegraphics[width=\linewidth]{your_image}
    \captionof{figure}{Example image}

\end{center}
```

In the example above:

- LaTeX looks for an image called `your_image.png` in the `./images/` folder.
- The figure has the caption "*Figure X.X: Example image*".

*Note: This repository's `.gitignore` ***ignores*** images by default. If you want to include them in version control, omit  `images/*`.*

## 4. Referencing & Citations

### 4.1. Supported Sources

Solent-Harvard style requires custom drivers for each type of source. These exist for the following source types:

- Online Sources (`@online`)
- Books (`@book`)
- Conference papers (`@inproceedings`)
- Journal Articles (`@article`)
- Standards & others (`@misc`)

### 4.2. References

References go in the `refs.bib` file in BibTeX format. You can generate these with a reference management tool such as RefWorks or Zotero.

References in this file will be automatically formatted and parsed into the document upon creation.

### 4.3. Citations

 Use `\cite{id}` anywhere in your document to cite a source.

 When the author name is in the text, use `\citeyear{id}` to exclude the author name from the citation.

## 5. Code Blocks

The `minted` package can be used to automatically highlight code, but there are some prerequisites if you are doing this locally. For this reason, it is disabled by default, but can be enabled by uncommenting the following lines in `master.tex`:

```latex
% Code
% \usepackage{minted}
```

Then, you will need to set up the `pygments` syntax highlighter. Assuming you have [Python 3](https://www.python.org/) installed, the following commands will do this (depending on your OS).

1. `python3 -m /path/to/venv`
2. `source /path/to/venv/bin/activate`
3. `pip install pygments`

You will need to re-run the second command to activate the virtual environment every time you close the terminal.

Then, you can add `minted` blocks which typically look something like this:

```latex
\begin{listing}[H]
\begin{minted}[linenos,breaklines]{<your_programming_language>}
    <your_code_here>
\end{minted}
\caption{Code caption}\label{listing:custom-label}
\end{listing}
```

Encapsulating it in a `listing` float ensures it receives a Listing caption and appears in the "List of Listings" section, if enabled.

However, there are lots of other options. More information is available on [Overleaf](https://www.overleaf.com/learn/latex/Code_Highlighting_with_minted).

## 6. List of Definitions & List of Abbreviations

You can add hyperlinked entries for both definitions and abbreviations in the document using `\newglossaryentry` for definitions and `\newacronym` for abbreviations.

```
\newglossaryentry{example}{
    name={Example},
    description={Definition of Example}
}

\newacronym{ab1}{AB1}{Abbreviation 1}
```

Reference them using their respective names in the documents:

```
My abbreviation is \gls{ab1}. My example definition is \gls{example}.
```

More information is available on [Overleaf](https://www.overleaf.com/learn/latex/Glossaries).

## 7. Other Elements

The guides listed below explain how to implement some other common typesetting features, courtesy of [Overleaf](https://www.overleaf.com/).

- [Tables](https://www.overleaf.com/learn/latex/Tables)
- [Footnotes](https://www.overleaf.com/learn/latex/Footnotes)
- [Cross-referencing](https://www.overleaf.com/learn/latex/Cross_referencing_sections%2C_equations_and_floats)