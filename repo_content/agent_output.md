---
name: Readme Generator Beginner
model: gpt-5.2
temperature: 0.45
toolkits: elita_toolkit_task
type: github
config:
  stepback_summary_index:
    cut_off: 0.1
    search_top: 10
---

# Repository structure

- Note: No GitHub repository URL or branch name was provided. I could not access or read the repository structure.
- To proceed, please provide the repository URL and branch name so I can list files and read specific files.

If you provide the repository and branch, I will:
- List the repository structure (top-level directories and files)
- Identify files relevant for documentation (README, package.json, setup.py, pyproject.toml, LICENSE, docs/, src/ etc.)
- Read file snippets as needed (in chunks if large)


# File contents needed for documentation

Below is a checklist of files and contents I need to generate a complete README. Mark which ones exist or provide them, and I will extract the necessary details.

- Project overview / README (existing): short description, goals, features
- Installation instructions:
  - package manager files (package.json, requirements.txt, pyproject.toml, setup.py)
  - build or install steps
- Usage examples:
  - example commands, API usage, CLI examples
- Configuration / Environment variables:
  - .env.example, config files, or documented env vars
- Contribution guidelines:
  - CONTRIBUTING.md, code of conduct
- License (LICENSE file)
- Tests (tests/ directory, instructions to run)
- CI config (GitHub Actions workflow files in .github/workflows)
- Source code entry points:
  - src/ or main package, and brief descriptions of modules
- Changelog or Releases

Notes on missing information
- Because no repository was provided, I could not derive any content from source files. Please provide the repository URL and branch name.

Next steps
1. Provide repository URL and branch name (for example: https://github.com/owner/repo and branch: main).
2. I will list the repository structure and read key files in chunks.
3. I will generate a README draft based strictly on the repository contents and store the output under repo_content/.

---

Indexed Document Search

When questions relate to indexed documents in the attachment bucket, I will use the stepback_summary_index tool with the parameters above (cut_off=0.1, search_top=10) to retrieve and summarize relevant documents.

Handling files

- I will follow the incremental write rules for creating/modifying files in the repository: create initial skeleton, then append or edit in small focused updates.
- For large files I will read in chunks and avoid dumping full contents in chat.

Context limitations

- If the repository is large, I will work file-by-file and summarize findings to avoid context overload.


Stored-by-agent: This message has been saved to repo_content/agent_output.md
