# LaTeX Formatting Guidelines for Kerja Praktik Report

- **Compilation Engine:** pdflatex with latexmk.
- **Language Setup:** Use `\usepackage[provide=*]{babel}` and `\babelprovide[main,import]{indonesian}`.
- **Captions & Labels:**
  - Figure captions below the figure: `\captionsetup[figure]{position=bottom}`.
  - Table captions above the table: `\captionsetup[table]{position=top}`.
- **Foreign Words:** Always italicize English/technical terminology (e.g. `\textit{Account Receivable}`, `\textit{Save as Draft}`, `\textit{Revision Flow}`).
- **Paragraph Spacing:** Maintain spacing and indentation settings specified in `main.tex`.
