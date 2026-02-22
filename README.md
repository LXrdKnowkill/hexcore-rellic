# hexcore-rellic

Experimental N-API bindings for pseudo-C decompilation — lifts machine code via Remill and decompiles LLVM IR to pseudo-C using a custom Rellic-inspired pipeline.
Part of [HikariSystem HexCore](https://github.com/LXrdKnowkill/HikariSystem-HexCore).

> **Warning: Experimental.** This module generates low-level IR-style pseudo-C with mnemonic annotations. Best suited for automated pattern matching and batch analysis. Real Clang AST-based decompilation passes are planned for a future release.

## Supported Architectures

| Architecture | Status |
|---|---|
| x86-64 | Supported |
| x86 (32-bit) | Supported |
| AArch64 | Not yet supported |

## Dependencies

- LLVM 18 static libraries
- Clang 18 AST and CodeGen libraries
- Z3 SMT solver
- Remill semantics module

Must use the same LLVM version as hexcore-remill (currently LLVM 18).

## License

MIT - Copyright (c) HikariSystem
