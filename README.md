# Repolex Knowledge Graph of samuelcolvin/datafusion-sql-udfs

RDF knowledge graph data for [samuelcolvin/datafusion-sql-udfs](https://github.com/samuelcolvin/datafusion-sql-udfs), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/datafusion-sql-udfs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d173e9ba6efd98481ae2c175ce4a29f5f6c47876
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d173e9ba6efd98481ae2c175ce4a29f5f6c47876
│           └── chunk-001.nq.gz
├── blob
│   ├── 24adcf30254c348bd7024a9859bfa4346acd1818.nq.gz
│   ├── 365eb1c58bac90112363eecaf3d593536c94c38b.nq.gz
│   ├── 7fe296dc59d068d43c544f6294d015e67c8db6d1.nq.gz
│   ├── 9cfe38b08799e522ab4f942195876bd52e61f748.nq.gz
│   ├── be4940fe02b78d4d52e78ac2f8be1de5c0eb80c4.nq.gz
│   ├── c8cd0f4be29a337bd0f90f4bec18c194127d4336.nq.gz
│   ├── e75b0f9917da86383748c65b263f3ee0a53aa2a8.nq.gz
│   ├── f62fa52cb6e91778b5b8e24baf3222e800884033.nq.gz
│   └── fa364e66916d07006aa183ed4c703de1ce473649.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d173e9ba6efd98481ae2c175ce4a29f5f6c47876.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 15 files
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

[samuelcolvin/datafusion-sql-udfs](https://github.com/samuelcolvin/datafusion-sql-udfs)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
