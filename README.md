# Leidokos-ChangeReport

Generates change reports with [elf_diff](https://github.com/CapeLeidokos/elf_diff) for the [Kaleidoscope](https://github.com/keyboardio/Kaleidoscope) firmware.

Sketches of two separate bundle repos are build that represent the old
and new state before and after a change to any of the firmwares subrepository. The resulting binaries are compared with `elf_diff`
and a report is generated as a pdf file.

The report contains detailed information about the binaries, their source code git-versions, the build environment and the changes to the firmware in terms of a symbol analysis.

## Usage

```
lcr [--old-sketch old_sketch]
    [--new-sketch new_sketch]
    [--title title]
    [--elf_diff-executable elf_diff_executable]
    [--report-file report_file]
    [sketches...]
```

* old_sketch: The old sketch file to build (identifies the old bundle directory tree).
* new_sketch: The new sketch file to build (identifies the new bundle directory tree).
* title: A string to be used as report title.
* elf_diff_executable: The elf_diff executable. Only supply this if elf_diff cannot be found in your PATH.
* report_file: The path to a pdf file that is supposed to be created.

## Requirements

Leidokos-ChangeReport requires [elf_diff](https://github.com/CapeLeidokos/elf_diff) to be installed together with all Python packages it requires to generate pdf-reports.
