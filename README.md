# `survey` (Evaluation function)

An Evaluation Function to call when using Lambda Feedback response areas to survey users.

Returns `is_correct = True` by default.

Returns a default feedback message if no custom feedback.

Returns custom feedback message if provided.

## Repository Structure

```bash
app/
    __init__.py
    evaluation.py # Script containing the main evaluation_function
    preview.py # Script containing the preview_function
    docs.md # Documentation page for this function (required)
    evaluation_tests.py # Unittests for the main evaluation_function
    preview_tests.py # Unittests for the preview_function
    requirements.txt # list of packages needed for algorithm.py
    Dockerfile # for building whole image to deploy to AWS

.github/
    workflows/
        test-and-deploy.yml # Testing and deployment pipeline

config.json # Specify the name of the evaluation function in this file
.gitignore
```

### GitHub Actions

Whenever a commit is made to the GitHub repository, the new code will go through a pipeline, where it will be tested for syntax errors and code coverage. The pipeline used is called **GitHub Actions** and the scripts for these can be found in `.github/workflows/`.

On top of that, when starting a new evaluation function, you will have to complete a set of unit test scripts, which not only make sure your code is reliable, but also helps you to build a _specification_ for how the code should function before you start programming.

Once the code passes all these tests, it will then be uploaded to AWS and will be deployed and ready to go in only a few minutes.

## Pre-requisites

Although all programming can be done through the GitHub interface, it is recommended you do this locally on your machine. To do this, you must have installed:

- Python 3.8 or higher.

- GitHub Desktop or the `git` CLI.

- A code editor such as Atom, VS Code, or Sublime.

Copy this template over by clicking **Use this template** button found in the repository on GitHub. Save it to the `lambda-feedback` Organisation.
