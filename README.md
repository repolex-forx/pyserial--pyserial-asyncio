# Repolex Knowledge Graph of pyserial/pyserial-asyncio

RDF knowledge graph data for [pyserial/pyserial-asyncio](https://github.com/pyserial/pyserial-asyncio), parsed by [repolex](https://repolex.ai).

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
rlex download pyserial/pyserial-asyncio
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 13694c5a09188faf15f3ae08eae3772f3a707a68
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 13694c5a09188faf15f3ae08eae3772f3a707a68
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ad4e5ab00b9ae847d05587c0aae43028a4c523a.nq.gz
│   ├── 0eb1fe73ad2bf069aa49efd4ffe1a6358e3613c3.nq.gz
│   ├── 0f178abcb0abbbdf7905e49733441850851e4dde.nq.gz
│   ├── 14ba81b5cdac1ce1b600928e81726337cfa45a11.nq.gz
│   ├── 1645f844e67102d74fdb7abe66087813957ea979.nq.gz
│   ├── 2c264fd22d58acb38165ad8ba4d1037d57eb9d9e.nq.gz
│   ├── 3a0e2b227ef5d94232d86aa905e2997024e3de0e.nq.gz
│   ├── 3c2ec4cf8e98edfa110ed50963c9e0b0e6c4f6a0.nq.gz
│   ├── 47aa922f74c5b80ffddd160f6c557be1aa37d440.nq.gz
│   ├── 4d1c31a00836110a71df19b6c7f2a89737888641.nq.gz
│   ├── 561ab2f90ef04b3bf1789bc9c7f4b08a70216a81.nq.gz
│   ├── 6fa4fd9c48279f8139e8134916a1c1475a84e1d1.nq.gz
│   ├── 838436012f4e36a4c1701e2e14be3e7a4f21c6d1.nq.gz
│   ├── 869de9f0aff0647b95e7d52fe509a461cb305880.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── a84b76dded88f78669f9dcabb9757043e0e33cea.nq.gz
│   ├── a861fb2b18168dc033e787c77a0b64dcdb5dc36c.nq.gz
│   ├── be9a2d373bd8e47df41cee0da81bde027a4889f8.nq.gz
│   ├── e173b56c48616aed7ac9699e37f704262034a613.nq.gz
│   ├── e7cb53cc7278c9d5c85c6db438bdd636563f00cb.nq.gz
│   ├── e9ead6abf26c2521fb985c1a21c9226c79c1f221.nq.gz
│   ├── f867dfcfd1fa66ea1219366e18120f532b7c96bc.nq.gz
│   ├── fb44ebbd3d6ffb46a3b1759144c52a87a32d9841.nq.gz
│   └── ffc5453775b81423c53a725a50f5b1fa49bbee75.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 13694c5a09188faf15f3ae08eae3772f3a707a68.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[pyserial/pyserial-asyncio](https://github.com/pyserial/pyserial-asyncio)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
