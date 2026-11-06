# Repolex Knowledge Graph of ansible-community/antsichaut

RDF knowledge graph data for [ansible-community/antsichaut](https://github.com/ansible-community/antsichaut), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/antsichaut
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5930d6c87cb67aa980f59df73ef1b242ba36f559
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5930d6c87cb67aa980f59df73ef1b242ba36f559
│           └── chunk-001.nq.gz
├── blob
│   ├── 153418eeed13d88f6cbec3e47f0612bf4d7b0cbc.nq.gz
│   ├── 498c064dc01d35166b6b81ef00073eabcb21294c.nq.gz
│   ├── 4c5f747ad550cd53ecf295f387a8b7d16f20bc35.nq.gz
│   ├── 4e84a309f18b2d9229b1d7849c51408acaa2b708.nq.gz
│   ├── 525de22c02656c7f94bf1e0525e047261e01d5ee.nq.gz
│   ├── 536e53dc9395cc3fc67de8beb11d1c3e2c352fc9.nq.gz
│   ├── 5cf4f99c9b9e51e260bbdb32b6f70a5f01ad2064.nq.gz
│   ├── 64c0ed4c69c42e3c3f7a15dd5b8bfef24b71c633.nq.gz
│   ├── 67215b6215579dcb63fb62a7170c7ccf0f55fce2.nq.gz
│   ├── 720f6e581a2dbe316f041b3a073d7f6d9bb8d339.nq.gz
│   ├── 79740da321f3b0b31e9b2f1a9ee7266b5c2c95e6.nq.gz
│   ├── 817360b9fe2ccbe28fd42ebfda900063ac3164ba.nq.gz
│   ├── 8e50178152adef4cccd9905007346138fabaeda6.nq.gz
│   ├── 8e68aa3ec801b174874ea29f387635ce82446cc0.nq.gz
│   ├── 9ad6cf413fd6297fe50b9d34eb3c7cd55d29ed04.nq.gz
│   ├── 9b7fe3e936e01174a1017320dacbfecf1d1f8e66.nq.gz
│   ├── a08b45521204d23b0109b8c88e1d375c804b4615.nq.gz
│   ├── a0bf4a16c5de5c627ada7f6235d89d53d490b831.nq.gz
│   ├── a0d110075afea202b7d36bb83e4d9dd5318b3f81.nq.gz
│   ├── ab97630832e0e548efaa089549c05c976e39e81d.nq.gz
│   ├── b60fb1c62f2269058bc4f59e49ea036c9809eacc.nq.gz
│   ├── cac5d91679844f61fa8e2115c0c4c41740fa0e93.nq.gz
│   ├── cd140b69cc9eb2021989c5fe276254e047dd6bfa.nq.gz
│   ├── d307fec4b8b036f77e051bebf586d65cdffcac14.nq.gz
│   ├── e079f8a6038dd2dc8512967540f96ee0de172067.nq.gz
│   ├── e36ba6c17a1dc91ad2b8fc444f3bf4aad4bd965e.nq.gz
│   ├── e53a7f3abb19bad6472af5e31d8220004930d091.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8eb302371569bb4e0cc702eb418f6a660ffd768.nq.gz
│   └── f077e54be45a388be0e489a8da2d4af54f6d9b18.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5930d6c87cb67aa980f59df73ef1b242ba36f559.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[ansible-community/antsichaut](https://github.com/ansible-community/antsichaut)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
