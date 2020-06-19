# decoders-group-project-workbook-template
Decoders Group (Audio) Project Workbook Template

- Provides easy Markdown template for gathering project requirements
- Provide a text file for project requirements that can be versioned (e.g. with Git or Perforce)
- Convert to LaTeX-generated PDF using the following:

```
pandoc PROJECT_WORKBOOK_TEMPLATE.md --latex-engine=xelatex  -V geometry:margin=1.5in --toc -N -s -o example.pdf
```
