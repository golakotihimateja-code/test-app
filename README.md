# Quiz CLI

An interactive command-line quiz game to test programming knowledge. Built with modern Node.js (ES modules) and a data-driven question format (JSON). No external dependencies — runs on Node.js >= 18.0.0.

## Table of Contents

- Introduction
- Features
- Requirements
- Installation
- Usage
- Questions Format
- Development
- Contributing
- License

## Introduction

Quiz CLI is a lightweight command-line application designed to help developers and learners test and improve their programming knowledge through short, focused quizzes. Questions are stored in JSON and the application runs directly on Node.js without extra dependencies.

## Features

- Interactive multiple-choice quizzes
- Timer and scoring options
- Support for JSON-based question banks
- Lightweight: no external dependencies (Node.js >= 18)
- Easy to extend and contribute

## Requirements

- Node.js >= 18.0.0
- A POSIX-compatible shell (macOS, Linux) or Windows Terminal/PowerShell

## Installation

1. Clone the repository:

   git clone https://github.com/golakotihimateja-code/test-app.git
   cd test-app

2. Install dependencies (if any) and run directly with Node.js. This project is designed to be dependency-free; however, use npm/yarn if additional tooling is required for development.

## Usage

Run the quiz from the project root:

   node ./bin/quiz.js

(If the project exposes an npm script, use `npm start`.)

During the quiz, you'll be presented with a question and multiple choices. Select the correct option by typing the choice number or letter and press Enter.

## Questions Format

Questions are stored in JSON format under the `data/` directory. Example structure:

{
  "title": "JavaScript Basics",
  "questions": [
    {
      "id": "q1",
      "text": "What is the output of `typeof null` in JavaScript?",
      "choices": ["'object'", "'null'", "'undefined'", "'number'"],
      "answer": 0,
      "time_limit": 30
    }
  ]
}

Fields:
- id: unique identifier for the question
- text: question text (supports inline code)
- choices: array of possible answers
- answer: index of the correct choice (0-based)
- time_limit: optional time limit in seconds for the question

## Development

- Run the CLI locally with `node ./bin/quiz.js`.
- Add new question banks under `data/` as JSON files.
- Write unit tests (if present) and follow the repository's testing conventions.

## Contributing

Contributions are welcome. Please follow these guidelines:
- Fork the repository and create a feature branch
- Add tests for new features or bug fixes
- Open a pull request describing your changes

## License

This project is open-source. Include a LICENSE file if applicable.

## Acknowledgements

Thanks to contributors and the community for improvements and feedback.