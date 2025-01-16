# Generating a PDF document

The easiest way to use LaTeX is with [Overleaf](https://www.overleaf.com/)—just import a copy of the template.

Alternatively, you can install it locally on Linux or Windows. Below are instructions for local installations.

If you want to use VS Code, check out the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension.

## Linux & Windows

1. [Install LaTeX](https://www.latex-project.org/get/).
2. To generate `master.pdf`, open a terminal and run the command below:
    ```
    pdflatex master.tex
    ```
3. If you are using BibLaTeX, run `biber` *after* `pdflatex` and then re-run it:

    ```
    biber master && pdflatex master.tex
    ```