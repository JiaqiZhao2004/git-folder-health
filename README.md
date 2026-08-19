# git-folder-health

A tiny terminal status display for a directory full of Git repositories. It checks each **direct subfolder** every 30 seconds and continually redraws one line without printing a trailing newline.

```text
CLEAN  4/4 repositories healthy
```

A repository is healthy only when it:

- is a Git work tree;
- has no tracked or untracked changes;
- has an upstream remote that can be fetched; and
- is neither ahead of nor behind that upstream.

## Usage

```bash
./git-folder-health /path/to/projects
```

Press `Ctrl-C` to stop it. Set `NO_COLOR=1` to turn off the terminal color treatment.

The tool intentionally considers only immediate child directories, making it suitable for a folder that directly contains your checked-out projects.

## Install (optional)

```bash
install -m 755 git-folder-health ~/.local/bin/git-folder-health
git-folder-health /path/to/projects
```
