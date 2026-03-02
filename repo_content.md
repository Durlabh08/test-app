---
name: Readme Generator Beginner
model: gpt-5.2
temperature: 0.45
toolkits: elita_toolkit_task
type: github
branch: readme-gen-repo_content
---

# Repository structure

- README.md — Minimal project README. Content: "test-app / App for Elita task".
- package.json — Project metadata:
  - name: "quiz-cli"
  - version: "1.0.0"
  - description: "An interactive command-line quiz game for learning JavaScript"
  - main: "index.js"
  - type: "module"
  - scripts: "start" (node index.js), "test" (node --test)
  - engines: node >= 18.0.0
  - license: MIT
- index.js — CLI entrypoint. Responsibilities:
  - Loads questions from data/questions.json
  - Displays a banner and category/question selection UI
  - Uses src/input.js for user prompts, src/quiz.js for quiz logic, src/colors.js for terminal styling
  - Implements the main application loop with async/await and error handling
- data/questions.json — Quiz content (JSON). Categories included: "JavaScript Basics", "Node.js Fundamentals", "General Programming". Each category contains multiple questions with options, answer index, and explanation.
- src/quiz.js — Quiz class and game logic:
  - shuffle(array) helper (Fisher–Yates)
  - Quiz class with methods: askQuestion, renderProgressBar, showResults and getters for currentQuestion, totalQuestions, isComplete, progress
  - Uses colors and input.select to display questions and record answers
- src/input.js — Readline-based input helpers: createInterface, prompt, select, confirm, pressEnter. Implements a simple numeric menu selection loop.
- src/colors.js — ANSI color utilities: colorize and convenience functions (red, green, yellow, cyan, bold, dim, success, error, etc.)

# File contents needed for documentation

Below are the specific pieces of information you should include in project documentation. I do not output full file contents here — only the key values and summaries extracted from the repository.

1) package.json (include these fields):
   - name: quiz-cli
   - version: 1.0.0
   - description: An interactive command-line quiz game for learning JavaScript
   - main: index.js
   - type: module
   - scripts: start (node index.js), test (node --test)
   - engines: node >= 18.0.0
   - license: MIT

   Documentation actions:
   - Add a short "Installation" section that mentions Node.js >= 18 and how to run: `npm start` (runs node index.js).

2) index.js (usage & behavior highlights):
   - Entry point and main loop that:
     - Loads data from data/questions.json
     - Lets the user choose a category and number of questions
     - Creates a Quiz instance and iterates through questions
     - Shows results and offers to play again
   - Note: index.js uses ES modules and relies on src/input.js, src/quiz.js, src/colors.js.

3) data/questions.json (content format to document):
   - Top-level object: { "categories": { <id>: { name: string, questions: [ { question, options, answer, explanation } ] } } }
   - Explain that `answer` is the numeric index into `options` (0-based).
   - Document available categories: "javascript", "nodejs", "general" with displayed names "JavaScript Basics", "Node.js Fundamentals", "General Programming".

4) src/quiz.js (important behaviors to document):
   - The Quiz class shuffles questions, tracks currentIndex, score, and answers
   - askQuestion shows a progress bar, prompts user using select(), records correctness, shows explanations when present
   - showResults prints score, percentage, and lists incorrect answers with both user and correct options

5) src/input.js and src/colors.js (brief API):
   - input.js exports: createInterface(), prompt(rl, question), select(rl, question, options) → {index, value}, confirm(rl, question) → boolean, pressEnter(rl)
   - colors.js exports utility functions for styling console output (e.g., success, error, info, highlight)

6) Missing / recommended additions (not present in repository files):
   - A user-facing README with installation, usage examples, and contribution guidelines (current README.md is minimal)
   - CONTRIBUTING.md, CODE OF CONDUCT, and a more detailed LICENSE file (package.json lists MIT, but no separate LICENSE file is present)
   - Tests and CI configuration: package.json has a "test" script but there are no test files or test framework configuration in the repo
   - Examples of expanding questions and how to add new categories (a short doc outlining the JSON schema would help contributors)

If you'd like, I can now:
- Draft a full README.md in this branch that includes Installation, Usage, Data format for questions, and Contribution guidance.
- Create CONTRIBUTING.md and docs/QUESTIONS.md incrementally.

Notes and accuracy checks:
- All items above are derived from the repository files currently on branch 'readme-gen-repo_content'.
- I did not include full source dumps; instead I summarized key values and behaviors. If you want specific code excerpts included in documentation, specify which file and I will add small, focused snippets instead of full files.
