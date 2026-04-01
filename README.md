# KiCAD Setup

## Installation
1. Download KiCAD from the official website.
2. Follow the installation instructions for your operating system.
3. Download and Install the Git plugin for KiCad through the Plugin and Content Manager.

## Configuration
1. Open KiCAD and open the project you'd like to use to work on the repo.
2. Initialize git in the local folder you're using and connect to GitHub.
```bash
git init
git remote add origin https://github.com/blyons-dev/BLDC-Drone.git
```
3. Switch to the current branch (replace current-branch with the branch name).
```bash
git fetch origin
git checkout -b current-branch origin/current-branch
```
4. Configure git to track the right branch.
```bash
git branch --set-upstream-to=origin/current-branch current-branch
```
4a. Optional. Verify you're on the right branch.
```bash
git branch -v
```
5. The plugin in KiCad can only be accessed in the Layout Editor, so navigate there. The plugin will automatically detect any Unstaged Changes that you have made, you just need to verify that by clicking **Rescan**.
6. Click the **Stage Changed** button to prepare everything for a commit
7. Write in the Commit Message a description of what you changed and click the **Sign Off** button as well.
8. Click **Commit** and then **Push** to send everything to the online repo.

# Project Structure

The entire project folder will be dumped here, so any resources used in the project (like custom symbols or footprints, which will be saved in project libraries) will be saved here as well.

# Version Information

- KiCAD Version: 10.0
- Last Updated: 2026-03-25

Ensure to keep your KiCAD and all libraries updated to the latest stable versions for compatibility and access to new features.
