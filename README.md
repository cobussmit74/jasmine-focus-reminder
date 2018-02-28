# jasmine-focus-reminder
A git pre-commit hook that prevents users from committing any jasmine tests that are focused.

This Git hook will scan all *\*spec.js* files and check for any focused Jasmine tests. Commit will not be allowed whilst any tests are focused.

## Installation
1. Copy the *pre-commit* file into the */.get/hooks/* folder of your local repository.
2. Remove the *pre-commit.sample* file if it exists.
3. Configure the *sourceFolder* and *testFilesEndWith* variables at the top of the script to match your project.
4. Laugh out load at the peasants who still accidently commit focused tests!

## Usage
The *pre-commit* script will be executed automatically everytime the ```git commit``` command is run. Commits will be cancelled if any focused tests are found and the script will also print the file paths of offending files.

## Bypassing
Running the commit command with the *--no-verify* argument will not run the *pre-commit* script.
```
git commit --no-verify
```
