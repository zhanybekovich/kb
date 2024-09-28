To find a bug it's important to state the `bad` commit and `good` commit.

1. Start looking: `git bisect start`
2. Set the `bad` commit: `git bisect bad`
3. Set the `good` commit: `git bisect good <hashOfGoodCommit>`
4. Log all commits: `git log --oneline --all`

Then git will move to the middle commit and developer can run tests if the issue is there that means that issue is somewhere in the 2nd half of the history.  

If there is no issue the current commit will be set as `good`: `git bisect good` and app is tested. This steps repeats until the commit with bug is found. 

When all bugs are fixed `head` should be attached to master: `git bisect reset`




