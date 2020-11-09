# Hacking The Github Stats
The [GitHub Stats](https://github.com/anuraghazra/github-readme-stats) 
is an external service to display your ranking based on commits, PRs,
contribution etc.

There is the computation for that:

```
  const COMMITS_OFFSET = 1.65;
  const CONTRIBS_OFFSET = 1.65;
  const ISSUES_OFFSET = 1;
  const STARS_OFFSET = 0.75;
  const PRS_OFFSET = 0.5;
  const FOLLOWERS_OFFSET = 0.45;
  const REPO_OFFSET = 1;
  ```
this is directly from the code of the app itself, so 
you want to focus on `commits` and `contrib`.

Commits are very easy to generate, simply create a private repo
named `test` so that it will look like you are testing GitHub
or any bug. Now, make sure that you turn on the include
private commits in the API.

Contributions to repos are actually your repos and
repos of others when you create pull requests even
if they simply closed them.
