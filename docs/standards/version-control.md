!!! success "We use Git"
    Current applications should be version controlled in Git.

    !!! info "Where are our Git repositories?"
        
        - [Visual Studio Team Services] hosts our private git repositories
        - [GitHub] hosts any public repositories.

[Visual Studio Team Services]: https://universityofnottingham.visualstudio.com
[GitHub]: https://github.com/universityofnottingham

## Git workflows

We use two branch workflows for Git, depending on the needs of the project.

!!! success "We always use Pull Requests to merge into important branches."

!!! tip "Which flow should I use?"
    
    - Use **Master Branch Only**
        - If you're starting a new project
            - Unless you've explicitly agreed with Senior Developers that **Git Flow** should be used.
        - If you agree with the Senior Developers that it's time to transition the project to **Master Branch Only**.
    - Use **Git Flow**
        - If your project already uses **Git Flow** (i.e. it has a `develop` branch).

### Master Branch Only

This workflow is simpler, and is based on [GitHub Flow] but has some caveats around the fact we don't continuously deploy to Production.

!!! tip "For more detailed guidance, refer to the **Guidelines** and **Processes** sections for Git (coming soon)."

??? warning "Your project must support versioning suitable for continuous release when using this workflow."
    Code that can be released from a single continuously integrated `master` branch must be able to automatically uniquely version a given code commit.
    
    Refer to [versioning] for more information.

- The `master` branch always contains the latest integrated version of the code.
    - `master` is a protected branch, and can only acquire code via a pull request
    - Releases to Production must come from `master`.
    - Commits on `master` should always be considered safe to deploy.

All other branches are work-in-progress branches. When work is complete:

- A version bump may occur, if the changes are meaningful enough to warrant it.
- A Pull Request is raised and reviewed
    - merged into `master`, if review passes.
- All merges to master undergo automated builds and testing before and after they get there.
- They subsequently deploy to any number of pre production environments, for as many stages of testing as are necessary.
- Approval on an environment allows deployment to the next environment, up until Production.
- Release to Production is optional, but a release can be made from any merge to `master`.

[GitHub Flow]: https://guides.github.com/introduction/flow/
[versioning]: ./versioning

### Git Flow

Most of our projects use the popular [Git Flow] workflow, which details a sensible branching and merging model.

!!! warning "We have slightly modified Git Flow to accomodate our Pull Request standards."

!!! tip "For more detailed guidance, refer to the **Guidelines** and **Processes** sections for Git (coming soon)."

- The `master` branch is either your initial commit (`readme.md`, `.gitignore`) or the current production verion of the code.
    - `master` is a protected branch, and can only acquire code via a pull request
    - Releases to Production must come from `master`.
    - Releases to environments must be version tagged e.g. `1.6.0`
- The `develop` branch represents the code that will be going into the next release branch, whenever that happens
    - `develop` is a protected branch, and can only acquire code via a pull request
- `release` branches are for preparing a release to test or production.
    - Create a `release` branch when all development for a new release is finished and included in `develop`
    - Use the `release` branch only to prepare for Production. The only changes on `release` branches should be bug fixes found during testing and changes to version numbering.
    - Releases to Test environments must come from a `release` branch
    - `release` branches should be named after the version they are preparing e.g. `1.7.0`
    - Releases to environments must be tagged e.g. `1.7.0-beta1`
    - When a release is ready for production:
        - Make a pull request to merge to `develop`
        - Make a pull request to merge to `master`
        - Your `release` branch will then be code reviewed
- `feature` branches are for adding features or fixing bugs to go into the next version
    - Create a `feature` branch when you start work on a specific task
    - If there is a JIRA issue for the feature, put it in the branch name
    - Only do work for this specific task in this branch.
    - When you have completed the development work for the task:
        - Make a pull request to merge to `develop`
        - Your `feature` branch will then be code reviewed
- `hotfix` branches are for fixing urgent bugs to Production
    - Create a `hotfix` branch when you start work on the bug
    - Only fix the bug in question
    - When you have completed the development work for the bug:
        - Make a pull request to merge to `master`
        - Make a pull request to merge to `develop`
        - Your `hotfix` branch will then be code reviewed

[Git Flow]: https://nvie.com/files/Git-branching-model.pdf

## Legacy applications

Some legacy applications are still in [SVN] or Visual SourceSafe.

If any work is ever done on these applications, their source must be migrated to an appropriate Git repo.

[SVN]: http://svn.nottingham.ac.uk