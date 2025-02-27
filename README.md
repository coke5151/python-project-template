# Python Project Template
A Python project template with Ruff and Mypy settings

**Important**: Remember to `pdm update` after virtual environment created to install the template default dependencies like ruff, mypy, jupyterlab, etc.

## Virtual Environment
This template uses [PDM](https://pdm.fming.dev/latest/) as project manager.

You can also use [uv](https://github.com/astral-sh/uv) as resolver and installer. uv (built in rust) is much faster than PDM's default resolver.

## Setup Steps
1. Install PDM and [uv](https://github.com/astral-sh/uv) (Optional) in your system.
2. (Optional) Enable uv as resolver and installer:
   `pdm config use_uv true`
3. Run `pdm init`, it will modify `pyproject.toml` automatically.
4. Run `pdm update` to install and update the template default dependencies.

[How to use uv as resolver and installer of PDM](https://pdm-project.org/en/latest/usage/uv/)

## PDM Usage
- `pdm add <package>`: Add new package to default dependency group.
- `pdm add -d <package>`: Add new package to dev dependency group.
- `pdm remove <package>`: Remove package (and unused dependencies) in default dependency group.
- `pdm remove -d <package>`: Remove package (and unused dependencies) in dev dependency group.
- `pdm run <script>`: Run a command. For example, `pdm run src/main.py` to run the specified script with the virtual environment.
- `pdm run <command>`: Run a command. For example, `pdm run ruff check` to run ruff check with the virtual environment. It's the same as `ruff check` in terminal with activated virtual environment.

## PDM Scripts
You can also add/edit custom scripts in `pyproject.toml` file.

- `pdm run main`: Run the main script in `src/main.py` (==`pdm run python src/man.py`)
- `pdm run lab`: Run jupyter lab. (==`pdm run jupyter lab`)


# Recommanded VSCode/Cursor Extension
- Must-have
	- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
	- [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
	- [Python Debugger](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy)
	- [Mypy (by Matan Gover)](https://marketplace.visualstudio.com/items?itemName=matangover.mypy): Compatibility better than [ms-python.mypy](https://marketplace.visualstudio.com/items?itemName=ms-python.mypy-type-checker) in my experience
	- [Ruff](https://marketplace.cursorapi.com/items?itemName=charliermarsh.ruff)
	- [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- Nice to have:
	- [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring)
	- [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
	- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
	- [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)


## VSCode Settings
For better experience, you can add the following settings to your personal `settings.json`: (already added in this project)

```json
{
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
  "mypy.runUsingActiveInterpreter": true,
  "mypy.checkNotebooks": true
}
```
