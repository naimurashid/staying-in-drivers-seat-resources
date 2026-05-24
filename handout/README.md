# Handout

## `staying-in-the-drivers-seat.pdf`

The downloadable PDF guide audience members are pointed to from the talk. Branded with the lab's navy / Carolina-blue typographic identity. Rendered from `source.qmd`.

## `source.qmd`

The Quarto source used to build the PDF. Includes the LaTeX configuration in its YAML header that produces the branded title page, running header, section colors, and Arial body font.

### To rebuild the PDF

Requires Quarto + a TeX distribution with `xelatex`, and Arial installed system-wide.

```bash
cd handout/
quarto render source.qmd
mv source.pdf staying-in-the-drivers-seat.pdf
```

### Relation to the lab-handbook source

The substantive content of `source.qmd` mirrors the lab handbook's `code-ownership.qmd`. The branded PDF has additional YAML configuration for PDF output (title page, fonts, custom LaTeX styling) that the web version doesn't need.

If you update content in the lab handbook, you'll need to re-sync `source.qmd` here (typically by replacing everything after the YAML block) and re-render.
