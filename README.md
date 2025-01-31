# Python Project Template
A Python project template with Ruff and Mypy settings

**Important**: Remember to `pdm add mypy` and `pdm add ruff` after virtual environment is created to use mypy and ruff. Also do `pdm add jupyterlab` if you want to use Jupyter Notebook (Web UI or in VSCode) / Jupyter Lab.

## Virtual Environment
- [PDM](https://pdm.fming.dev/latest/)

You can set up with `pdm init`, it will modify `pyproject.toml` automatically.

# VSCode/Cursor Extension

- Must-have
	- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
	- [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
	- [Python Debugger](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy)
	- [Mypy](https://marketplace.visualstudio.com/items?itemName=matangover.mypy): Compatibility better than ms-python.mypy in my experience
	- [Ruff](https://marketplace.cursorapi.com/items?itemName=charliermarsh.ruff)
	- [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- Nice to have:
	- [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring)
	- [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
	- [GitLens)(https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
	- [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)


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
