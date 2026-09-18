# foreman

Inspired by https://github.com/kunchenguid/firstmate/

Firstmate is amazing, but honestly it does way more than what I need it for.

So this is a smaller & opinionated version for use with herdr and optimizing for speed & token efficiency.

## Conventions

- Any requested code change will open a PR immediately, and any related changes will commit and push to the PR immediately.

## Setup

For Bash or Zsh, add Foreman's helpers to your current shell's PATH:

```sh
export PATH=~/foreman/bin:$PATH
```

For persistence, add the same line to `~/.bashrc` (Bash) or `~/.zshrc` (Zsh).

Run `foreman-branches` from any directory to show an alphabetically sorted
project/branch table. It discovers immediate directories in `~/foreman/projects`
(including symlinks), marks detached HEADs with their commit, and labels
non-repository directories. No project registry is needed.

Add `TERMINOLOGY.md` if you have terms that refer to some aspect of your project (i.e. basically a shortcut for a project subdirectory).

## Espanso matches

Prompts I often use that I've abbreviated to Espanso matches:

```yaml
matches:
  - trigger: ";hlt"
    replace: "What high level tasks have you completed, and what are you working on right now?"
```

Licensed under the [MIT License](LICENSE).
