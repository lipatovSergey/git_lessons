#git #command

Used to show git logs. Which changes were made, by who, when, etc.

This command has a lot of useful argument. Here is some of them:
```bash
# short one line output
git log --pretty=oneline
# other commands easy to understand
git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=<your name>
git log --pretty=oneline --all
```

Autor of course "Git Immersion" gives this variant of git log as his favorite:
```bash
git log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short
```

**`gitk`** is a UI for git log. Looks pretty good need to try it.