# Git Rebase Challenge

## Objective

The goal of this challenge is to use `git rebase` to integrate commits from two branches, `add-echo` and `add-reverse`, onto the `master` branch. The final commit history on the `master` branch should be linear, with no merge commits or branching.

### Expected Commit Log

Upon successful completion, the `git log` on the `master` branch should appear as follows:

```
/challenge-git master
⚡ git log
61a2c67 feat: add reverse route (David Guttman, 7 minutes ago)
2c2c5d6 feat: add echo route (David Guttman, 10 minutes ago)
dcc4c0b docs: add more instructions (David Guttman, 11 minutes ago)
...
```

## Instructions

To attempt this challenge, please follow these steps:

1. **Create a New Repository:**
   - Create a new repository in your GitHub account and note the repository URL.

2. **Clone the Challenge Repository:**
   - Clone this repository to your local machine using the following command:
     ```bash
     git clone <challenge-repo-url>
     ```

3. **Solve the Challenge:**
   - Use `git rebase` to integrate the `add-echo` and `add-reverse` branches onto the `master` branch, ensuring a linear commit history.

4. **Set Your New Repository as the Origin:**
   - Update the remote URL to point to your newly created repository:
     ```bash
     git remote set-url origin <your-repo-url>
     ```

5. **Push Your Solution:**
   - Push your changes to your repository:
     ```bash
     git push origin master
     ```

**Note:** It is essential to follow these steps precisely for your solution to be accepted. Forks or alternative methods will not be considered.

## Resolution

To successfully complete the challenge, follow these detailed steps:

1. **Checkout the `master` Branch:**
   - Ensure you are on the `master` branch:
     ```bash
     git checkout master
     ```

2. **Rebase `add-echo` onto `master`:**
   - Rebase the `add-echo` branch onto `master`:
     ```bash
     git checkout add-echo
     git rebase master
     ```

3. **Merge `add-echo` into `master`:**
   - Fast-forward merge the rebased `add-echo` branch into `master`:
     ```bash
     git checkout master
     git merge add-echo
     ```

4. **Rebase `add-reverse` onto `master`:**
   - Rebase the `add-reverse` branch onto the updated `master` branch:
     ```bash
     git checkout add-reverse
     git rebase master
     ```

5. **Merge `add-reverse` into `master`:**
   - Fast-forward merge the rebased `add-reverse` branch into `master`:
     ```bash
     git checkout master
     git merge add-reverse
     ```

6. **Verify the Commit History:**
   - Check the git log to ensure the commits are in the desired order without any merge commits:
     ```bash
     git log --oneline
     ```

By following these steps, you will have successfully rebased both branches onto `master` without any merge commits or branching, achieving the desired linear commit history.
