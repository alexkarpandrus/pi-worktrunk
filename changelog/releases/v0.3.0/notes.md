This release exposes configured Worktrunk aliases as `/worktree` subcommands and improves recovery when a session's worktree disappears. It also makes Worktrunk tool calls easier to scan with clearer, bolder headers.

## 🚀 Features

### Worktrunk alias subcommands in Pi

Configured Worktrunk aliases now appear as subcommands of Pi's single `/worktree` command. For example, you can run a `wt land` alias directly from Pi:

```text
/worktree land
/worktree land 42
```

Arguments are forwarded to Worktrunk without shell expansion, and project aliases retain Worktrunk's approval checks.

*By @mavam in #7.*

## 🔧 Changes

### Bold actions in Worktrunk tool calls

Worktrunk tool calls now render the action in bold, making calls such as `Worktrunk › list` easier to scan in Pi's transcript.

*By @mavam in #7.*

### Clearer Worktrunk tool calls

Worktrunk tool calls now separate the tool name from the action and emphasize the target branch or path:

```text
Worktrunk › create remove-github
```

This makes tool calls easier to scan while keeping them visually distinct from shell commands.

*By @mavam in #6.*

## 🐞 Bug fixes

### Recovery from removed worktrees

The `/worktree continue` command now recovers when another process removes Pi's current worktree. You can continue the session in an existing worktree instead of seeing a misleading message that Worktrunk is missing. If no worktree remains available, the error now identifies the removed working directory.

*By @mavam in #5.*
