# KiCAD - GitHub Integration using the Git Plugin for KiCad
This repository is designed to teach users how to effectively use GitHub for version control and project management when working with KiCad projects. It provides a step-by-step introduction to managing schematic and PCB files. Additionally, it demonstrates how to use the Kicad Git plugin to streamline collaboration, making it easier for individuals and teams to develop hardware projects.

## Installation
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
3. Switch to the current branch (replace current-branch with the branch name).
```bash
git fetch origin
git checkout -b main origin/main
```
4. Open the Schematic Editor for the next steps. If you do not see anything in the schematic editor, then restrart KiCad. If it still does not work, please ask for assistance.

# Version Information

- KiCAD Version: 9.0
- Last Updated: 2026-04-01

Ensure to keep your KiCAD and all libraries updated to the latest stable versions for compatibility and access to new features.
