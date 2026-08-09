This release lets you manage Worktrunk worktrees directly from pi and continue sessions in existing or newly created worktrees. The new /worktree command and agent tool preserve Worktrunk’s safety safeguards while making worktree-based workflows easier to control.

## 🚀 Features

### Continue pi sessions in Worktrunk worktrees

Use `/worktree continue [target]` to continue the current pi session in an existing Worktrunk worktree. You can also create a worktree and continue there in one operation:

```sh
/worktree create feature/auth --continue
```

The extension asks for confirmation, creates a linked session copy in the target worktree, and switches the current pi process to it. It preserves the source session and records a visible working-directory transition without rewriting historical messages. Continuation also works as the first action in a fresh session, before pi has written its session file.

*By @mavam and @codex in #3.*

### Interactive Worktrunk management in pi

Pi now provides a `/worktree` command and a `worktree` agent tool for listing, inspecting, creating, resolving, and safely removing Worktrunk worktrees:

```sh
/worktree create feature/auth
/worktree list
```

Both interfaces keep Worktrunk as the source of truth and preserve its hook approval and removal safeguards. This integration requires Worktrunk 0.70 or later.

*By @mavam and @codex in #2.*
