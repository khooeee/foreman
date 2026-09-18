# foreman

Inspired by https://github.com/kunchenguid/firstmate/

Firstmate is amazing, but honestly it does way more than what I need it for.

So this is a smaller & opinionated version for use with herdr and optimizing for speed & token efficiency.

## Conventions

- Any requested code change will open a PR immediately, and any related changes will commit and push to the PR immediately.

## Setup

With Foreman installed at `~/foreman`, add its helpers to your shell's PATH.
Run the block for your shell; it persists the setting and applies it to the
current shell. Re-running it does not add duplicate startup lines or PATH entries.

Bash (`~/.bashrc`):

```bash
foreman_path_line='case ":$PATH:" in *":$HOME/foreman/bin:"*) ;; *) export PATH="$HOME/foreman/bin:$PATH" ;; esac'
grep -Fqx "$foreman_path_line" "$HOME/.bashrc" 2>/dev/null || printf '\n%s\n' "$foreman_path_line" >> "$HOME/.bashrc"
eval "$foreman_path_line"
unset foreman_path_line
```

For Bash login shells (including the default macOS Terminal configuration),
ensure your `~/.bash_profile` loads `~/.bashrc`:

```bash
foreman_rc_line='[ -f "$HOME/.bashrc" ] && . "$HOME/.bashrc"'
grep -Fqx "$foreman_rc_line" "$HOME/.bash_profile" 2>/dev/null || printf '\n%s\n' "$foreman_rc_line" >> "$HOME/.bash_profile"
unset foreman_rc_line
```

Zsh (`~/.zshrc`):

```zsh
foreman_path_line='case ":$PATH:" in *":$HOME/foreman/bin:"*) ;; *) export PATH="$HOME/foreman/bin:$PATH" ;; esac'
grep -Fqx "$foreman_path_line" "$HOME/.zshrc" 2>/dev/null || printf '\n%s\n' "$foreman_path_line" >> "$HOME/.zshrc"
eval "$foreman_path_line"
unset foreman_path_line
```

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
