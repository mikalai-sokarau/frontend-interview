### How many types of version control systems exist?
1. Centralized have a central server where all the code is stored, and developers check out and commit changes to that central repository. Examples of centralized version control systems include Subversion (SVN) and Perforce.
2. Decentralized do not have a central server. Instead, each developer has a complete copy of the code repository, and they can commit changes to their local repository. Then, they can push their changes to a remote repository to share them with other developers. Examples of distributed version control systems include Git, Mercurial, and Bazaar.

### Centralized VCS pros and cons:
Pros:
1. Centralized architecture makes it easy to manage access control, as all the code is stored in one central location.
2. Changes can be easily tracked, and it's possible to revert to a previous version of the code if needed.
3. Collaboration is facilitated, as users can access and modify the code from a central repository.
4. Easy to backup, as all code is stored in a central location.

Cons:
1. If the central repository is down or inaccessible, users won't be able to access the code or save their changes.
2. Performance can be an issue with larger teams or projects, as all code is stored in a central location.
3. Branching and merging can be more difficult, as multiple users may need to make changes to the same code at the same time.
4. The central repository can become a bottleneck for development, as all code changes must go through it.

Overall, while CVCS can be a good choice for smaller teams or simpler projects, the limitations of a centralized architecture can become problematic as projects grow in size and complexity.

### Decentralized VCS pros and cons:
Pros:
* Offline work: With DVCS, you can work offline and commit changes locally, which is useful when you don't have a reliable internet connection. You can synchronize your changes with the central repository once you are connected again.
* Distributed workflow: In DVCS, each developer has their own repository, which means they can work independently without affecting others. This distributed workflow allows for more flexibility in how developers work together.
* Backup: Each developer has a full copy of the repository, which acts as a backup. This means that if the central repository is lost, the development history can be reconstructed from any of the developer's repositories.
* Branching and merging: DVCS makes it easier to create and manage branches, which can be merged more easily than in centralized systems. This allows developers to work on different features simultaneously without conflicts.

Cons:
* Complexity: DVCS can be more complex to use than centralized systems, particularly for new users who may find it difficult to understand the distributed workflow.
* Learning curve: DVCS requires developers to learn new concepts and commands, which may take some time and effort.
* Data duplication: Each developer has a full copy of the repository, which means that more disk space is required. This can be a problem if the repository is very large.
* Security: With a distributed workflow, it is easier for a developer to make unauthorized changes or introduce malicious code, which can compromise the security of the system.

### How to choose between rebase and merge?
Merge is a simpler and more straightforward option than rebase.
Merge preserves the original commit history, making it easier to track changes and identify which branch a specific commit originated from.
Rebase provides a cleaner and more linear history.
Rebase allows incorporating changes from an upstream branch while maintaining the commit history of your local branch.

### Why rebasing the master branch can be dangerous?
Rebasing master can be dangerous because it changes the Git history of the master branch, which can cause problems for other developers who are also working on the same branch. If other developers have already based their work on the original version of the branch, and then the branch is rebased, their work may conflict with the updated version of the branch.
Furthermore, rebasing rewrites the Git history of the branch, which can make it difficult to track down bugs or to revert changes if something goes wrong. Additionally, if a mistake is made during the rebase process, it can be challenging to undo the changes and restore the branch to its previous state.

### How to maintain code quality on the project?
* Follow best practices, conventions and principles (codding, committing, commenting, SOLID, KISS, etc.)
* Use automatic tools (linters, prettier) to keep the codebase consistent (ESLint, JSLint, Prettier, .editorconfig)
* Use static code analyzers (SonarQube, DeepSource)
* Use docker vulnerability scanners (Snyk, Docker Bench)
* Use automatic source/dependency checkers (Dependabot, BlackDuck)
* Write tests (unit, integration, e2e, etc.)
* Use pre-commit/push hook (Husky)
* Use typed version of JavaScript (TypeScript, Flow)
* Adopt continuous integration
* Manually review pull requests
* Practice pair programming

### What branching strategies do you know?
* GitFlow: This is a branching model designed for large projects with complex workflows. It uses two main branches, "master" and "develop", and has separate feature, release, and hotfix branches.
* GitHub Flow: This is a simplified version of GitFlow that is based on the idea of continuous deployment. It uses only one branch, "master", and feature branches are created for each new feature or change.
* Trunk-Based Development: This is a branching strategy where all changes are committed to a single trunk or mainline branch. Feature flags and other techniques are used to isolate changes until they are ready for release.
* GitLab Flow: This is a workflow designed specifically for GitLab, which uses a combination of feature branches and continuous integration to ensure that changes are tested and deployed quickly.

### How to choose a branching strategy?
* Small teams or individual developers may benefit from using a simple strategy like GitHub flow or feature branching.
* For larger teams, a branching strategy that provides more isolation between development efforts, or if you need to support hotfixes or patches on production code, a strategy that includes a stable production branch such as Gitflow may be more appropriate.
* If you have frequent releases, a strategy that emphasizes continuous integration and delivery, like Trunk-Based Development may be more suitable.

In conclusion, the best branching strategy depends on the specific needs and requirements of your project. You may need to experiment with different strategies and adapt them over time as your project evolves.




