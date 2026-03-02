---
name: Readme Generator Beginner
model: gpt-5.2
temperature: 0.45
toolkits: elita_toolkit_task
type: github
notes: "Generated placeholder README. No repository URL or branch was provided; content is generic and includes guidance for what to extract when real repo data is available."
indexed_document_search:
  method: stepback_summary_index
  cut_off: 0.1
  search_top: 10
---

# Repository structure

NOTE: Repository URL and branch were not provided, so I could not read the actual repository contents. The README below is a template and a record of what I would store in `repo_content/README.md`. Please provide the repository URL and branch to generate a complete, code-derived README.

Expected/Template structure (placeholder):

- repo_content/
  - README.md  # this file (placeholder)
  - src/       # source code (modules, packages)
  - docs/      # documentation, design notes
  - tests/     # unit and integration tests
  - .github/   # workflows, issue templates
  - LICENSE
  - setup.py / pyproject.toml or package.json
  - requirements.txt / Pipfile / Gemfile / package-lock.json

Missing information:
- Repository URL (not provided).
- Branch name (not provided).
- File list and contents (cannot read without repository info).

If you provide the repository URL and branch, I will:
1. Read the repository tree and list files and folders precisely.
2. Extract short descriptions for key files (modules, README, config files).
3. Fill the "File contents needed for documentation" section with concrete excerpts and usage instructions derived from the code.

# File contents needed for documentation

To produce a full, accurate README for this repository I need the following files and/or information from the repo. For each item I list what I will extract and how it will be represented in the final README.

1) Project overview / README (existing)
   - Extract: project description, goals, badges, links
   - Use: populate the top-level project summary and quick start
   - Missing: original README file content

2) License
   - Extract: license name and short copy (or include LICENSE file)
   - Use: include license badge and section
   - Missing: LICENSE file

3) Setup & installation files
   - Examples: requirements.txt, pyproject.toml, package.json, Dockerfile
   - Extract: install steps, runtime requirements, build commands
   - Use: create "Setup" and "Installation" sections with exact commands
   - Missing: these files

4) Code entry points
   - Examples: src/, main modules, CLI entrypoints
   - Extract: module purpose, example usage, CLI flags, API endpoints
   - Use: Usage, Examples, API Reference sections
   - Missing: source files

5) Configuration and environment
   - Examples: .env.example, config/*.yml, settings files
   - Extract: required environment variables, default values
   - Use: Configuration section with example .env and security notes
   - Missing: config files

6) Tests
   - Examples: tests/ directory, CI workflows in .github/workflows
   - Extract: test running instructions, coverage info
   - Use: Testing and CI section
   - Missing: test files and workflows

7) Contribution guidelines
   - Examples: CONTRIBUTING.md, CODE_OF_CONDUCT.md
   - Extract: contribution process, PR guidelines, coding standards
   - Use: Contributing section
   - Missing: contributing files

8) Examples & docs
   - Examples: examples/, docs/, notebooks/
   - Extract: usage examples or demo steps
   - Use: Quickstart and Examples sections
   - Missing: example code or docs

9) Changelog, Roadmap
   - Examples: CHANGELOG.md, ROADMAP.md
   - Extract: recent changes, planned features
   - Use: Release notes / Roadmap sections
   - Missing: changelog/roadmap

# Review and completeness

This README is a placeholder generated without access to the target repository. It follows the required YAML frontmatter and includes the requested sections. It intentionally does not contain verbatim file contents from any repository because no repository was provided. Once you supply the repository URL and branch name, I will update this README with concrete repository-derived content, and will strictly avoid dumping entire file contents in chat — instead, I will store full files in `repo_content/` and include concise, relevant excerpts in the README.

# Requests / Next steps

Please provide the following so I can update this README with accurate, code-derived content:
- Repository URL (e.g. https://github.com/owner/repo)
- Branch name (e.g. main)

Optional (recommended):
- Which files or sections you want prioritized (e.g., API reference, setup, examples)

# Feedback

Please review this placeholder README and tell me:
- Are the template sections aligned with your expectations?
- Which parts should be prioritized when I inspect the real repo?
- Any internal documentation standards I should follow (formatting, licenses, templates)?

I will update the README in `repo_content/README.md` after you provide the repository URL and branch.

Thank you.
