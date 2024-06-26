# solent-latex-template
Template project for Solent style reports with LaTeX.

## Usage

### Headings

You can define headings up to level four as follows:

1. `/chapter{chapter name}`
2. `/section{section name}`
3. `/subsection{subsection name}`
4. `/subsubsection{subsubsection name}`

### Paragraphs

Paragraphs can be written in plaintext, separated by newlines:

```tex
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam auctor diam augue, at fermentum mauris cursus eget.

Fusce mauris dolor, egestas quis molestie ac, semper et libero. Pellentesque varius eros in dui porta suscipit.
```

### Figures

To insert an image, you can use the following:

```tex
\begin{center}

    \includegraphics[width=\linewidth]{your_image}
    \captionof{figure}{Example image}

\end{center}
```

In the example above:

- LaTeX looks for an image called your_image.png in the ./images/ folder
- The figure has the caption *Example image*

### Tables

### Referencing

Referencing is WIP. Solent has a CSL style but no BibLaTex support (.bbx and .cbx). Therefore I have to make them myself, and I don't have time right now!

### Cross-referencing

#### Figures

#### Headings

#### Tables