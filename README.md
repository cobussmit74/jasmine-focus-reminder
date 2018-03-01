# jasmine-focus-reminder
A git pre-commit hook that prevents developers from committing any jasmine tests that are focused.

This Git hook will scan all *\*spec.js* files and check for any focused Jasmine tests. Commit will not be allowed whilst any tests are focused.

## Prerequisites
- Python3 (remember to add Python to your PATH)

[Python Downloads](https://www.python.org/downloads/)

## Installation
1. Copy the *pre-commit* file into the */.git/hooks/* folder of your local repository.
2. Remove the *pre-commit.sample* file if it exists.
3. Configure the *sourceFolder* and *testFilesEndWith* variables at the top of the script to match your project structure.
   By default the script will scan the *./source/* folder looking for files ending with *spec.js* / *specs.js*
4. Laugh out load at the peasants who still accidently commit focused tests!

## Usage
The *pre-commit* script will be executed automatically everytime the ```git commit``` command is run. Commits will be cancelled if any focused tests are found and the script will also print the file paths of offending files.

## Bypassing
Running the commit command with the *--no-verify* argument will not run the *pre-commit* script.
```
git commit --no-verify
```
