# Repolex Knowledge Graph of devicekit/DeviceKit

RDF knowledge graph data for [devicekit/DeviceKit](https://github.com/devicekit/DeviceKit), parsed by [repolex](https://repolex.ai).

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
rlex download devicekit/DeviceKit
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fab82bd988405367c915143e293479f481e93ba0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fab82bd988405367c915143e293479f481e93ba0
│           └── chunk-001.nq.gz
├── blob
│   ├── 0134dfe0b9a7eca79f423731292a4834936c50b5.nq.gz
│   ├── 0980478690937bd746b83dea778bddd999f43c97.nq.gz
│   ├── 0c67376ebacb410fd873cac1d8d8dd431b262c02.nq.gz
│   ├── 14a1a74bf67fc218f8f3ef853b0ba2c7923583f0.nq.gz
│   ├── 18d981003d68d0546c4804ac2ff47dd97c6e7921.nq.gz
│   ├── 2809633ae43e9f00c160dde6d8702308d173057c.nq.gz
│   ├── 2d29d234625bfcc7d6ec81a3a15e6a3e3fcbffc5.nq.gz
│   ├── 8206bd8a0c647180f9751375fc80d6d3df391117.nq.gz
│   ├── 8f26694484c789ddedf99c86d2409f409e35ba3c.nq.gz
│   ├── 94b2795e225da4a26d84167bc90b2474092a7f03.nq.gz
│   ├── 95003b0615c36f880aba4846d5a1dfda857efd56.nq.gz
│   ├── 984ce4dd21e309ba114a929b5cde229111dfb857.nq.gz
│   ├── 9a0521cd75be234aafb6a2a18447d92464847ce1.nq.gz
│   ├── 9c94b98b61e4f2cf9cc68a7272cf9dd2e8ab3eae.nq.gz
│   ├── 9cb6c7316d200353832352189a98ad0a9adf45fa.nq.gz
│   ├── a3ebf4a2ed97cb1bbbdc38f5236ada82769a95e5.nq.gz
│   ├── a751024c469366bc890cb811d54508bd900ce3cb.nq.gz
│   ├── a822d8cefd41d16092e933c1aabca2a9103c8d0c.nq.gz
│   ├── af7f28214406a46491f4ab22dc36999e8dac578d.nq.gz
│   ├── b10138c73600522fd45bc2193138f1c035c60a94.nq.gz
│   ├── b3cdf245547dea419e99fe52b237b952be1df5ad.nq.gz
│   ├── b7b0056ce8e47c5a290144150d5368eb251fdbf4.nq.gz
│   ├── ba72822e8728ef2951005e49b6c27a2f1da6572d.nq.gz
│   ├── beaf51fa82537512b3e5f5be557277f51f4bda74.nq.gz
│   ├── c792c52e8daad9d156ac1208cc30625e7d7bd0ca.nq.gz
│   ├── ca23c84f4c4e0c3bd1dc74cd562b3bf0aba22335.nq.gz
│   ├── cc0fae25973cf4cfbb9af3de23a12b218527cdc3.nq.gz
│   ├── d72930c22ca0516a8a0e444b52ef0ac0beec13a9.nq.gz
│   ├── e6de23621c8e18a41187021c744a81f31815fe13.nq.gz
│   ├── e796c1cffb42c503f7abdc5ba7235630b955fca3.nq.gz
│   └── fb5698a2583dc1c4e0db6bc245d20367da7b9f35.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fab82bd988405367c915143e293479f481e93ba0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[devicekit/DeviceKit](https://github.com/devicekit/DeviceKit)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
