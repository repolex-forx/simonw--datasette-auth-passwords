# Repolex Knowledge Graph of simonw/datasette-auth-passwords

RDF knowledge graph data for [simonw/datasette-auth-passwords](https://github.com/simonw/datasette-auth-passwords), parsed by [repolex](https://repolex.ai).

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
rlex download simonw/datasette-auth-passwords
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bb96899c84395bb40e903b0da5e1e7cdb5d8c4dd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bb96899c84395bb40e903b0da5e1e7cdb5d8c4dd
│           └── chunk-001.nq.gz
├── blob
│   ├── 024a80cd9e5b28cf9113ae2082751ebefd2a70f7.nq.gz
│   ├── 10718c94b35f7cbfb8c914691e66f8e938e214ad.nq.gz
│   ├── 150fd2fa9b06321f5c66139afb5028276b8d5ba9.nq.gz
│   ├── 230e31dcde10714ff53e5f65df0879b029025076.nq.gz
│   ├── 53605b7a5ec51bc95dca4fb43fdb350bf9362435.nq.gz
│   ├── 641c4b55d03cd3ba3f2184b0a448b173766dcd7e.nq.gz
│   ├── 65af5fa713f65e3fcca7c393cb6145da8e31ab17.nq.gz
│   ├── 6ecd8364dec38630f6f726b515d622eeed5117b6.nq.gz
│   ├── 8d976dbd314d8b3c53429659f499618ccd48d650.nq.gz
│   ├── b1a7f7542cdd5978aa4695e2cec995030d568576.nq.gz
│   ├── b7f99b96f6dc3f4a302bd66d2c2d47723c339b25.nq.gz
│   └── ea47dfbd6469152f24cf64ef3562852ef334c97d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bb96899c84395bb40e903b0da5e1e7cdb5d8c4dd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[simonw/datasette-auth-passwords](https://github.com/simonw/datasette-auth-passwords)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
