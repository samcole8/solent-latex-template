# SSU LaTeX Template
[![](https://img.shields.io/github/v/release/samcole8/solent-latex-template
)](https://github.com/samcole8/solent-latex-template/releases/latest)
![](https://img.shields.io/badge/status-in_development-orange
)

LaTeX Template for Southampton Solent University reports.

## Why use LaTeX?

Formatting in Microsoft Word (and other document editors) is notoriously painful. LaTeX separates concerns by defining 
the layout as code, meaning you can focus on the content of your work without messing things up.

It can also parse exported references into the document in the Solent-Harvard format, and will work with tools like RefWorks or Zotero.

## Disclaimer

Every effort has been made to ensure that this template accurately produces documents in the required format. However, responsibility lies with the user in the event that it produces incorrectly formatted or corrupted content.

Therefore, it is strongly advised that:

- Document generation is tested at the earliest possible stage (LaTeX can take a long time to install).
- Generated content is tested and proofread prior to submission.

## Usage

### Headings

You can define headings at levels one through four, as follows:

1. `/chapter{chapter name}`
2. `/section{section name}`
3. `/subsection{subsection name}`
4. `/subsubsection{subsubsection name}`

### Paragraphs

Write paragraphs in plaintext, separated by newlines:

```tex
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam auctor diam augue, at fermentum mauris cursus eget.

Fusce mauris dolor, egestas quis molestie ac, semper et libero. Pellentesque varius eros in dui porta suscipit.
```

### Figures

To insert an image, use the following code block:

```tex
\begin{center}

    \includegraphics[width=\linewidth]{your_image}
    \captionof{figure}{Example image}

\end{center}
```

In the example above:

- LaTeX looks for an image called `your_image.png` in the `./images/` folder.
- The figure has the caption "*Example image*".

### Referencing & Citations

#### Supported Sources

Solent-Harvard style requires custom drivers for each type of source. These exist for the following source types:

- Online Sources (`@online`)
- Books (`@book`)
- Conference papers (`@inproceedings`)
- Journal Articles (`@article`)
- Standards & others (`@misc`)

#### References

References go in the `refs.bib` file in BibTeX format. You can generate these with a reference management tool such as RefWorks or Zotero.

References will be automatically formatted and parsed into the document upon creation.

#### Citations

 Use `\cite{id}` anywhere in your document to cite a source.

 When the author name is in the text, use `\citeyear{id}` to exclude the author name from the citation.

### Tables

LaTeX tables guide: https://www.overleaf.com/learn/latex/Tables

### Footnotes

Footnotes guide: https://www.overleaf.com/learn/latex/Footnotes

### Cross-referencing

Cross-referencing guide: https://www.overleaf.com/learn/latex/Cross_referencing_sections%2C_equations_and_floats

## Generating a PDF document

The easiest way to use LaTeX is with [Overleaf](https://www.overleaf.com/)—just import a copy of the template. Alternatively, you can install it locally on Linux or Windows. Below are instructions for local installations.

### Linux & Windows

1. [Install LaTeX](https://www.latex-project.org/get/).
2. To generate `master.pdf`, open a terminal and run the command below:
    ```
    pdflatex master.tex
    ```
3. If you are using BibLaTeX, run `biber` *after* `pdflatex` and then re-run it:

    ```
    biber master && pdflatex master.tex
    ```

## Software license

This template is **software** licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en). This license establishes different rules for **software** and **content**, which are explained in more detail below:

- You *cannot* use the template code itself (**software**) for commercial purposes.
- You *can* use the generated PDF/DOCX document (**content**) for any purpose, including commercial applications, without attribution.
- If you redistribute the template code (**software**), you must attribute the [original source](https://github.com/samcole8/solent-latex-template) and retain the existing license.
