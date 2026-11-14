# Pooling wells explorer

Interactive chart of how many wells (tubes) three combinatorial pooling layouts need for V guides when at most K guides share a well, next to the no-pooling baseline (N = V).

- 2D Fragmented: `N = 2K * ceil(V / K^2)`
- 2D Matrix: `N = 2s * ceil(s / K)`, `s = ceil(sqrt V)`
- 3D: `N = 3c * ceil(c^2 / K)`, `c = ceil(cbrt V)`

The formulas are the ones used by the pooling module of Diana (iGEM UMA-Málaga 2026). Counts include the empty slots a layout reserves but never fills. The chart compares well counts only; it says nothing about how reliably each layout decodes a screen.

It is one static page (`index.html`, no build step). Chart.js 4.4.1 is bundled in `vendor/`; fonts (Roboto Slab, Roboto Condensed) are in `fonts/` with their licences.

## Embedding

```html
<iframe src="https://javiertorralbo.dev/pooling-wells-explorer/" title="Pooling wells explorer" width="100%" height="760" style="border:0" loading="lazy"></iframe>
```

## Licence

MIT for the page (see `LICENSE`). Chart.js is MIT (https://www.chartjs.org), the fonts carry their own licences in `fonts/`.
