# MS C 5.0 + MASM 5.1 Cross-Compilation Toolchain

Pre-assembled Microsoft C 5.0 compiler and MASM 5.1 assembler for use with
the [doscc](https://github.com/Mario9501/doscc) cross-compilation tool and
the [XT](https://github.com/nicktrienenern/xt) 8086 emulator.

## Contents

| Directory  | Description |
|------------|-------------|
| `BIN/`     | Compiler, linker, assembler, and utility executables |
| `INCLUDE/` | C standard headers + MASM include files (BIOS.INC, DOS.INC) |
| `LIB/`     | Runtime libraries for all memory models (S/M/C/L) + LIBH.LIB |

## Versions

- **MS C 5.0** (1987) — `CL.EXE`, `C1.EXE`, `C2.EXE`, `C3.EXE`, `LINK.EXE`
- **MASM 5.1** (1988) — `MASM.EXE`, `BIOS.INC`, `DOS.INC`
- **LIBH.LIB** — Helper library providing long arithmetic routines
  (`__aNlmul`, `__aNldiv`, `__aNlrem`, `__aNNalshr`)

## Usage with doscc

After cloning, point doscc at this toolchain:

```bash
# Automatic (doscc setup wizard)
doscc setup

# Manual (edit ~/.doscc/config.toml)
[toolchains.msc50]
path = "/path/to/this/repo"
```

## Original Sources

- MS C 5.0: Microsoft C Optimizing Compiler 5.0 (1987), 5.25" 360K floppies
- MASM 5.1: Microsoft Macro Assembler 5.1 (1988), 5.25" floppies
- Both available at [WinWorldPC](https://winworldpc.com/) and
  [archive.org](https://archive.org/)

## License

These are vintage Microsoft tools from 1987-1988, preserved for retrocomputing
and historical software development. Use at your own discretion.
