# Dependencies

This directory should contain the pre-compiled native dependencies.

## Directory Structure

```
deps/
├── llvm/
│   ├── include/          # LLVM 18.1.8 headers
│   └── lib/              # LLVM 18 static libs (~78 libs)
├── clang/
│   ├── include/          # Clang 18.1.8 headers
│   └── lib/              # Clang 18 static libs (10 libs)
├── z3/
│   ├── include/          # Z3 headers (z3.h, z3++.h)
│   └── lib/              # Z3 static lib (libz3.lib)
└── rellic/
    ├── include/rellic/   # Rellic pass headers
    └── lib/              # Rellic static lib (rellic.lib)
```

## For CI (GitHub Actions)

Dependencies are automatically downloaded from the GitHub Release
asset `rellic-deps-win32-x64.zip` during the prebuild workflow.

## For local development

Download the deps zip from the latest release:
```powershell
gh release download v0.1.0 -p "rellic-deps-win32-x64.zip" -R LXrdKnowkill/hexcore-rellic
Expand-Archive rellic-deps-win32-x64.zip -DestinationPath .
```

Or build from source using the monorepo build scripts:
```powershell
cd <monorepo>/extensions/hexcore-rellic
python _rebuild_all.py
```
