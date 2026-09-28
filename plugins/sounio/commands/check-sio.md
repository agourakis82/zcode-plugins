---
description: Check one Sounio .sio file with an existing local compiler
---

Check the single `.sio` file named in $ARGUMENTS. If there is no unambiguous path, ask for one. Do not search the filesystem for a substitute file.

1. Read the project's agent instructions before running a command. Confirm the file exists and has a `.sio` extension.
2. From the Sounio repository root, prefer its `bin/souc` wrapper. Otherwise use `souc` already on `PATH`. If neither is available, report that prerequisite and stop. Do not download, build, or install a compiler.
3. Run the selected compiler's `check` subcommand on that file, with the path passed as one quoted argument. Do not use `eval`, interpolate the path into a shell program, or run `compile` or `run`.
4. Report the compiler path, source path, exit status, and relevant diagnostics. A successful `check` is only a source-check result; it does not establish successful native compilation, execution, scientific validity, or CI status.
