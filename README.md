# foreman

Inspired by https://github.com/kunchenguid/firstmate/

Firstmate is amazing, but honestly it does way more than what I need it for.

So this is a smaller & opinionated version for use with herdr and optimizing for speed & token efficiency.

## Conventions

- Any requested code change will open a PR immediately, and any related changes will commit and push to the PR immediately.

## Setup

Add Foreman's helpers to PATH for your shell:

```sh
# Bash
echo 'export PATH=~/foreman/bin:$PATH' >> ~/.bashrc

# Zsh
echo 'export PATH=~/foreman/bin:$PATH' >> ~/.zshrc
```

Run the command for your shell, then open a new terminal. Use `>>` to append
without replacing existing configuration; single quotes keep `$PATH` literal.

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
