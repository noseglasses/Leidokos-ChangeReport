# Leidokos-ChangeReport

Generates change reports with [elf_diff](https://github.com/CapeLeidokos/elf_diff) for the [Kaleidoscope](https://github.com/keyboardio/Kaleidoscope) firmware.

Sketches of two separate bundle repos are build that represent the old
and new state before and after a change to any of the firmwares subrepository. The resulting binaries are compared with `elf_diff`
and a report is generated as a pdf file.

The report contains detailed information about the binaries, their source code git-versions, the build environment and the changes to the firmware in terms of a symbol analysis.

## Usage

```
usage: lcr [-h] [--old_sketch OLD_SKETCH_FILENAME]
           [--new_sketch NEW_SKETCH_FILENAME]
           [--old_kaleidoscope_repo OLD_REPO_PATH]
           [--new_kaleidoscope_repo NEW_REPO_PATH] [--title CHANGE_TITLE]
           [--elf_diff-executable ELF_DIFF_EXECUTABLE]
           [--report_file_basename REPORT_FILE_BASENAME]
           [--report_target_dir REPORT_TARGET_DIR] [-v]
           [sketches [sketches ...]]

Compare two firmware bundles and generate a change report.

positional arguments:
  sketches              The sketches (this is an alternative to --old-sketch
                        and --new-sketch)

optional arguments:
  -h, --help            show this help message and exit
  --old_sketch OLD_SKETCH_FILENAME
                        The old Arduino sketch
  --new_sketch NEW_SKETCH_FILENAME
                        The new Arduino sketch
  --old_kaleidoscope_repo OLD_REPO_PATH
                        Path to the old kaleidoscope repo
  --new_kaleidoscope_repo NEW_REPO_PATH
                        Path to the new kaleidoscope repo
  --title CHANGE_TITLE  A title to use for the report
  --elf_diff-executable ELF_DIFF_EXECUTABLE
                        An absolute path to the elf_diff exectuable.
  --report_file_basename REPORT_FILE_BASENAME
                        The path of the report file to generated.
  --report_target_dir REPORT_TARGET_DIR
                        The path where to store report files.
  -v, --verbose         Enable verbose output.
```

## Requirements

Leidokos-ChangeReport requires [elf_diff](https://github.com/CapeLeidokos/elf_diff) to be installed together with all Python packages it requires to generate pdf-reports.
