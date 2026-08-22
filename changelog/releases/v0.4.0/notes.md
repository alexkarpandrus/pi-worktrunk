This release lets Pi agents run configured Worktrunk aliases with clear confirmation, shortens the interactive command to `/wt`, and makes Worktrunk tool calls easier to scan with consistent colors.

## 💥 Breaking changes

### Shorter Worktrunk slash command

The interactive slash command is now `/wt`, replacing `/worktree`.

Before:

```text
/worktree status
```

After:

```text
/wt status
```

Update saved prompts and workflows that invoke the old command. The `worktree` agent tool keeps its existing name.

*By @mavam in #8.*

## 🚀 Features

### Agent-callable Worktrunk aliases

The agent can now run configured Worktrunk aliases when you explicitly request a matching action. For example, if your configuration defines a `deploy` alias, you can ask:

```text
Deploy to staging.
```

The agent calls the `worktree_alias` tool with `deploy` and the user-supplied `staging` argument. Pi shows the exact command and pipeline for confirmation before running it, and Worktrunk continues to enforce project-command approvals.

*By @mavam in #10.*

## 🔧 Changes

### Consistent Worktrunk command colors

Worktrunk tool calls now render their action names in the same blue as the `Worktrunk` label, so commands such as `create`, `list`, and `remove` are consistently styled in Pi's tool-call display.

*By @mavam in #9.*
