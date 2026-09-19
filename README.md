# foreman

Inspired by https://github.com/kunchenguid/firstmate/

Firstmate is amazing, but honestly it does way more than what I need it for.

So this is a smaller & opinionated version for use with herdr and optimizing for speed & token efficiency.

## Setup

```sh
cd
git clone git@github.com:khooeee/foreman.git
```

Add Foreman's helpers to PATH for your shell:

```sh
# Bash
echo 'export PATH=~/foreman/bin:$PATH' >> ~/.bashrc

# Zsh
echo 'export PATH=~/foreman/bin:$PATH' >> ~/.zshrc
```

Add `TERMINOLOGY.md` if you have terms that refer to some aspect of your project (i.e. basically a shortcut for a project subdirectory).

## Espanso matches

Prompts I often use that I've abbreviated to Espanso matches:

```yaml
matches:
  - trigger: ";hlt"
    replace: "What high level tasks have you completed, and what are you working on right now?"
```

## Default Conventions

- Any requested code change will open a PR immediately, and any related changes will commit and push to the PR immediately.
- When a PR is merged or closed, it will delete all worktrees & branches immediately. It will also fast forward the default branch to latest.

Licensed under the [MIT License](LICENSE).
