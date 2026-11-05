# Assignment 1 – Campus Canteen Menu

**Q1: Your friend ran `git commit` and Git replied "nothing added to commit but untracked files present". What went wrong, and what should they type next?**

**Ans:** The problem is that the file was not added to the staging area. Git only commits files that have been staged. First, the friend should use `git add filename` to stage the file and then run `git commit -m "Add file"` to commit it.

**Q2: When would you use `git diff`, and when `git diff --staged`? Give an example from this assignment.**

**Ans:** `git diff` is used to view changes made in files that have not been staged yet. `git diff --staged` is used to view changes that have already been staged and are ready to be committed.
In this assignment, I used `git diff` after changing the Dosa price from 40 to 45 and adding Vada and Poori to the menu. After running `git add menu.txt`, I used `git diff --staged` to check the changes before committing.

**Q3: A classmate committed `manager.env` before creating `.gitignore`. Will adding it to `.gitignore` now stop Git tracking it? Which command stops tracking the file but keeps it on disk?**

**Ans:** No, adding a file to `.gitignore` does not stop Git from tracking a file that has already been committed. To stop tracking the file while keeping it on the computer, the classmate should use `git rm --cached manager.env`. Then they should commit the change. The `.gitignore` file should also contain `*.env` to prevent similar files from being tracked in the future.

**Q4: Explain the difference between `git restore <file>` and `git restore --staged <file>`.**

**Ans:** `git restore <file>` is used to discard unstaged changes in a file and restore it to its last committed version.
`git restore --staged <file>` is used to remove a file from the staging area without deleting the modifications made to it.
In this assignment, I used `git restore menu.txt` to bring back a deleted menu item and `git restore --staged menu.txt` to unstage changes while keeping the file modifications.

**Q5: One of your teammates writes `update` as every commit message. Rewrite one of your own commits' messages to show what a good message looks like, and explain why it matters.**

**Ans:** A good commit message should clearly describe the changes made in the commit. For example, instead of writing `update`, a better commit message would be `Update canteen menu and prices`.
The command `git commit --amend -m "Update canteen menu and prices"` can be used to change the message of the latest commit. However, amending a commit rewrites Git history. Since the assignment requires preserving commit history, I would avoid amending an existing commit unless instructed otherwise.
Meaningful commit messages make it easier to understand changes, track project progress and collaborate with other developers.