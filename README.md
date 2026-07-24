# MDDash Notebooks

Curated notebook workflows for [MDDash](https://github.com/sb-ncbr/mddash), the molecular dynamics dashboard.

## Layout

Each MD engine has its own directory, with self-contained workflow modules inside:

```
gromacs/
  protein/        # Solvated protein setup and analysis
amber/
  protein/        # Solvated protein setup
```

Every module directory is copied as-is into an experiment workspace. A module must be self-contained — notebooks, helper scripts, and JSON schemas all live together so that bare imports and `$schema` relative paths work from the experiment root.

## Adding a new workflow

1. Create a directory under the appropriate engine (e.g. `gromacs/membrane/`).
2. Place the notebook(s), helpers, and schema files inside it.
3. Register the module in MDDash's bundled `notebook-modules.json` catalog.

External repositories (e.g. Binder-compatible repos) can also be registered with `"path": "."` and a `"repository"` URL, in which case the full repository is cloned as-is.
