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

### To update the content

`source.qmd` is the canonical source for the published handout PDF in this repo. To change content, edit `source.qmd` and re-run the rebuild steps above.
