# PROJECT KNOWLEDGE BASE

**Generated:** 2026-02-01
**GitHub:** FrankieeW/GroupAction-PDF
**Author:** Frankie F.-C. Wang

## OVERVIEW

PDF output aggregator for GroupAction project. Consolidates Lean formalization results, LaTeX report, and Beamer slides into final PDF deliverables.

## STRUCTURE

```
PDF/
├── merged/             # Merged PDF output
├── report/             # Report PDF output
├── slides/             # Slides PDF output
├── lean-results/       # Lean formalization exports
└── README.md           # Build instructions
```

## WHERE TO LOOK

| Task | Location | Notes |
|------|----------|-------|
| Final PDF | `merged/` | Combined output |
| Report PDF | `report/` | Report output |
| Slides PDF | `slides/` | Slides output |
| Lean exports | `lean-results/` | Formalization PDFs |

## CONVENTIONS

- **Output naming**: semantic versioning (v0.1.0, v1.0.0)
- **Quality**: 300+ DPI for figures
- **Compression**: Lossless for text, optimized

## ANTI-PATTERNS (THIS PROJECT)

- **Low-resolution figures** → Use 300+ DPI
- **Missing metadata** → Include author/title/producer
- **No versioning** → Tag releases properly

## COMMANDS

```bash
# Merge PDFs
pdftk report.pdf slides.pdf output merged.pdf

# Using ImageMagick
convert -density 300 file.pdf output.pdf

# Optimize PDF
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/prepress -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
```

## NOTES

- Greenfield: No content yet
- Aggregates output from Lean, Report, Slides
- Coordinate with Orch-GroupAction for automated build
