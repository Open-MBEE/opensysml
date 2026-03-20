# opensysml

Minimal package layout for publishing both `opensysml` and `sysml`.

## Layout

- `packages/opensysml`: primary Python distribution and import package
- `packages/sysml`: compatibility distribution that depends on `opensysml`
- `recipe/meta.yaml`: conda-forge multi-output recipe for both package names

## Local build

```powershell
python -m build .\packages\opensysml
python -m build .\packages\sysml
```

## Conda build

The `recipe/meta.yaml` file is structured as a multi-output recipe so a
conda-forge feedstock can publish both `opensysml` and `sysml` from the same
repository.
