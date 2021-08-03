# PyRef


## Description
PyRef is a tool that automatically detect mainly method-level refactoring operations in Python projects.

Current supported refactoring operations:
* Rename Method
* Add Parameter
* Remove Parameter
* Change/Rename Parameter
* Extract Method
* Inline Method
* Move Method
* Pull Up Method
* Push Down Method

## Usage

Clone a repository from GitHub using PyRef:

```sh
python3 main.py repoClone -u "username" -r "Repo Name"
```

You can also use git command to clone the repository.

Extract refactorings from a given repository

```sh
python3 main.py getrefs -r "[PATH_TO_REPOSITORY]"
```

If you want to look into specific commit, you can use flag *-c*.
If you want to look into specific directory, you can use flag *-d*.

```sh
python3 main.py getrefs -r "[PATH_TO_REPOSITORY]" -c "[CommitHash]" -d "[Directory]"
```

The detected refactorings will be recorded in the current folder as a json file "[project]_data.json".

## Play with PyRef
You will need to first install the third-party dependencies. You can use the following command in the folder of PyRef:

```sh
pip3 install -r requirements.txt
```

We provide a toy project for you to test PyRef, which can be found at https://github.com/PyRef/DummyRef
Please execute the following commands in order:

```sh
python3 main.py repoClone -u "PyRef" -r "DummyRef"
python3 main.py getrefs -r "Repos/DummyRef"
```

The detected refactorings can be found in the file "DummyRef_data.json"

## Dataset for the Paper

The labeled oracle used in the paper can be found in the file "data/dataset.csv".