# Good Software Checklist and Best Practices
The following is a checklist of best practices to develop and maintain good modern software. This list does not pretend to be complete, exhaustive or definitive, but should be considered as an evolving document to which anyone can **contribute** (please do), sending a pull request.

The backbone of this list was drafted within [TwinLogix s.r.l.](https://www.twinlogix.com/) in order to promote the use of good software development and management practices and standardize them across projects. For many practices, thid parties tools, services or products are also recommended to help with proper application. Feel free to supplement and evolve these lists.

## Version Control

- Use a **VCS**
  - [`GIT`](https://git-scm.com/)
- Use a **branch naming convention**
  - [`main`, `stage`, `develop`, `feature`, `bugfix`, `hotfix` or `test`](https://dev.to/varbsan/a-simplified-convention-for-naming-branches-and-commits-in-git-il4)
- Use **conventional commits**
  - [`feat`, `fix`, `chore`, `refactor`, `doc`, `test`](https://www.conventionalcommits.org/)
- **Protect** your production **branch**
- Adopt and combine **workflows**
  - [`GitFlow`](https://dev.to/the_previ/a-practical-introduction-to-git-flow-5420)
  - [`GitHub flow`](https://docs.github.com/en/get-started/quickstart/github-flow)
  - [`Rebase and squash`](https://matt-rickard.com/squash-merge-or-rebase) insted of merge
- Use **[release tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging)**
- Organize projects using **[monorepo](https://monorepo.tools/)**
- Use **[git hooks](https://git-scm.com/docs/githooks)** to add pre-commit checks

## IDE

- Use an **IDE**
  - [`Visul Studio Code`](https://code.visualstudio.com/)
- Use a generative AI copilot
  - [`GitHub Copilot`](https://github.com/features/copilot)
- Use a secure coding plugin
  - [`Snyk`](https://snyk.io/platform/ide-plugins/)  
