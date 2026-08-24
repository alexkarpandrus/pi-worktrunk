This release makes Worktrunk commands easier for Pi agents to use by providing complete command trees, meaningful options, canonical examples, and clear separation of arguments. Pi also asks for confirmation before running hooks or administrative commands that change approvals, state, shell integration, or plugins.

## 🔧 Changes

### Complete Worktrunk command guidance

Pi agents now receive the generated Worktrunk command tree with its arguments, meaningful options, and canonical examples. The tool enumerates built-in commands, commands added by the installed Worktrunk version, and configured aliases separately from their remaining arguments, making calls such as worktree creation unambiguous:

```json
{"command":"switch","args":["--create","video-backgrounds"]}
```

Pi asks for confirmation before running hooks or administrative commands that change approvals, state, shell integration, or plugins.

*By @mavam in #12.*
