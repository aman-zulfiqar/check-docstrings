# 🧪 check-docstrings

**check-docstrings** is a static code analysis tool that scans Python files to ensure all public API endpoint functions include proper docstrings. It enforces code documentation best practices, especially for longer functions or those exposed via decorators like `@get`, `@post`, etc.

## 🚀 Features

- Detects **missing docstrings** in public functions and API endpoints
- Supports both `async` and `sync` methods
- Ignores private methods (those starting with `_`)
- Skips functions that already have docstrings
- Configurable method length threshold via CLI
- Designed to integrate with **pre-commit** hooks

## 🛠️ Usage

```bash
python check_docstrings.py [--length LENGTH] <filename1> <filename2> ...
CLI Arguments
Flag	Description	Default
--length	Minimum lines of code to trigger check	6

Example
bash
Copy
Edit
python check_docstrings.py --length 8 app/routes.py
If any public API function is missing a docstring, you'll see:

bash
Copy
Edit
app/routes.py:42 missing docstring.
✅ Use Case
This tool is perfect for:

API-based projects (e.g., FastAPI, Flask)

Teams enforcing docstring coverage

Pre-commit hook pipelines
