<h1 align="center">📚 Research Library 📚</h1>

<h1 align="center"><a href="https://vasileios-bellos.github.io/ResearchLibrary/"><img src="https://img.shields.io/badge/Interactive_Mind_Map-3b82f6?style=flat" width="300"></a></h1>

An interactive mind map for exploring, filtering, and navigating my curated personal collection of scientific research papers. Built with [D3.js](https://d3js.org), it visualizes ~1,350 papers in coastal and ocean wave science - though the framework is domain-agnostic and can be adapted to any research field.

<div align="center">

<a href="https://vasileios-bellos.github.io/ResearchLibrary/"><img src="https://img.shields.io/badge/Papers-1%2C336-3b82f6?style=flat" width="150" /></a> <a href="https://vasileios-bellos.github.io/ResearchLibrary/"><img src="https://img.shields.io/badge/Authors-1%2C419-FF9800?style=flat" width="160" /></a> <a href="https://vasileios-bellos.github.io/ResearchLibrary/"><img src="https://img.shields.io/badge/Categories-17-4CAF50?style=flat" width="160" /></a> <a href="https://vasileios-bellos.github.io/ResearchLibrary/"><img src="https://img.shields.io/badge/Tags-76-9C27B0?style=flat" width="100" /></a>

</div>

---

## Quick Start

Open [`Mind Map`](https://vasileios-bellos.github.io/research-library/) in any modern browser. No server, no installation, no dependencies - everything runs locally from just three files.

## Views

The mind map offers four distinct visualization modes, each designed for a different way of exploring the literature.

| View | Description |
|:----:|:------------|
| Tree | Collapsible hierarchy of categories, subfolders, and papers. Click a category to expand and see its contents. Supports nested folder structures of arbitrary depth. |
| Clusters | Force-directed graph with papers as nodes, clustered by category. The largest category sits at the center, with the rest arranged radially. Zoom and drag to explore. |
| Network | Co-authorship network built from CrossRef metadata. Node size reflects paper count; links represent co-authored publications. Search for any author to highlight their connections. |
| Timeline | Stacked bar chart of papers per year, color-coded by category. Covers the full date range of the collection. |

## Features

| Feature | Description |
|:-------:|:------------|
| Search | Fuzzy search across titles, authors, and years with instant results |
| Category filter | Toggle categories on/off in the sidebar. Clear all / select all shortcut. |
| Tag filter | 76 domain-specific keyword tags with search. AND logic - selecting multiple tags narrows the results. |
| Year range | Dual-handle slider to filter papers by publication year |
| Detail panel | Click any paper for full metadata: author, year, journal, DOI link, tags, filename, and related papers |
| Author search | In the Network view, type a name to highlight that author and all their direct co-authors |
| Drop-to-add | Drag a PDF onto the mind map to instantly classify, tag, and add it to the visualization |

## Data

Paper metadata was enriched using the [CrossRef API](https://api.crossref.org), providing proper author names, publication years, journal titles, and DOIs for 904 of the 1,336 papers. The remaining papers use metadata parsed from filenames.

Tags are assigned from a controlled vocabulary of 76 keywords organized into six facets: **topic**, **theory**, **method**, **depth regime**, **structure type**, and **output type**. Each paper carries at least five tags.

All data lives in `data.js` - a single JSON object loaded at startup. To adapt the mind map to a different paper collection, replace this file.

## Automation

The statistics in this README are kept in sync with `data.js` via a [GitHub Action](.github/workflows/update-statistics.yml) that runs automatically on every push.

## File Structure

```
index.html       Main application (single-page, self-contained)
data.js          Paper metadata, categories, tags, author links, tree structure
d3.v7.min.js     D3.js v7 (included locally for offline use)
README.md
```

## Acknowledgements

Visualization patterns adapted from [D3 Observable Examples](https://observablehq.com/@d3) by [Mike Bostock](https://bost.ocks.org/mike/):
- [Collapsible Tree](https://observablehq.com/@d3/collapsible-tree)
- [Force-Directed Graph](https://observablehq.com/@d3/force-directed-graph)
- [Stacked Bar Chart](https://observablehq.com/@d3/stacked-bar-chart)

Paper metadata from [CrossRef](https://www.crossref.org/) public API.

Special thanks to my former colleague and friend [Steven Huo](https://www.linkedin.com/in/chong-h-507695152/) for brainstorming and inspiring this idea during our early years in the PhD.

## Author

**[Vasileios Bellos](https://www.linkedin.com/in/vasileios-bellos/)**

## License

[MIT](LICENSE)
