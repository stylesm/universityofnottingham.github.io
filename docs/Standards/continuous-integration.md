!!! success "We use [Visual Studio Team Services][VSTS] to automate builds and testing of private repositories."

!!! success "We use [Travis-CI] to automate builds and testing of public repositories."

All projects should have their build tasks completed automatically on pushes to most branches.

- `master` (and `develop` if applicable) must always be built
- all **Pull Requests** must require passing builds.
- Work In Progress branches should be built, unless consciously decided otherwise
    - they should be opt-out, not opt-in

!!! tip "What should CI builds do?"
    CI builds should run all build tasks:

    - Dependency management
    - Linting
    - Compilation
    - Automated testing
    - Preparing deployable artifacts

!!! info "CI builds should use `Release` (or `Production`) configurations as a minimum."
    - The CI server should ensure that code you **plan to deploy** builds and passes tests
    - It's a bonus if it does the same for other configurations

## Deployment

!!! info "We do not use Continuous Deployment, but we deploy via [VSTS]."

Most of our applications are deployed by manually triggering a deployment to an environment on the CI / CD server.

- Deployments to Development environments (from the `develop` or `master` branch) can be continuous.
- Deployments to Test environments should be agreed with the Testing Team. They may be able to be continuous.
- Deployments to Production environments usually depend on gating by our Change Management process.
    - Must be from `master`. Service Management will not approve Production releases from other branches.
    - Ideally we prepare a release to Production once it has passed all other environments.
    - The Service Management Team are then free to approve and schedule deployment of the release once all other conditions have been met.

[VSTS]: https://universityofnottingham.visualstudio.com
[Travis-CI] https://travis-ci.org