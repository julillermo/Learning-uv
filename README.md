# Learning-uv
Playground for trying out the uv python build tool.

## Details
- Mainly a repo to follow along the [Tech With Tim Youtube Channel's Video](https://www.youtube.com/watch?v=6pttmsBSi8M&t=1s) on uv in preparation for a personal project.

## Commands of interest
- `uv python list`
  - This appears to detect the system's installed python version. However, installing with `uv` would appear to create a space for `uv` managed python instances [docs](https://docs.astral.sh/uv/guides/install-python/#using-existing-python-versions)
- `uv python upgrade`
  - upgrade all uv-managed Python versions
- `uv run [path_path_to_python_file.py]`
- `uv run --python 3.12.3`
  - for specifying use of a specific python version.
- `uv run --with [package_name]`
  - For running with a package without commiting it as part of the project.
  - Will be cached for future runs
  - A lot like `npx` where the package is ran without necessarily being part of the project.
- `uv init`
  - Kind of analogous to `npm init` or `pnpm init` to start a TypeScript project.
  - This creates a `pyproject.toml` which is akin the a `package.json`
- `uv add [package_name]`
  - Add's the apckage to the `pyproject.toml`
  - If you set up a [workspace in uv](https://docs.astral.sh/uv/concepts/projects/workspaces/#when-not-to-use-workspaces), this also works within specific app/package directories like it would in `pnpm` workspaces.

## Things to note
- The `uv` build tool doesn't seem to have "script" commands you can specify in the `.toml` file like you would in `package.json`