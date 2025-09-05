## Releasing khx-publish-pypi ✨

### 1) Bump version
```bash
khx-publish-pypi bump patch  # or minor/major
```

### 2) Commit and tag
```bash
git add -A
git commit -m "chore: release vX.Y.Z"
git tag vX.Y.Z
```

### 3) Build
```bash
python -m build
```

### 4) Upload (TestPyPI first recommended)
```bash
twine upload -r testpypi dist/*
# verify, then
twine upload dist/*
```

### Tips
- Ensure `pyproject.toml` dynamic version points to `src/khx_publish_pypi/__version__.py`.
- Keep changelog or release notes in GitHub Releases.

---

## GitHub Actions publishing (recommended)

This repo includes a workflow at `.github/workflows/publish.yml` that:
- Builds wheels and sdist
- Publishes to PyPI when a GitHub Release is published
- Can manually publish to TestPyPI or PyPI via workflow dispatch

### One-time setup
- In your GitHub repository settings, add secrets:
  - `PYPI_API_TOKEN` → PyPI token (for uploads to pypi.org)
  - `TEST_PYPI_API_TOKEN` → TestPyPI token (for uploads to test.pypi.org)
  - Token username is always `__token__` when creating tokens on PyPI/TestPyPI.

### Publish via Release (PyPI)
1. Bump version and push tags (as above)
2. Create a GitHub Release for tag `vX.Y.Z`
3. The workflow runs, uploads `dist/*` to the Release assets, and publishes to PyPI automatically

### Manual publish (TestPyPI/PyPI)
1. Go to Actions → “Publish to PyPI”
2. Click “Run workflow” and choose target repository (`testpypi` or `pypi`)
3. Run; the workflow builds and uploads from the current default branch


