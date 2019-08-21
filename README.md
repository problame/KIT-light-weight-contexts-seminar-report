My seminar report on [Light-Weight Contexts](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/litton):

> We introduce a new OS abstraction—light-weight contexts (lwCs)—that provides independent units of protection, privilege, and execution state within a process. A process may include several lwCs, each with possibly different views of memory, file descriptors, and access capabilities. lwCs can be used to efficiently implement roll-back (process can return to a prior recorded state), isolated address spaces (lwCs within the process may have different views of memory, e.g., isolating sensitive data from network-facing components or isolating different user sessions), and privilege separation (in-process reference monitors can arbitrate and control access).

> lwCs can be implemented efficiently: the overhead of a lwC is proportional to the amount of memory exclusive to the lwC; switching lwCs is quicker than switching kernel threads within the same process. We describe the lwC abstraction and API, and an implementation of lwCs within the FreeBSD 11.0 kernel. Finally, we present an evaluation of common usage patterns, including fast rollback, session isolation, sensitive data isolation, and inprocess reference monitoring, using Apache, nginx, PHP, and OpenSSL.

LaTeX template: https://github.com/problame/KIT-seminar-report-template

---

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
