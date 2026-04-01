# Stevens Institute of Technology Beamer Presentation Template

[![LaTeX](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/)
[![Beamer](https://img.shields.io/badge/Theme-Moloch-A32638.svg)](#)
[![Stevens](https://img.shields.io/badge/Stevens%20Institute-of%20Technology-A32638.svg)](https://www.stevens.edu/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A clean, professional **Beamer presentation template** in official **Stevens Institute of Technology** branding. Built on the [Moloch](https://github.com/jolists/moloch) theme with Stevens red color scheme, custom section outlines, contribution blocks, and a polished title page.

<p align="center">
  <img src="assets/stevens-long-logo.png" alt="Stevens Logo" width="300"/>
</p>

---

## Features

- **Stevens-branded color scheme** -- Stevens red (#A32638) across frame titles, progress bars, blocks, and links
- **Moloch theme** -- minimal, information-dense slides with footer progress bar
- **Custom title page** with Stevens logo and red accent rule
- **Automatic section outline pages** highlighting the current section
- **Three custom block types** -- `colorblock`, `contribblock`, and standard Beamer blocks styled in Stevens colors
- **Modular section files** -- each section lives in its own `.tex` file under `sections/`
- **pdfpc toggle** -- enable/disable presenter console notes with a single flag
- **Check/cross marks** -- `\cmark` and `\xmark` commands for comparison tables
- **Overlay support** -- progressive reveal examples included

## Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/guanqun-yang/StevensTechBeamerPresentationTemplate.git
   cd StevensTechBeamerPresentationTemplate
   ```

2. **Edit your content**
   - Open `main.tex` and update `\title`, `\author`, `\course`, `\institute`, and `\date`
   - Edit (or replace) the section files in `sections/`

3. **Compile**
   ```bash
   pdflatex main.tex
   pdflatex main.tex   # run twice for correct page numbers and outlines
   ```
   Or use your preferred LaTeX editor (Overleaf, Texifier, TeXShop, VS Code + LaTeX Workshop).

## Project Structure

```
.
├── main.tex                  # Main document -- preamble, theme config, metadata
├── sections/
│   ├── 001-introduction.tex  # Section 1: columns, overlays, contribution blocks
│   ├── 002-methods.tex       # Section 2: tables, block types, math
│   ├── 003-results.tex       # Section 3: result tables, ablations, summary
│   └── 004-conclusion.tex    # Section 4: summary table, standout closing
├── assets/
│   ├── stevens-long-logo.png # Stevens logo for title page
│   ├── logo_RGB.png          # Stevens logo for section outlines
│   ├── beamerthememoloch.sty  # Moloch theme files
│   ├── beamerthemesintef.sty  # SINTEF base theme
│   ├── sintefcolor.sty       # Color definitions
│   ├── pdfpc.sty             # pdfpc presenter console support
│   └── ...                   # Other Beamer theme .sty files
└── README.md
```

## Customization

### Section Names

Update the section short/full names near line 205 of `main.tex`:

```latex
\newcommand{\secnameI}{Introduction}
\newcommand{\secfullI}{Background and Motivation}
```

### Colors

All Stevens colors are defined in `main.tex` and can be overridden. The primary accent is `stevensred` (RGB 163, 38, 56).

### Adding Sections

1. Create a new file in `sections/`, e.g., `005-appendix.tex`
2. Add a `\section` and `\input` line in `main.tex`
3. Add corresponding `\secnameV` / `\secfullV` commands and an `\outlineitem` entry

### pdfpc Presenter Notes

Toggle in the preamble of `main.tex`:

```latex
\usepdfpctrue   % Enable pdfpc presenter console
\usepdfpcfalse  % Disable (default, for Texifier/Overleaf)
```

## Requirements

- A LaTeX distribution with Beamer support (TeX Live, MiKTeX, or MacTeX)
- No external package installation needed -- all theme `.sty` files are bundled in `assets/`

## Contributing

Contributions are welcome! Feel free to open an issue or pull request for bug fixes, new slide examples, or additional color themes.

## License

This template is provided under the [MIT License](LICENSE). The Stevens Institute of Technology logo and branding are the property of Stevens Institute of Technology.
