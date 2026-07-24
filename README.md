# MDDash Notebooks

Curated notebook workflows for [MDDash](https://github.com/CERIT-SC/mddash), the molecular dynamics dashboard.

## Layout

Each MD engine has its own directory, with self-contained workflow modules inside:

```
gromacs/
  protein/        # Solvated protein setup and analysis
amber/
  protein/        # Solvated protein setup
```

Every module directory is copied as-is into an experiment workspace.

## Adding a new workflow

1. Create a directory under the appropriate engine (e.g. `gromacs/membrane/`).
2. Place the notebook(s), helper scripts, and schema files inside it.
3. Make sure everything is self-contained — bare imports and `$schema` relative paths must work from the module directory alone.
4. Register the new module in MDDash's bundled `notebook-modules.json` catalog.
