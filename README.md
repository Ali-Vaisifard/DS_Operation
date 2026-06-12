# README.md

````md
# DS_Operation - UV & Python Environment Setup

This project documents the commands and steps used to set up a Python development environment using `uv`, virtual environments, Jupyter, and package installation inside GitHub Codespaces.

---

## 1. Check Python Version

```bash
python --version
````

Output:

```bash
Python 3.12.1
```

---

## 2. Install `uv`

### Wrong Package Name

```bash
pip install uvb
```

Error:

```bash
ERROR: Could not find a version that satisfies the requirement uvb
```

### Correct Installation

```bash
pip install uv
```

Successful installation:

```bash
Successfully installed uv-0.11.16
```

---

## 3. Initialize UV Project

```bash
uv init
```

Output:

```bash
Initialized project `ds-operation`
```

---

## 4. Incorrect Command Attempt

```bash
init uv
```

Error:

```bash
Couldn't find an alternative telinit implementation to spawn.
```

---

## 5. Create Virtual Environment

```bash
uv venv --python 3.11 --seed
```

Notes:

* Uses Python 3.11.15
* Warning about Python version mismatch because project requires Python >=3.12

Activate environment:

```bash
source .venv/bin/activate
```

---

## 6. Verify Python Version Inside Environment

```bash
python -V
```

Output:

```bash
Python 3.11.15
```

---

## 7. Incorrect UV Python Command

```bash
uv python -V
```

Error:

```bash
error: unexpected argument '-V' found
```

---

## 8. Incorrect UV Subcommand

```bash
uv python3 --version
```

Error:

```bash
error: unrecognized subcommand 'python3'
```

---

## 9. Correct Way to Run Python with UV

```bash
uv run python3 --version
```

Output:

```bash
Python 3.12.1
```

---

## 10. Remove Existing Virtual Environment

```bash
rm -rf .venv
```

---

## 11. Recreate Virtual Environment

```bash
uv venv --python 3.11 --seed
```

Activate again:

```bash
source .venv/bin/activate
```

---

## 12. Install Packages

### Wrong Package Name

```bash
uv pip install pandas juoter ipykernel
```

Error:

```bash
Because juoter was not found in the package registry
```

### Correct Installation

```bash
uv pip install pandas jupyter ipykernel
```

Installed successfully:

* pandas
* jupyter
* ipykernel
* notebook
* numpy
* matplotlib-inline
* ipython
* jupyterlab
* and many dependencies

---

## 13. Create Project Folder

```bash
mkdir aap
```

---

## 14. Navigate to App Directory

### Incorrect Directory

```bash
cd app
```

Error:

```bash
No such file or directory
```

### Correct Navigation

```bash
cd app
```

---

## 15. Attempt to Open Notebook Incorrectly

```bash
notebook.ipynb
```

Error:

```bash
command not found
```

---

## 16. Create Notebook File

```bash
touch notebook.ipynb
```

---

## 17. Activate Virtual Environment from App Directory

```bash
source /workspaces/DS_Operation/.venv/bin/activate
```

---

# Useful Commands Summary

## Create Virtual Environment

```bash
uv venv --python 3.11 --seed
```

## Activate Environment

```bash
source .venv/bin/activate
```

## Install Packages

```bash
uv pip install pandas jupyter ipykernel
```

## Run Python

```bash
python -V
```

## Run Python with UV

```bash
uv run python3 --version
```

## Create Jupyter Notebook

```bash
touch notebook.ipynb
```

---

# Notes

* `uv` is a fast Python package and environment manager.
* Always verify package names before installation.
* Activate the virtual environment before installing packages.
* Use `jupyter` instead of `juoter`.
* Ensure directories exist before using `cd`.

---

# Author

Ali Vaisifard

```

Based on the terminal history you shared. :contentReference[oaicite:0]{index=0}
```
