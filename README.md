# Python Project Template
A Python project template with Ruff and Mypy settings

**Important**: Remember to `pdm add mypy` and `pdm add ruff` after virtual environment is created to use mypy and ruff.

## Virtual Environment
- [PDM](https://pdm.fming.dev/latest/)

You can set up with `pdm init`, it will modify `pyproject.toml` automatically.

# VSCode/Cursor Extension
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
- [Python Debugger](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy)
- [Mypy](https://marketplace.visualstudio.com/items?itemName=matangover.mypy)：Compatibility better than ms-python.mypy in my experience
- [Ruff](https://marketplace.cursorapi.com/items?itemName=charliermarsh.ruff)

## VSCode Settings
For better experience, you can add the following settings to your personal `settings.json`: (already added in this project)

```json
"[python]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "charliermarsh.ruff",
    "editor.codeActionsOnSave": {
      "source.fixAll": "always",
      "source.organizeImports": "always"
    }
  },
"python.analysis.inlayHints.variableTypes": true,
"python.analysis.inlayHints.pytestParameters": true,
"python.analysis.inlayHints.functionReturnTypes": true,
"python.analysis.inlayHints.callArgumentNames": "all",
"python.analysis.extraPaths": ["./.venv/Lib/site-packages"],
"python.analysis.autoFormatStrings": true,
"python.analysis.typeCheckingMode": "basic",
"python.analysis.autoImportCompletions": true,
```

## Default Scripts
- `pdm run main`: Run the main script in `src/main.py`
