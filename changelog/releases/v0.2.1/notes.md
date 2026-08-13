Pi's TUI now presents Worktrunk's native output for every agent tool action while preserving structured JSON for the model. This release also supports the current Worktrunk removal result schema.

## 🐞 Bug fixes

### Native Worktrunk tool output

The `worktree` agent tool now shows Worktrunk's native text output in Pi's TUI instead of raw JSON. Lists retain Worktrunk's table and status symbols, while create, remove, status, path, and settings results use their corresponding Worktrunk presentation. The model continues to receive structured JSON.

*By @mavam in #4.*
