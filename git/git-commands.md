# Git Commands Reference

 A living document of Git commands I'm learning during my DevOps journey.
---

## 1. Setup & Config

1. **Check Git version**
   - Command: `git --version`
   - Description: Check which version of Git is installed on your system.
   - Example: `git --version`

2. **Set global username**
   - Command: `git config --global user.name "Your Name"`
   - Description: Set your name for all Git commits.
   - Example: `git config --global user.name "DevOps Learner"`

3. **Set global email**
   - Command: `git config --global user.email "email@example.com"`
   - Description: Set your email for all Git commits.
   - Example: `git config --global user.email "learner@devops.local"`

4. **View all configurations**
   - Command: `git config --list`
   - Description: View all Git configuration settings.
   - Example: `git config --list`

---

## 2. Basic Workflow

1. **Initialize repository**
   - Command: `git init`
   - Description: Initialize a new Git repository in the current directory.
   - Example: `git init`

2. **Check status**
   - Command: `git status`
   - Description: Show the current state of your working directory and staging area.
   - Example: `git status`

3. **Add specific file**
   - Command: `git <add file>`
   - Description: Add file(s) to the staging area, preparing them for commit.
   - Example: `git add git-commands.md`

4. **Add all files**
   - Command: `git add .`
   - Description: Add all changed files in the current directory to staging.
   - Example: `git add .`

5. **Commit changes**
   - Command: `git commit -m "message"`
   - Description: Create a commit with the staged changes and a descriptive message.
   - Example: `git commit -m "Initial commit: Add git commands reference"`

---

## 3. Viewing Changes

1. **View commit history**
   - Command: `git log`
   - Description: Display the commit history with full details.
   - Example: `git log`

2. **Compact log view**
   - Command: `git log --oneline`
   - Description: Show commit history in compact, one-line-per-commit format.
   - Example: `git log --oneline`

3. **View unstaged changes**
   - Command: `git diff`
   - Description: Show changes in files that haven't been staged yet.
   - Example: `git diff`

4. **View staged changes**
   - Command: `git diff --staged`
   - Description: Show changes in files that are staged for commit.
   - Example: `git diff --staged`

---

## 4. Repository Management

1. **Explore .git directory**
   - Command: `ls -la .git/`
   - Description: Explore the contents of the hidden .git directory.
   - Example: `ls -la .git/`

2. **Remove file**
   - Command: `git rm <old file>`
   - Description: Remove a file from both working directory and staging area.
   - Example: `git rm oldfile.txt`

3. **Rename/move file**
   - Command: `git mv <old-file> <new-file>`
   - Description: Rename or move a file and stage the change.
   - Example: `git mv old-name.md new-name.md`

---

## 5. Commit History

1. **Graph view**
   - Command: `git log --graph`
   - Description: Display commit history with an ASCII graph showing branch structure.
   - Example: `git log --graph`

2. **Compact graph all branches**
   - Command: `git log --oneline --graph --all`
   - Description: Compact view of all branches with visual graph.
   - Example: `git log --oneline --graph --all`

3. **Show specific commit**
   - Command: `git show commit`
   - Description: Show detailed information about a specific commit.
   - Example: `git show ccc2e47`

4. **Limit commit count**
   - Command: `git log -n 5`
   - Description: Show only the last 5 commits.
   - Example: `git log -n 5`

---

## 6. Undoing Changes

1. **Restore file**
   - Command: `git <file>`
   - Description: Discard changes in working directory (unstage and revert to last commit).
   - Example: `git restore file.txt`

2. **Unstage file**
   - Command: `git restore --staged <file>`
   - Description: Unstage a file but keep the changes in working directory.
   - Example: `git restore --staged file.txt`

---

## 7. Branching

1. **List branches**
   - Command: `git branch`
   - Description: List all local branches in the repository.
   - Example: `git branch`

2. **Create branch**
   - Command: `git branch <name of the branch>`
   - Description: Create a new branch but don't switch to it.
   - Example: `git branch feature-1`

3. **Switch branch (legacy)**
   - Command: `git checkout branch `
   - Description: Switch to an existing branch.
   - Example: `git checkout feature-1`

4. **Create and switch (legacy)**
   - Command: `git checkout -b branch`
   - Description: Create a new branch and switch to it in one command.
   - Example: `git checkout -b feature-2`

5. **Switch branch (modern)**
   - Command: `git switch branch`
   - Description: Modern command to switch between branches (clearer than checkout).
   - Example: `git switch main`

6. **Create and switch (modern)**
   - Command: `git switch -c branch`
   - Description: Create a new branch and switch to it (modern alternative).
   - Example: `git switch -c feature-3`

7. **Delete merged branch**
   - Command: `git branch -d branch`
   - Description: Delete a branch (only if it's been merged).
   - Example: `git branch -d old-feature`

8. **Force delete branch**
   - Command: `git branch -D branch;`
   - Description: Force delete a branch even if not merged.
   - Example: `git branch -D experimental`

9. **Merge branch**
   - Command: `git merge branch`
   - Description: Merge specified branch into current branch.
   - Example: `git merge feature-1`

---

## 8. Remote Repositories

1. **Add remote**
   - Command: `git remote add origin <url>`
   - Description: Connect your local repo to a remote repository.
   - Example: `git remote add origin https://github.com/username/repo.git`

2. **View remotes**
   - Command: `git remote -v`
   - Description: View all configured remote repositories.
   - Example: `git remote -v`

3. **Push to remote**
   - Command: `git push <remote> <branch>`
   - Description: Upload your commits to a remote repository.
   - Example: `git push origin main`

4. **Push with upstream*
   - Command: `git push -u  <remote> <branch>`
   - Description: Push and set upstream tracking (for first push of a branch).
   - Example: `git push -u origin feature-1`

5. **Pull changes**
   - Command: `git pull  <remote> <branch>`
   - Description: Fetch changes from remote and merge into current branch.
   - Example: `git pull origin main`

6. **Fetch changes**
   - Command: `git fetch remote`
   - Description: Download changes from remote but don't merge them.
   - Example: `git fetch origin`

7. **Clone repository**
   - Command: `git clone <url>`
   - Description: Copy a remote repository to your local machine.
   - Example: `git clone https://github.com/username/repo.git`

8. **Push all branches**
   - Command: `git push --all`
   - Description: Push all branches to remote.
   - Example: `git push --all origin`

9. **Remove remote**
   - Command: `git remote remove origin`
   - Description: Remove a remote connection.
   - Example: `git remote remove origin`

---

## Quick Reference Cheat Sheet

```bash
# Start a new repository
git init
git add .
git commit -m "Initial commit"

# Create and switch to new branch
git switch -c feature-branch

# Push to remote
git push -u origin feature-branch

# Pull latest changes
git pull origin main

# View status and log
git status
git log --oneline

# Merge Commands
git merge feature-branch              # Merge (fast-forward if possible)
git merge --no-ff feature-branch      # Force merge commit
git merge --squash feature-branch     # Squash all commits into one

# Rebase Commands
git rebase main                       # Rebase current branch onto main
git rebase --continue                 # Continue after resolving conflicts
git rebase --abort                    # Cancel the rebase

# Stash Commands
git stash push -m "description"       # Stash with message
git stash list                        # List all stashes
git stash pop                         # Apply and delete latest stash
git stash apply stash@{0}             # Apply specific stash (keep it)
git stash drop stash@{0}              # Delete specific stash
git stash clear                       # Delete all stashes

# Cherry-Pick Commands
git cherry-pick abc1234               # Cherry-pick single commit
git cherry-pick A^..C                 # Cherry-pick range
git cherry-pick --continue            # Continue after resolving conflicts
git cherry-pick --abort               # Cancel the cherry-pick

# Visualization
git log --oneline --graph --all       # Visual commit history
```

# Reset Commands

**Reset soft**
- Command: `git reset --soft HEAD~1`
- Description: Undo commits but keep changes staged.
- Example: `git reset --soft HEAD~1`

**Reset mixed (default)**
- Command: `git reset --mixed HEAD~1`
- Description: Undo commits and unstage changes (keep in working directory).
- Example: `git reset --mixed HEAD~1`

**Reset hard**
- Command: `git reset --hard HEAD~1`
- Description: Completely discard commits and all changes (DESTRUCTIVE).
- Example: `git reset --hard HEAD~1`
-  Warning: This permanently deletes uncommitted work

**Reset to specific commit**
- Command: `git reset --hard <commit-hash>`
- Description: Reset repository to a specific commit state.
- Example: `git reset --hard abc1234`

---

# Revert Commands

**Revert specific commit**
- Command: `git revert <commit-hash>`
- Description: Create new commit that undoes changes from target commit (safe for shared branches).
- Example: `git revert abc1234`

**Revert last commit**
- Command: `git revert HEAD`
- Description: Revert the most recent commit.
- Example: `git revert HEAD`

**Revert older commit**
- Command: `git revert HEAD~3`
- Description: Revert a commit from 3 steps back in history.
- Example: `git revert HEAD~3`

**Revert without committing**
- Command: `git revert --no-commit <commit-hash>`
- Description: Stage revert changes without automatically committing.
- Example: `git revert --no-commit abc1234`

**Continue revert**
- Command: `git revert --continue`
- Description: Continue revert process after resolving conflicts.
- Example: `git revert --continue`

**Abort revert**
- Command: `git revert --abort`
- Description: Cancel the revert operation and return to previous state.
- Example: `git revert --abort`

---

# Reflog (Recovery)

**View reflog**
- Command: `git reflog`
- Description: View complete history of all Git operations (your safety net for recovery).
- Example: `git reflog`

**Recover using reflog**
- Command: `git reset --hard HEAD@{n}`
- Description: Restore repository to a specific point in reflog history.
- Example: `git reset --hard HEAD@{2}`
- Use case: Undo accidental hard reset or recover "lost" commits

**Reflog for specific branch**
- Command: `git reflog show <branch-name>`
- Description: View reflog history for a specific branch.
- Example: `git reflog show main`

# GitHub CLI Commands Reference

Manage GitHub directly from your terminal - no browser required.

---

## Authentication

**Login to GitHub**
- Command: `gh auth login`
- Description: Authenticate with your GitHub account (supports OAuth, PAT, SSH).
- Example: `gh auth login`

**Check authentication status**
- Command: `gh auth status`
- Description: View current authentication status and logged-in account.
- Example: `gh auth status`

**Logout**
- Command: `gh auth logout`
- Description: Sign out from GitHub CLI.
- Example: `gh auth logout`

---

## Repository Management

**Create public repository**
- Command: `gh repo create <name> --public`
- Description: Create a new public repository.
- Example: `gh repo create my-project --public --description "My awesome project"`

**Create private repository**
- Command: `gh repo create <name> --private`
- Description: Create a new private repository.
- Example: `gh repo create my-secret-project --private --clone`

**Clone repository**
- Command: `gh repo clone <owner/repo>`
- Description: Clone a repository using GitHub CLI.
- Example: `gh repo clone torvalds/linux`

**View repository details**
- Command: `gh repo view`
- Description: Display details about the current repository.
- Example: `gh repo view`

**View specific repository**
- Command: `gh repo view <owner/repo>`
- Description: Display details about any repository.
- Example: `gh repo view facebook/react`

**Open repository in browser**
- Command: `gh repo view --web`
- Description: Open the repository in your default web browser.
- Example: `gh repo view --web`

**List your repositories**
- Command: `gh repo list`
- Description: List all repositories owned by you.
- Example: `gh repo list --limit 20`

**Delete repository**
- Command: `gh repo delete <owner/repo>`
- Description: Delete a repository (requires confirmation).
- Example: `gh repo delete myusername/old-project --yes`

---

## Issues

**Create issue interactively**
- Command: `gh issue create`
- Description: Create a new issue with interactive prompts.
- Example: `gh issue create`

**Create issue with details**
- Command: `gh issue create --title "..." --body "..." --label "bug"`
- Description: Create an issue with title, description, and labels.
- Example: `gh issue create --title "Login broken" --body "Cannot authenticate" --label "bug"`

**List open issues**
- Command: `gh issue list`
- Description: List all open issues in the current repository.
- Example: `gh issue list`

**List all issues**
- Command: `gh issue list --state all`
- Description: List both open and closed issues.
- Example: `gh issue list --state all`

**Filter issues by label**
- Command: `gh issue list --label <label>`
- Description: List issues with a specific label.
- Example: `gh issue list --label "help wanted"`

**View specific issue**
- Command: `gh issue view <number>`
- Description: Display details of a specific issue.
- Example: `gh issue view 42`

**Open issue in browser**
- Command: `gh issue view <number> --web`
- Description: Open an issue in your web browser.
- Example: `gh issue view 42 --web`

**Close issue**
- Command: `gh issue close <number>`
- Description: Close an open issue.
- Example: `gh issue close 42 --comment "Fixed in PR #43"`

**Reopen issue**
- Command: `gh issue reopen <number>`
- Description: Reopen a closed issue.
- Example: `gh issue reopen 42`

---

## Pull Requests

**Create PR interactively**
- Command: `gh pr create`
- Description: Create a pull request with interactive prompts.
- Example: `gh pr create`

**Create PR with auto-fill**
- Command: `gh pr create --fill`
- Description: Auto-populate PR title and body from commit messages.
- Example: `gh pr create --fill`

**Create PR with details**
- Command: `gh pr create --title "..." --body "..."`
- Description: Create a PR with specific title and description.
- Example: `gh pr create --title "Add feature X" --body "This PR implements feature X"`

**List open PRs**
- Command: `gh pr list`
- Description: List all open pull requests.
- Example: `gh pr list`

**List all PRs**
- Command: `gh pr list --state all`
- Description: List both open and closed pull requests.
- Example: `gh pr list --state all`

**View PR details**
- Command: `gh pr view <number>`
- Description: Display details of a specific pull request.
- Example: `gh pr view 15`

**Open PR in browser**
- Command: `gh pr view <number> --web`
- Description: Open a pull request in your web browser.
- Example: `gh pr view 15 --web`

**Checkout PR locally**
- Command: `gh pr checkout <number>`
- Description: Check out a pull request branch to your local machine.
- Example: `gh pr checkout 15`

**View PR diff**
- Command: `gh pr diff <number>`
- Description: View the diff of a pull request.
- Example: `gh pr diff 15`

**Check PR status**
- Command: `gh pr checks`
- Description: View the status of checks/CI for the current PR.
- Example: `gh pr checks`

**Approve PR**
- Command: `gh pr review <number> --approve`
- Description: Approve a pull request.
- Example: `gh pr review 15 --approve --body "LGTM"`

**Comment on PR**
- Command: `gh pr review <number> --comment --body "..."`
- Description: Leave a comment on a pull request.
- Example: `gh pr review 15 --comment --body "Please add tests"`

**Request changes on PR**
- Command: `gh pr review <number> --request-changes --body "..."`
- Description: Request changes on a pull request.
- Example: `gh pr review 15 --request-changes --body "Fix the typos"`

**Merge PR**
- Command: `gh pr merge <number>`
- Description: Merge a pull request (default merge commit).
- Example: `gh pr merge 15`

**Merge with merge commit**
- Command: `gh pr merge <number> --merge`
- Description: Merge using a merge commit.
- Example: `gh pr merge 15 --merge`

**Squash and merge**
- Command: `gh pr merge <number> --squash`
- Description: Squash all commits and merge.
- Example: `gh pr merge 15 --squash --delete-branch`

**Rebase and merge**
- Command: `gh pr merge <number> --rebase`
- Description: Rebase and merge the pull request.
- Example: `gh pr merge 15 --rebase`

**View your PR status**
- Command: `gh pr status`
- Description: Show status of relevant pull requests (yours + assigned reviews).
- Example: `gh pr status`

---

## GitHub Actions & Workflows

**List workflow runs**
- Command: `gh run list`
- Description: List recent workflow runs in the repository.
- Example: `gh run list --limit 10`

**List runs for specific workflow**
- Command: `gh run list --workflow=<name>`
- Description: Filter runs by workflow name.
- Example: `gh run list --workflow=ci.yml`

**View run details**
- Command: `gh run view <run-id>`
- Description: Display details of a specific workflow run.
- Example: `gh run view 123456`

**View run logs**
- Command: `gh run view <run-id> --log`
- Description: Display logs of a workflow run.
- Example: `gh run view 123456 --log`

**Watch workflow run**
- Command: `gh run watch`
- Description: Watch a workflow run in real-time.
- Example: `gh run watch`

**Rerun workflow**
- Command: `gh run rerun <run-id>`
- Description: Rerun a failed or completed workflow.
- Example: `gh run rerun 123456`

**List workflows**
- Command: `gh workflow list`
- Description: List all workflows in the repository.
- Example: `gh workflow list`

**View workflow details**
- Command: `gh workflow view <workflow>`
- Description: Display details of a specific workflow.
- Example: `gh workflow view ci.yml`

**Trigger workflow manually**
- Command: `gh workflow run <workflow>`
- Description: Manually trigger a workflow run.
- Example: `gh workflow run deploy.yml`

**Enable workflow**
- Command: `gh workflow enable <workflow>`
- Description: Enable a disabled workflow.
- Example: `gh workflow enable ci.yml`

**Disable workflow**
- Command: `gh workflow disable <workflow>`
- Description: Disable a workflow.
- Example: `gh workflow disable old-workflow.yml`

---

## GitHub API

**Make API call**
- Command: `gh api <endpoint>`
- Description: Make a raw GitHub API request.
- Example: `gh api repos/owner/repo/issues`

**Check API rate limit**
- Command: `gh api rate_limit`
- Description: View your current API rate limit status.
- Example: `gh api rate_limit`

**Get user info**
- Command: `gh api user`
- Description: Fetch information about the authenticated user.
- Example: `gh api user`

---

## Gists

**Create gist from file**
- Command: `gh gist create <file>`
- Description: Create a new public gist from a file.
- Example: `gh gist create script.sh`

**Create private gist**
- Command: `gh gist create --secret <file>`
- Description: Create a new private (secret) gist.
- Example: `gh gist create --secret notes.md`

**List your gists**
- Command: `gh gist list`
- Description: List all your gists.
- Example: `gh gist list`

**View gist**
- Command: `gh gist view <id>`
- Description: Display a specific gist.
- Example: `gh gist view abc123def456`

**Edit gist**
- Command: `gh gist edit <id>`
- Description: Edit an existing gist.
- Example: `gh gist edit abc123def456`

**Delete gist**
- Command: `gh gist delete <id>`
- Description: Delete a gist.
- Example: `gh gist delete abc123def456`

---

## Releases

**Create release**
- Command: `gh release create <tag>`
- Description: Create a new release.
- Example: `gh release create v1.0.0`

**Create release with notes**
- Command: `gh release create <tag> --notes "..."`
- Description: Create a release with release notes.
- Example: `gh release create v1.0.0 --notes "First stable release"`

**List releases**
- Command: `gh release list`
- Description: List all releases in the repository.
- Example: `gh release list`

**View release**
- Command: `gh release view <tag>`
- Description: Display details of a specific release.
- Example: `gh release view v1.0.0`

**Download release assets**
- Command: `gh release download <tag>`
- Description: Download assets from a release.
- Example: `gh release download v1.0.0`

**Delete release**
- Command: `gh release delete <tag>`
- Description: Delete a release.
- Example: `gh release delete v1.0.0 --yes`

---

## Search

**Search repositories**
- Command: `gh search repos <query>`
- Description: Search for repositories on GitHub.
- Example: `gh search repos "devops automation" --language=python`

**Search issues**
- Command: `gh search issues <query>`
- Description: Search for issues across GitHub.
- Example: `gh search issues "bug" --state=open`

**Search code**
- Command: `gh search code <query>`
- Description: Search code across GitHub repositories.
- Example: `gh search code "import pandas" --language=python`

**Search users**
- Command: `gh search users <query>`
- Description: Search for GitHub users.
- Example: `gh search users "location:India" --followers=">100"`

---

## Aliases

**Create alias**
- Command: `gh alias set <name> <command>`
- Description: Create a shortcut for a frequently-used command.
- Example: `gh alias set pv "pr view"`

**List aliases**
- Command: `gh alias list`
- Description: Display all your configured aliases.
- Example: `gh alias list`

**Delete alias**
- Command: `gh alias delete <name>`
- Description: Remove an alias.
- Example: `gh alias delete pv`

---

## Useful Flags

**JSON output**
- Flag: `--json`
- Description: Output results in JSON format for scripting.
- Example: `gh pr list --json number,title,author`

**Filter with jq**
- Flag: `--jq <query>`
- Description: Filter JSON output using jq syntax.
- Example: `gh pr list --json number --jq '.[].number'`

**Open in browser**
- Flag: `--web`
- Description: Open the resource in your web browser.
- Example: `gh repo view --web`

**Target specific repo**
- Flag: `--repo <owner/repo>`
- Description: Run command on a specific repository.
- Example: `gh issue list --repo facebook/react`

---

## Quick Reference Cheat Sheet
```bash
# Essential workflow
gh auth login
gh repo clone owner/repo
gh pr create --fill
gh pr list
gh pr checkout 42
gh pr merge 42 --squash

# Issues workflow
gh issue create
gh issue list --label bug
gh issue close 15

# CI/CD monitoring
gh run list
gh run watch
gh workflow run deploy.yml

# Quick tasks
gh repo view --web          # Open repo in browser
gh pr status                # See your PR status
gh issue list --assignee @me  # Your assigned issues
```

---

**Pro Tips:**

- Most commands work without arguments in a repo directory (auto-detects current repo)
- Use `--json` with `jq` for powerful scripting: `gh pr list --json number,title --jq '.[0]'`
- `gh pr create --draft` creates a draft PR
- `gh pr create --fill` saves time by auto-filling from commits
- Combine with shell commands: `gh issue list --json number | jq '.[].number' | xargs -I {} gh issue close {}`
