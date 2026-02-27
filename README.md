# gh-actions-pycicd-walk

[![Python CI/CD Pipeline](https://github.com/andryhialy/gh-actions-pycicd-walk/actions/workflows/python-pipeline.yml/badge.svg)](https://github.com/andryhialy/gh-actions-pycicd-walk/actions/workflows/python-pipeline.yml)

A simple repository demonstrating a Python CI/CD workflow using GitHub Actions.

## Contents

- `hello.py` - a trivial script that prints "Hello, world!".
- `.github/workflows/python-pipeline.yml` - GitHub Actions pipeline that lints, tests, builds a Docker image, pushes it to GitHub Container Registry and pulls it back for verification.

## Usage

1. Clone the repository.
2. Run `python hello.py` to see the greeting.
3. Push changes to trigger the workflow badge above.

## Workflow

The pipeline consists of three jobs:

1. **lint-and-test** – install flake8 & pylint, lint the script, run a basic execution test.
2. **build-and-push** – build a multi-arch Docker image and push to GHCR.
3. **test-image** – pull the just-built image and execute it to confirm output.

## License

MIT © 2026
