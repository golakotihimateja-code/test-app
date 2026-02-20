# Quiz CLI

An interactive command-line quiz game for learning JavaScript. This repository provides a small Node.js (ES modules) CLI app that loads a JSON question bank and runs an interactive quiz session from the terminal.

![Node.js](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen) ![License: MIT](https://img.shields.io/badge/license-MIT-blue)

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Features](#features)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Installation

Requirements
- Node.js >= 18.0.0

Steps
1. Clone the repository:
   git clone https://github.com/golakotihimateja-code/test-app.git
2. Change directory into the app:
   cd test-app/test-app
3. Install dependencies (if any are declared in package.json):
   npm install

Note: The project is implemented as an ES module (package.json contains "type": "module") and is intended to run with Node 18+.

## Usage

Start the quiz from the project folder:

- Using npm script:
  npm start

- Directly with node:
  node index.js

The CLI will load questions from `data/questions.json` and guide you through an interactive quiz in the terminal. Questions are organized by category (javascript, nodejs, general). Follow on-screen prompts to select categories and answer questions.

Example:
- Run `npm start`
- Select a category when prompted (if category selection is offered)
- Answer each question by typing the option number/letter or following the prompt instructions
- At the end, view your score and optionally restart

## Project Structure

- README.md — This file
- test-app/
  - index.js — CLI entrypoint with shebang; loads questions and starts the interactive loop
  - package.json — Project metadata (name: `quiz-cli`, version: `1.0.0`, description: "An interactive command-line quiz game for learning JavaScript", type: `module`, engines: Node >=18.0.0)
  - data/
    - questions.json — JSON question bank (categories: javascript, nodejs, general; ~5 questions each)
  - src/
    - colors.js — Small helper for terminal colors/styles
    - input.js — CLI input handling utilities
    - quiz.js — Quiz class and logic that runs the question flow and scoring

## Features

- Interactive command-line quiz experience
- Categorized question bank (javascript, nodejs, general)
- Lightweight ES module implementation
- Small helper library for input and terminal colors
- Easy to extend by editing `data/questions.json` or `src/quiz.js`

## Development

Run the application locally:
- npm start or node index.js (from test-app directory)

Testing:
- package.json includes a `test` script placeholder. There are no tests included in the repository currently. To add tests:
  - Add a test framework (e.g., Jest) to devDependencies
  - Implement test files under a `tests/` folder
  - Update the `test` script in package.json

Linting:
- No linter is configured. Recommended:
  - Add ESLint for code quality: npm install --save-dev eslint
  - Configure `.eslintrc.cjs/.json` and add a `lint` script in package.json

Tips for development:
- Update `data/questions.json` to add or edit questions
- Extend `src/quiz.js` to support additional question types or scoring rules

## Contributing

Contributions are welcome. Suggested workflow:
1. Fork the repository
2. Create a feature branch (git checkout -b feat/my-feature)
3. Make changes and add tests if applicable
4. Submit a pull request describing your changes

Please include:
- Clear description of the change
- Any setup steps to exercise the change
- Tests or manual verification instructions where applicable

Recommended additional repository files to add:
- LICENSE (the package.json license is MIT — consider adding a LICENSE file)
- CONTRIBUTING.md with contribution and code style guidelines
- Tests and CI workflow (e.g., GitHub Actions) to run tests and linting

## License

This project is licensed under the MIT License (see package.json). Consider adding a top-level LICENSE file with the full MIT text.

## Acknowledgements

- Built as a simple educational CLI for learning JavaScript and Node concepts
- Inspired by many small terminal-based learning tools and quizzes