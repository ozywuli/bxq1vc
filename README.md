How To Remove Files from an older commit

1. Run `git log` to get the SHA1 of the commit you want to edit
2. Run `git base --interactive <SHA1 id>^`. This will open a file for you with a list of commits. At the beginning of each commit is the word "pick". For the commit you want to edit, change "pick" to "edit". Save and quit.
3. Run `git rm <filename>` to remove the files you don't want in your commit.
4. Run `git commit --amend` to modify your commit message
5. Run `git rebase --continue` to complete your rebase.
6. ALL DONE!