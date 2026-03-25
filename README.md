<h1 align="center">📚 Research Library &nbsp;<a href="https://vasileios-bellos.github.io/ResearchLibrary/"><img src="https://img.shields.io/badge/Live_Demo-Interactive_Mind_Map-3b82f6?style=flat" width="300"></a></h1>

An interactive mind map for exploring, filtering, and navigating my curated personal collection of scientific research papers. Built with [D3.js](https://d3js.org), it visualizes ~1,400 papers in coastal and ocean wave science - though the framework is domain-agnostic and can be adapted to any research field.

<div align="center">

<img src="https://img.shields.io/badge/Papers-1%2C399-3b82f6?style=flat" width="150" /> <img src="https://img.shields.io/badge/Authors-1%2C545-FF9800?style=flat" width="160" /> <img src="https://img.shields.io/badge/Categories-16-4CAF50?style=flat" width="160" /> <img src="https://img.shields.io/badge/Tags-76-9C27B0?style=flat" width="100" />

</div>

---

## Quick Start

Open [`Mind Map`](https://vasileios-bellos.github.io/research-library/) in any modern browser. No server, no installation, no dependencies - everything runs locally from just three files.

## Views

The mind map offers four distinct visualisation modes, each designed for a different way of exploring the literature.

| View | Description |
|------|-------------|
| **Tree** | Collapsible hierarchy of categories, subfolders, and papers. Click a category to expand and see its contents. Supports nested folder structures of arbitrary depth. |
| **Clusters** | Force-directed graph with papers as nodes, clustered by category. The largest category sits at the centre, with the rest arranged radially. Zoom and drag to explore. |
| **Network** | Co-authorship network built from CrossRef metadata. Node size reflects paper count; links represent co-authored publications. Search for any author to highlight their connections. |
| **Timeline** | Stacked bar chart of papers per year, colour-coded by category. Covers the full date range of the collection. |

## Features

| Feature | Description |
|---------|-------------|
| **Search** | Fuzzy search across titles, authors, and years with instant results |
| **Category filter** | Toggle categories on/off in the sidebar. Clear all / select all shortcut. |
| **Tag filter** | 76 domain-specific keyword tags with search. AND logic - selecting multiple tags narrows the results. |
| **Year range** | Dual-handle slider to filter papers by publication year |
| **Detail panel** | Click any paper for full metadata: author, year, journal, DOI link, tags, filename, and related papers |
| **Author search** | In the Network view, type a name to highlight that author and all their direct co-authors |
| **Drop-to-add** | Drag a PDF onto the mind map to instantly classify, tag, and add it to the visualisation |

## Data

Paper metadata was enriched using the [CrossRef API](https://api.crossref.org), providing proper author names, publication years, journal titles, and DOIs for 967 of the 1,399 papers. The remaining papers use metadata parsed from filenames.

Tags are assigned from a controlled vocabulary of 76 keywords organised into six facets: **topic**, **theory**, **method**, **depth regime**, **structure type**, and **output type**. Each paper carries at least five tags.

All data lives in `data.js` - a single JSON object loaded at startup. To adapt the mind map to a different paper collection, replace this file.

## File Structure

```
index.html       Main application (single-page, self-contained)
data.js          Paper metadata, categories, tags, author links, tree structure
d3.v7.min.js     D3.js v7 (vendored for offline use)
README.md
```

## Acknowledgements

Visualisation patterns adapted from [D3 Observable Examples](https://observablehq.com/@d3) by [Mike Bostock](https://bost.ocks.org/mike/):
- [Collapsible Tree](https://observablehq.com/@d3/collapsible-tree)
- [Force-Directed Graph](https://observablehq.com/@d3/force-directed-graph)
- [Stacked Bar Chart](https://observablehq.com/@d3/stacked-bar-chart)

Paper metadata from [CrossRef](https://www.crossref.org/) public API.

## Author

**[Vasileios Bellos](https://www.linkedin.com/in/vasileios-bellos/)**

## License

[MIT](LICENSE)
