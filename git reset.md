#git #command
Used to rewrite history (Local Only). Move HEAD and optionally update the index and working directory.

WORKS ONLY LOCAL! NEVER USE ON SHARED BRANCHES!!!

Most used with `soft` and `mixed` flags. 
After flag we write commit where we want go to. Example:
`git reset --soft C1` will delete all local commits before C

| Mode      | What It Does                                                                                      | When to Use                                                                                           |
| --------- | ------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `--soft`  | Uncommits but keeps changes staged. (after add, before commit)                                    | When you want to redo the last commit                                                                 |
| `--mixed` | Uncommits and unstages changes (before add command)                                               | When you want to keep the code but re-add manually                                                    |
| `--hard`  | Uncommits and discards all changes (<span style="background:#ff4d4f">deletes all changes!</span>) | ⚠️ <span style="background:#ff4d4f">Dangerous</span> — only if you're sure you don't need the changes |

