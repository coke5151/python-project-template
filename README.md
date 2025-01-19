# Python Project Template
A Python project template with Ruff and Mypy settings

## Recommended Virtual Environment
- [PDM](https://pdm.fming.dev/latest/)

You can set up with `pdm init`, it will modify `pyproject.toml` automatically.

## VSCode Settings

For better experience, you can add the following settings to your `settings.json`:

```json
"[python]": {
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "source.fixAll": true,
        "source.organizeImports": true
    },
    "editor.defaultFormatter": "charliermarsh.ruff"
},
"python.analysis.inlayHints.variableTypes": true,
"python.analysis.inlayHints.pytestParameters": true,
"python.analysis.inlayHints.functionReturnTypes": true,
"python.analysis.inlayHints.callArgumentNames": "all",
"python.analysis.autoImportCompletions": true,
"python.analysis.extraPaths": ["./.venv/Lib/site-packages"]
```

## Scripts

- `pdm run main`: Run the main script in `src/main.py`
