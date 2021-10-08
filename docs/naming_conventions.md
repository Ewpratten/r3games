# Project Naming Conventions

## Whole project

The whole project should follow the [Snake Case](https://en.wikipedia.org/wiki/Snake_case) naming system. This means that folder names and file names should both be in lowercase and separated by underscores.

## Asset organization

Assets live in the `/assets` directory, and are sorted based on their parent project. All assets for a project should be contained in `/assets/proj/<project_name>`, known as the **Project Asset Root** (PAR). The PAR may be used in file paths in this document as `$PAR`.

The PAR is then broken into subdirectories based on the file's purpose, aka: weather the file is a **workfile** or a **production asset**.

Assets inside these directories should then be sorted by type:

| Asset Type    | Workfile Path   | Production Asset Path |
|---------------|-----------------|-----------------------|
| Characters    | `$PAR/work/chr` | `$PAR/prod/chr`       |
| Scene Objects | `$PAR/work/obj` | `$PAR/prod/obj`       |

### Workfiles

  - Stored in `$PAR/workfiles`
  - Contains DCC-specific save files (`.blend`, `.xcf`, `.psd`, etc.)