---
name: python-project
description: Creates a new Python project with a virtual environment and installs requests.
---

# Python Project

Use this when the user asks to create or scaffold a new Python project. Run these commands in order:

```bash
mkdir {project}
cd {project}
python -m venv venv
source venv/bin/activate
pip install requests
```
