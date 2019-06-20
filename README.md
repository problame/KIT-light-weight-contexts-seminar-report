# How to use this template:

Install `latexmk` and a somewhat complete version of the TeXlive distribution.

```
sudo dnf install latexmk texlive-scheme-small
```

Use `latexmk` to run the fix-point process of building the doucment:

```
latexmk -pdf report.tex         # build report.pdf
latexmk -pdf -pvc report.tex    # live-updating
latexmk -C report.tex           # clean
```

## Bibliography

We use BibLaTeX in `literature.bib`.

# External Content / Licensing

The following files were imported into the tree from other templates under unclear licenses:

* `style/*`
