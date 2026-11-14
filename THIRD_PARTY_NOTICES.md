# Third-party notices

## Luraph deep engine

NOX Deobfuscator includes a vendored copy of the Luraph v15/v14.x deobfuscator
in `resources/luraph-engine/`.

- Upstream project: `caomod2077/Deobfuscator-Luraph-V15`
- Copyright: the upstream contributors
- License: MIT

The full MIT license text is available at `resources/luraph-engine/LICENSE`.

## Prometheus / MoonSec deep engine

NOX Deobfuscator includes a vendored copy of the Prometheus Deobfuscator
Toolkit in `resources/prometheus-engine/`.

- Upstream project: `0x251/Prometheus-Deobfuscator`
- Copyright: the upstream contributors
- License: the upstream README declares MIT, but the reviewed snapshot does
  not contain a `LICENSE` file. Included as-is for local, offline use.
- Modifications: `networkx` and `colorama` imports were made optional so the
  bundled toolkit runs on a standard-library-only Python installation. Python
  `eval` calls used by the text transforms were replaced with a whitelist numeric
  evaluator (`modules/safe_math.py`); calls, attribute access and other
  expression forms are rejected. The upstream bytecode-compilation path and its
  `subprocess` dependency were removed because NOX only processes text.

The toolkit operates on text and does not execute the analyzed Lua file.

## MoonSec deep engine

NOX Deobfuscator includes the MoonSec V2/V3 devirtualizer and bytecode lifter
in `resources/moonsec-engine/`.

- Copyright: the upstream contributors
- License: MIT (as declared in `resources/moonsec-engine/engine.json`)

## luau-vmp engine

`resources/luau-vmp-engine/` holds a vendored copy of the luau-vmp-deobf
toolkit. It is present in the source tree for reference and is not shipped in
the Windows installer: the current build does not reference it from the code.

- Upstream project: `binxgtl/luau-vmp-deobf`
- Copyright (c) 2026 luau-vmp-deobf contributors
- License: MIT

The full MIT license text is available at `resources/luau-vmp-engine/LICENSE`.

## Luau

`resources/luraph-engine/bin/luau.exe` and `luau-ast.exe` are Luau runtime and
AST tooling binaries. Luau is developed by Roblox Corporation and contributors
and is distributed under the MIT license.

- Project: https://github.com/luau-lang/luau
- License: MIT
