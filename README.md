# Repolex Knowledge Graph of katharostech/cfg_aliases

RDF knowledge graph data for [katharostech/cfg_aliases](https://github.com/katharostech/cfg_aliases), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download katharostech/cfg_aliases
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3d55ba79872b61265a7176110a5200df0c9d9e54
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3d55ba79872b61265a7176110a5200df0c9d9e54.nq.gz
│   └── repolex
│       └── 3d55ba79872b61265a7176110a5200df0c9d9e54
│           └── chunk-001.nq.gz
├── blob
│   ├── 03c085883374a75d289032aca8f2228d4fec8b17.nq.gz
│   ├── 765da4950c3ac093c107666259da3ba5eac619d6.nq.gz
│   ├── 7af4ca5367ef2fc7eb48ca17b21c82260f8d16f1.nq.gz
│   ├── 96ef6c0b944e24fc22f51f18136cd62ffd5b0b8f.nq.gz
│   ├── ae270efac1d2413a4af5072390ca5da3aafaf81f.nq.gz
│   ├── b4ae2b8108f30695f0562419fea17484b38b85ba.nq.gz
│   ├── bdf6f4be136f78335919f9f86cfc031a6291af91.nq.gz
│   ├── d2ef45b3c01d286d910b1aa7744a267f1706ac2b.nq.gz
│   └── f1dcd62842ca2d724b6b9a33185ad925a5c4698e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3d55ba79872b61265a7176110a5200df0c9d9e54.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 18 files
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

## Source repository

[katharostech/cfg_aliases](https://github.com/katharostech/cfg_aliases)

---
*Parsed on 2026-04-22 by [repolex](https://repolex.ai)*
