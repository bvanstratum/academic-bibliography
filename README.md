# Academic Bibliography

A single-source BibTeX bibliography that syncs into LaTeX projects and Obsidian.

## Repository layout

```
references.bib   ← the one file to rule them all
```

## Using with LaTeX

### Option A — Git submodule (recommended)

Add this repo as a submodule inside your LaTeX project:

```bash
git submodule add https://github.com/bvanstratum/academic-bibliography.git bib
```

Then reference the bibliography in your `.tex` file:

```latex
\bibliography{bib/references}
```

Update to the latest entries at any time:

```bash
git submodule update --remote bib
```

### Option B — Direct path

Clone or copy `references.bib` alongside your `.tex` file and reference it directly:

```latex
\bibliography{references}
```

## Using with Obsidian

1. Install the [**Citations**](https://github.com/hans/obsidian-citation-plugin) community plugin.
2. Open *Settings → Citations*.
3. Set **Citation database path** to the absolute path of `references.bib` in your local clone of this repo (e.g. `~/repos/academic-bibliography/references.bib`).
4. Use the *Insert literature note* or *Open literature note* commands to create Markdown notes from any entry in the file.

Keeping this repo cloned locally means Obsidian always reads the most up-to-date bibliography after a `git pull`.

## Adding new entries

Edit `references.bib` directly. Templates for all common entry types (article, book, chapter, conference paper, misc) are included as comments at the top of the file.

Commit and push your changes so every LaTeX project and Obsidian vault stays in sync.
