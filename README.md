## IDA PS5 .elf plugin (c) 2021-2022 by flatz

# Instructions
* Put all files into their corresponding directories by keeping this directory's structure.
* Use `64-bit IDA` and standard `ELF64 for x86-64 (Unknown) [elf64.dll]` when loading `.elf`/`.prx` file.
* Apply any kernel options that you use usually.
* If you see warning `Unsupported or unknown image type`, then press `Yes`, thus ignoring it.
* Wait till plugin complete its own work. I use many heuristics to locate a lot of useful information within .elf file, so please be patient.
* Ignore all possible warnings that may happen during processing. Some of structures are getting updates from one version of SDK to another, that may cause warnings as well until they will be fully supported.
* If you want to add new symbols or edit existing ones, then update file `cfg/ps5_symbols.txt` and `til/prospero.til` optionally.

# Known bugs
* Need to update some structures, e.g. sceProcessParam, to reflect more fields that it may take.
* Need to parse exception handler sections properly because their format was changed since PS4. Could be useful to tweak function boundaries even more.

P.S. PRs with bug fixes and improvements are welcome.
