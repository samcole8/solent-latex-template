# solent-latex-template

LaTeX Template for Southampton Solent University reports.

## Disclaimer

Every effort has been made to ensure that this template accurately produces documents in the required format. However, responsibility lies with the user in the event that it produces incorrectly formatted or corrupted content.

Therefore, it is strongly advised that:

- Document generation is tested at the earliest possible stage (LaTeX can take a long time to install).
- Generated content is tested and proofread prior to submission.

## Usage

### Headings

You can define headings up to level four as follows:

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

Solent-Harvard style requires custom drivers for each type of source. Currently, partial support has been added for the following source types:

- Online (`@online`)
- Book (`@book`)

The source types listed below are work-in-progress, partially complete, and may not work as expected.

- Academic journals (`@article`)
- Conference papers (`@inproceedings`)
- Standards (`@techreport`)

#### References

References go in the `refs.bib` file in BibTeX format. You can generate these with a reference management tool such as RefWorks or Zotero.

These references will be automatically formatted and parsed into the document upon creation.

#### Citations

 Use `\cite{id}` anywhere in your document to cite a source. Citations are currently work-in-progress, but you should be able to generate semi-compliant results.

## Generating a PDF document

First, [install LaTeX](https://www.latex-project.org/get/). Then, refer to the OS-specific instructions below.

### Linux

To generate `master.pdf`, open a terminal and run the command below:

```
pdflatex master.tex
```

If you are using BibLaTeX, run `biber` *after* `pdflatex` and then re-run it:

```
biber master && pdflatex master.tex
```

### Windows

Instructions coming soon.

### MacOS

Instructions coming soon.

## Software license

This template is **software** licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en). This license establishes different rules for **software** and **content**, which are explained in more detail below:

- You *cannot* use the template code itself (**software**) for commercial purposes.
- You *can* use the generated PDF/DOCX document (**content**) for any purpose, including commercial applications, without attribution.
- If you redistribute the template code (**software**), you must attribute the [original source](https://github.com/samcole8/solent-latex-template) and retain the existing license.