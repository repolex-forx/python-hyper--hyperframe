# Repolex Knowledge Graph of python-hyper/hyperframe

RDF knowledge graph data for [python-hyper/hyperframe](https://github.com/python-hyper/hyperframe), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/hyperframe
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 632e309bf6d76d6a3cd04e3cbc0b006eddbf7056
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 632e309bf6d76d6a3cd04e3cbc0b006eddbf7056
│           └── chunk-001.nq.gz
├── blob
│   ├── 1092bf085ed4310adfd18388f98f28c648ba7381.nq.gz
│   ├── 1154eb5ad5f7a2e4d9a1ab8e49091b08381f8280.nq.gz
│   ├── 1290cf2042ba4eed8f811ea5504b67098291cfe8.nq.gz
│   ├── 17b6a98c27a8c17d7d3cd30f68e6798f75fc4b6a.nq.gz
│   ├── 1a53151131c9855720fb150a278b34d04b99b9c9.nq.gz
│   ├── 226d7e2bf948a2c3116c410d0599b5a823df8715.nq.gz
│   ├── 2e4c0b21c39c2fdad6ef336f3858d2aed877e8cb.nq.gz
│   ├── 51c50478f0bbfbee194ab969f4136f9fc0bf6ccb.nq.gz
│   ├── 5bab673d5b2b5cf99634320b642766ef54e62791.nq.gz
│   ├── 6247f7e231716482115f34084ac61030743e0715.nq.gz
│   ├── 750102f65e2cd125637df9d3c177f8f7ce67f941.nq.gz
│   ├── 7a40f4ab767eeaad952e268010fc080475912b93.nq.gz
│   ├── 85add81b02aba728f5db603ad9817abe9bc44bad.nq.gz
│   ├── 8c57adb2e85541910fbbb5854e274fdb303dabce.nq.gz
│   ├── aa7ab8b637cab250e1e625373ce93104204771b6.nq.gz
│   ├── b6833549fed75e8a2e1474e22172a19525273d2b.nq.gz
│   ├── d0c3cbf1020d5c292abdedf27627c6abe25e2293.nq.gz
│   ├── d24c351e1889b5b7837e4c9c1dc59334191c7f2c.nq.gz
│   ├── d7710d4fd66ba9295bfa39fe57c30b2098b27960.nq.gz
│   ├── d95c2f18d9b7bf9e97e717c8d15c81aa96bb8228.nq.gz
│   ├── db2472009c60acc72ca2f6f065bb4b674dc66746.nq.gz
│   ├── e5650c45b0c1a8180cfefcec1c423730c55a201b.nq.gz
│   ├── e5f4a22bd96e6ef3a327b962681bf6a9a76f5804.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fe6e2e70e75926d233076fd1748e111bd3fcebdd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 632e309bf6d76d6a3cd04e3cbc0b006eddbf7056.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[python-hyper/hyperframe](https://github.com/python-hyper/hyperframe)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
