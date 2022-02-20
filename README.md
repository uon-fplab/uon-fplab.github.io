This is the source of the Nottingham FP Lab blog.
The live version is at [uon-fplab.github.io](https://uon-fplab.github.io).

Posts (stored in `_posts`) are written in a combination of Markdown and KaTeX/LaTeX: `$...$` and `\\[...\\]` (note the double backslash) for inline and display math respectively (see also the Krater [readme][2] and [sample page][3] for the basics).

There's also the following extra LaTeX-like functionality:

### Sections and numbering

```
{% section Heading %}
{% subsection Subheading %}
{% subsubsection Subsubheading %}
```
Turn numbering on with
`section-numbers: true`
in front matter (off by default).

### Theorem blocks

```
{% theorem Lévy reflection principle %}
    etc. etc.
{% endtheorem %}
```
generates the appropriate permalinked block and heading.
Optional numbering with `theorem-numbers: true` in front matter (on by default).

Also available are `lemma`, `proposition`, `definition`, `notation`, `remark`.

### Labels

```
{% labeled choose-your-own-reference-name %}
Equation, diagram, etc. goes here
{% endlabeled %}
```
generates the appropriate numbered label.
There's currently no support for custom labels.

### Intra-document references

```
{% ref use-your-chosen-reference-names %}
```
for equation referencing, or
```
{% ref the full heading of a section/theorem block also works (case-insensitive) %}
```
Turning on numbering is suggested with the latter.

### Citations

Uses [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar).
Place Bibtex reference data in `_bibliography/references.bib` and cite with
`{% cite citation-key %}`.

### Todo tags

`{% todo %}` or `{% todo write a note to self %}` for all your shopping list needs.



[1]: https://github.com/paolobrasolin/krater
[2]: https://github.com/paolobrasolin/krater/blob/main/README.md
[3]: https://github.com/paolobrasolin/krater/blob/main/index.md