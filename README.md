# KiCAD - GitHub Integration using the Git Plugin for KiCad
This repository is designed to teach users how to effectively use GitHub for version control and project management when working with KiCad projects. It provides a step-by-step introduction to managing schematic and PCB files. Additionally, it demonstrates how to use the Kicad Git plugin to streamline collaboration, making it easier for individuals and teams to develop hardware projects.

# Installation
1. Download KiCAD from the official website.
2. Follow the installation instructions for your operating system.
3. Download and Install the Git plugin for KiCad through the Plugin and Content Manager.

## Configuration
1. Open KiCAD and open the project you'd like to use to work on the repo.
2. Initialize git in the local folder you're using and connect to GitHub.
```bash
git init
git remote add origin https://github.com/blyons-dev/KiCad-Git-Workshop.git
```
3. Switch to the current branch.
```bash
git fetch origin
git checkout -b main origin/main
```
4. Open the Schematic Editor for the next steps. If you do not see anything in the schematic editor, then restrart KiCad. If it still does not work, please ask for assistance.

# General Workflow
1. Create a new branch before making changes.
2. Open the project in KiCad.
3. Make schematic and/or PCB changes.
4. Use the KiCad Git plugin to:
  - Rescan
  - Stage changes
  - Commit changes
5. Push your branch to GitHub.
6. Create a pull request.

## Branching
- Always create a new branch before starting work.
- Suggested naming conventions:
  - feature/<description>
  - fix/<issue>
  - <firstinitial>_<lastname>
Branching allows multiple contributors to work without affecting the main project.

## Pull Requests
A pull request is used to merge your changes into the main branch.
### Creating a Pull Request
1. Push your branch to GitHub using the Git plugin.
2. Navigate to the repository on GitHub.
3. Click "Compare & Pull Request".
4. Add a title and description of your changes.
5. Submit the pull request.
### Pull Request Guidelines
- Clearly describe what changes were made.
- Explain why the changes were necessary.
- Include any notes that may help reviewers.

# Common Issues
## Setup Issues
### KiCad opens but no project files appear
- Ensure you opened the cloned repository files.
### Git commands not working
- Verify Git is installed:
```bash
git --version
```
### Remote already exists
```bash
git remote remove origin
git remote add origin <repo-url>
```
## KiCad Plugin Issues
### Git plugin not visible
- Install via Plugin and Content Manager and restart KiCad.
- It is only visible in the Layout Editor, so make sure you navigate there before looking for it.
### Changes not appearing in plugin
- Save files before rescanning.
- Click "Rescan" in the plugin.
### Schematic appears blank
- Restart KiCad
- Verify the correct project directory is open.
## Git Workflow Issues
### Changes not showing as staged
- Click "Rescan"
- Check if files are excluded by .gitignore.
### What does staging mean?
- Staging selects files to include in the next commit.
### Why create a branch?
- Prevents breaking the main branch and supports collaboration.
## Merge and Conflict Issues
### Merge conflicts
- The KiCad Git plugin will not allow you to push if your local branch is not up to date, this prevents merge conflicts on the branch but could create conflicts in your local files.
- Occur when multiple users edit the same file.
- Resolve by reviewing and manually fixing differences.
### Files appear broken after pulling
- May be caused by conflicts or version mismatches.
## Push Issues
### Push failed or permission denied
- Ensure you are authenticated with GitHub.
- Setup your User Name and Email in the Git plugin by navigating to Edit->Options.
### Branch not visible on GitHub
- Set upstream branch:
```bash
git push -u origin <branch-name>
```
## Pull Request Issues
### Cannot create a pull request
- Ensure the branch has been pushed to GitHub.
### Cannot merge pull request
- May be due to conflicts or missing permissions.
### Changes requested on pull request
- Make updates locally, commit, and push again.
### Should branches by deleted after merging?
- Recommended, but optional.
## KiCad-Specific Notes
- KiCad files are text-based and may show many small changes.
- Avoid multiple users editing the same file simultaneously, use branches.
- Git diffs may be difficult to read; the plugin helps visualize changes.

# Version Information

- KiCAD Version: 9.0
- Last Updated: 2026-04-01

This repository was developed in KiCad 9.0 for compatibility reasons to ensure those who have not update to 10.0 can still open the files without issue. Generally, ensure that KiCad and all libraries are kept up to date for compatibility and stability.
