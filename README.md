# pygitflow

[![PyPI version](https://badge.fury.io/py/pygitflow.svg)](https://badge.fury.io/py/pygitflow)  
A lightweight, experimental CLI tool to simplify Git workflows, crafted out of necessity for developers(especially me ;).

---

## 🚀 Features

`pygitflow` is a developer-focused Git CLI tool designed to streamline common Git operations while maintaining flexibility.  

- **Branch Management**  
  - Create branches for features, hotfixes, enhancements, and more.
  - Automatically fetch and switch to the base branch before creating a new one.

- **Commit with Standards**  
  - Helps you write commits that follow standardized conventions.

- **Merging Simplified**  
  - Merge your current branch into another effortlessly, with options to stash changes dynamically.

- **Interactive Workflows**  
  - Fully interactive CLI with dynamic prompts for missing information.

---

## ⚠️ Experimental Status

This (new) tool is in its **experimental phase** and was built out of the need for a personal Git helper. Use at your own discretion, and report issues or suggest features if you find it helpful.

---

## 📥 Installation

You can install `pygitflow` via pip:

```bash
pip install pygitflow
```

Can be used via cli with alias `gflow` as well (`gflow new-branch`):

---

## 🛠️ Usage

### General Usage

```bash
pygitflow [COMMAND]
```

### Available Commands

#### 1. Create a New Branch

```bash
pygitflow new-branch
```

Interactive flow for creating a branch:
- Select the branch type: Feature, Hotfix, Enhancement, etc.
- Specify a branch name.
- Automatically fetches the latest base branch (default: `master`) before creating the new branch.

#### 2. Commit Changes

```bash
pygitflow commit
```

Helps you create standardized commit messages:
- Select the commit type: `feat`, `fix`, `docs`, etc.
- Provide a concise summary for the commit.

#### 3. Merge Branches

```bash
pygitflow merge [TARGET_BRANCH]
```

Merge the current branch into a target branch:
- Automatically checks for uncommitted changes and stashes them if required.
- Provides a list of recent branches to choose from if no target branch is specified (default: `master`).

---

## 💡 Examples

### Creating a New Branch

```bash
pygitflow new-branch
```

Example Interaction:
```
Select the branch type:
1. Feature
2. Hotfix
3. Enhancement
4. Bugfix
Enter Branch Type number [1/2/3/4]: 1
Enter branch name (without spaces): feature_x
```

### Committing Changes

```bash
pygitflow commit
```

Example Interaction:
```
Select the type of commit:
1. feat: A new feature
2. fix: A bug fix
3. docs: Documentation changes
Enter Commit Type number [1/2/3]: 1
Enter a concise summary of your changes: Added login functionality
```

### Merging Branches

```bash
pygitflow merge
```

Example Interaction:
```
Recent branches:
1. feature/login
2. bugfix/ui-fix
3. enhancement/readme-update
...
10. hotfix/payment-bug
11. master (default)

Select the target branch by number or enter branch name [11]: 1
Warning: Uncommitted changes detected in the working directory.
Do you want to stash the changes? (yes/no) [yes]: yes
Stashing uncommitted changes...
Switching to target branch 'feature/login'...
Merging branch 'main' into 'feature/login'...
Successfully merged 'main' into 'feature/login'.
```

---

## 🧰 Dependencies

- [Click](https://click.palletsprojects.com): Command-line interface library.
- [GitPython](https://gitpython.readthedocs.io): Python library for interacting with Git repositories.
- [Rich](https://rich.readthedocs.io): Beautiful CLI formatting and styling.

---

## 🤝 Contributions

Since `pygitflow` is experimental, contributions, feature suggestions, and issue reports are highly welcome. Fork this repository and submit a pull request to improve the tool.

---

## 🏗️ Built With

- **Python 3.11+**
- **Some Love**

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⚡ Acknowledgments

`pygitflow` was created out of a need for simplifying repetitive Git tasks and improving efficiency in workflows. Inspired by the challenges faced during development, this tool is a handy companion for developers who work extensively with Git.
