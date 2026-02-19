# OpenCode Dev Team Setup

Use this guide when your team runs this forked `opencode-dev` workflow.

## 1) Clone and install

```bash
git clone https://github.com/p-changki/Opencode-tool-v1.git
cd Opencode-tool-v1
git checkout dev
bun install
```

## 2) Run the dev TUI

```bash
bun run --cwd packages/opencode dev
```

## 3) Quick verification (read-only)

In TUI input:

```text
현재 repo에서 package.json scripts만 요약해줘(파일 수정 금지)
```

Then check:

```bash
git status --short
```

Expected: no changed files.

## 4) Panel keybinds (default leader = `ctrl+x`)

- Right sidebar toggle: `ctrl+x` then `b`
- Left sidebar toggle: `ctrl+x` then `v`
- Enter panel resize mode: `ctrl+x` then `p`
- Right width: `ctrl+x` then `-` / `=`
- Left width: `ctrl+x` then `[` / `]`
- Presets: `ctrl+x` then `0` (reset), `1` (code), `2` (review)

In resize mode:

- Left width: `h/l` or `←/→`
- Right width: `j/k` or `↓/↑`
- Exit: `esc` or `enter`

## 5) Important notes

- Repo code changes are shared through this fork branch.
- Personal config is **not** in this repo and must be set per user:
  - `~/.config/opencode/*`
- If someone launches the Homebrew OpenCode binary instead of this repo dev command, custom TUI changes will not appear.
