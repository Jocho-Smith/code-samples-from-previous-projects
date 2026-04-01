# Testing & Development

pytest
- preferred over `unittest`
- https://docs.pytest.org/ has everything
- favorites: `--pdb`, `--lf`

Debugging  
- I usually start with print debugging, then move to pdb if I'm stuck
- `pdb` built-in minimal test: `import pdb; pdb.set_trace()`
- VSCode debugger is nicer for bigger projects, proper watch variables etc.
- fast logging bootstrap with loguru: https://github.com/Delgan/loguru

nox
- like tox but with actual Python instead of ini files
- run tests across multiple Python versions without manually managing virtualenvs
- inspired by https://github.com/Advanced-Machine-Learning-UBonn
- mostly use it for libraries where I care about 3.9-3.12 compatibility
- my default for test-driven development setup using github-runner

VSCode Workflows
- "Go to Definition" (F12) and "Find All References" are my most-used shortcuts
- helps trace through unfamiliar codebases super fast
- multi-cursor editing (Ctrl+D) for quick refactors
- watch this before diving in: https://www.youtube.com/watch?v=jqHXJ3O7WG
- Remote SSH extension is a game-changer for working on clusters

MVC Pattern
- mostly use it for CLI tools to keep commands/logic/output separate
- Explicit code example: https://github.com/Jocho-Smith/CLI-todo-app--typer
- makes testing way easier since you're not testing UI and logic together
- overkill for tiny scripts, but scales nicely