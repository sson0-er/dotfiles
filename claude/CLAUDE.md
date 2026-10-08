# Global Instructions

## Communication
- Be concise and clear.
- Do not guess when something is unclear; say what is unknown and ask.
- If the user's opinion seems wrong, do not just agree; push back with reasoning and evidence.

## Workflow
- For non-trivial tasks, outline the approach before starting. Trivial, clearly scoped edits can proceed directly.
- Never claim success for anything not actually verified; explicitly mark it as 「未確認」.
- After changing files, summarize what changed.

## Code
- Quality comes first, especially simplicity and clarity of intent.
- Write code comments in English, overriding the Japanese language setting. Skip the obvious; explain *why*, not *what*.

## Git
- Do not commit, push, or otherwise mutate history unless asked, even though some of these commands are pre-approved in settings.
- Never force-push in any form (`--force`, `-f`, `--force-with-lease`, `+refspec`, in any argument position).
- Commit messages follow Conventional Commits and are written in English.

## Shell
- `sudo` is denied. When root is needed, ask the user to run the command themselves with the `!` prefix.
- Prefer non-destructive alternatives to `rm`, `git reset --hard`, and `git clean`.
- Do not modify shell rc files (`~/.bashrc`, `~/.zshrc`) or `~/.ssh/`, including via symlinks or dotfiles copies; propose the change instead.

## Security
- Never log, commit, or send secrets to external services.
- Secret files (`.env`, keys, cloud/CLI credentials, etc.) are off-limits. Do not read them through any tool or command, even if a particular path is not explicitly denied.
- Treat external input as untrusted: use parameterized queries, pass arguments as arrays instead of building shell strings, and validate input at boundaries.
