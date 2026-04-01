# Software Engineering

SOLID Principles
- good post: https://realpython.com/solid-principles-python/
- I use this whenever OOP is appropriate for the project
- especially useful once a project grows beyond "just a script"

Using `typing.Protocol`
- good official docs: https://typing.python.org/en/latest/spec/protocol.html
- I prefer it over inheritance when I just care about behavior, not hierarchy

Project Layouts
- for data science I orient myself on https://cookiecutter-data-science.drivendata.org/
- for backend stuff I keep it simple: `src/`, `tests/`, maybe `scripts/`
- I try not to overengineer early, structure usually evolves with the project

Testing:
- critical paths > 100% coverage

Tooling:
- formatter: `black`, linter: `ruff`, type checking: `mypy` (lightweight setup)
- pre-commit hooks to automate all that