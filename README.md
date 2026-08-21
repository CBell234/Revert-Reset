# Revert-Reset
Revert vs Reset assessment 
Reverting Changes
Definition

Refers to creating a new commit that undoes the changes introduced by a specific commit or a range of commits. Instead of removing the commit from the project history, Git creates a new commit that inverses the changes introduced by the original commit(s).

Effect

When you revert a commit, Git keeps a record of the reversal, which means the history remains intact. The original commit(s) and their changes are still part of the project history, but the reverted changes are now undone by the new commit.

Use Case

Reverting is typically used when you want to safely undo changes without altering the existing commit history. It's useful in collaborative environments where other team members might have already pulled the original changes.

Commands

git revert <commit-hash>
This command creates a new commit that undoes the changes made by the specified commit.

Resetting Changes

Definition

Refers to altering the commit history by moving the HEAD and branch references to a different commit. It can be used to undo changes in a more forceful manner, potentially discarding commits and their changes from the branch's history.

Effect

When you reset commits, Git moves the branch pointer to a specified commit, which can discard commits from the branch's history. Depending on the reset mode, it can also modify the working directory and staging area.

Use Case

Resetting is used when you want to undo local changes or reset the branch to a previous state, potentially discarding commits. It's more aggressive than reverting and should be used with caution, especially when working in a shared repository.

Commands

git reset --soft <commit-hash>
Soft reset - moves the HEAD to a different commit, keeping changes in the working directory and staging area.

git reset --mixed <commit-hash>
Mixed reset - moves the HEAD to a different commit and resets the staging area, but keeps changes in the working directory.

git reset --hard <commit-hash>
Hard reset - moves the HEAD to a different commit and resets both the staging area and working directory, discarding changes.
