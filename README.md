# Repolex Knowledge Graph of jaraco/pytest-checkdocs

RDF knowledge graph data for [jaraco/pytest-checkdocs](https://github.com/jaraco/pytest-checkdocs), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download jaraco/pytest-checkdocs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 356d6718b154e95fbda0b87b9d477a2199a67614
│   │   │   └── chunk-001.nq.gz
│   │   └── cd17badd6fe68cc3386e29a38c046e528a4265d7
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── cd17badd6fe68cc3386e29a38c046e528a4265d7.nq.gz
│   └── repolex
│       ├── 356d6718b154e95fbda0b87b9d477a2199a67614
│       │   └── chunk-001.nq.gz
│       └── cd17badd6fe68cc3386e29a38c046e528a4265d7
│           └── chunk-001.nq.gz
├── blob
│   ├── 01f1e5f01beea0a564de9b2cd2c0c29ce9ec23a0.nq.gz
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1413c857001e3c9a52e996eac460be96d827208f.nq.gz
│   ├── 14243051409fccc0404edd15a2c993e572626dd8.nq.gz
│   ├── 15cc07300297309bfebcdb6eac0458bff5831273.nq.gz
│   ├── 1b1ec8acc718156f4331f49de5456ef730896b5e.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 3db4ea780c9353f7c61bbe0caf20c1c86e4b7fd8.nq.gz
│   ├── 53513eee9b3a2f4df50df1febd59a5206718995a.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 63c0825f6bd49615f4f386b95463111f7992f6bc.nq.gz
│   ├── 64978c08f5f3a922875675d229e739ca699b31cc.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 81c696441f2e30365f3bf41c784b4eb02b74823e.nq.gz
│   ├── 8a37da07e52983bedcf7a3f7221321836ff18e94.nq.gz
│   ├── 8cbce3d28990b827a3e9ed7d4be88f61e3c4b31e.nq.gz
│   ├── 906c9073238be6cee630452300cdc2f39978a484.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── a5f7743ee739d418cde5b9bb73062dfababff00a.nq.gz
│   ├── d1b21850709bb2f415a2ff1e54f16b7decc99d18.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fa5592412f13835ef19d2517513c9f5c4af96ead.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── cd17badd6fe68cc3386e29a38c046e528a4265d7.nq.gz
├── filetree
│   ├── 356d6718b154e95fbda0b87b9d477a2199a67614.nq.gz
│   └── cd17badd6fe68cc3386e29a38c046e528a4265d7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

17 directories, 41 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[jaraco/pytest-checkdocs](https://github.com/jaraco/pytest-checkdocs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
