!!! tip
    We use two versioning systems. One of them can be considered optional depending on the [Git workflow] in use.

[git workflow]: ./version-control

## Semantic Versioning

!!! success "We use [Semantic Versioning] (&quot;SemVer&quot;)"
    **SemVer** provides application (or API) **versions** that contain **meaningful semantic information** by themselves.

    We use them so that developers, testers and, sometimes, users can compare version numbers and get a sense of the scope of the change.

    They are very much a **public** versioning system intended for **humans**.

!!! summary "SemVer definition"
    SemVer is a 3 part numeric version number, with an optional string label:
    
    `MAJOR.MINOR.PATCH-label`

### The numbers

- Increment `MAJOR` when you make incompatible (breaking) API changes.
    - This is very rare for us in our client-facing applications, but more common in integration APIs and common code libraries.
- Increment `MINOR` when you new features / functionality but remain backwards compatible.
- Increment `PATCH` when you make bug fixes.

### The labels

SemVer allows use of any labels for any purpose

It is common to use `alpha.X` or `beta.X` (where `X` is an incrementing number) to pre-release version packages.

Labels can be useful when deploying early releases from work-in-progress branches, to identify that the build is not intended to go into production.

[semantic versioning]: http://semver.org

## Continuous Versioning

!!! warning "SemVer doesn't work for Continuous Deployment."

    **SemVer** is good practice, and provides useful version information to humans, but it breaks down in continuous release workflows, because the automated tooling responsible for releasing cannot make decisions about how meaningful code changes were, and therefore what effect they should have on a Semantic Version.

    Therefore, in addition to SemVer, we need another versioning system for use with such a workflow.

When we use the **Master Branch Only** Git workflow, we are moving towards a Continuous Deployment attitude, and so any given commit in the `master` branch could be deployed to Production, and therefore **must** be uniquely and identifiably versioned.

Typically, we use our CI system to provide a unique version for a given release; either a build or release number, or a git commit hash, or something similar.

Ideally, applications will be able to report on this version as well as their human-friendly semantic version (which may not change with every release). The CI system should provide this capability.

!!! tip
    Refer to **Guidelines** for versioning (coming soon) for examples of how this has been done on **Master Branch Only** projects to date.

## Version reporting

We should always be able to find out the version of an application we have made, preferably without having to log in, but preferably not publicly visible all the time.

!!! success "Publicly accessibly Version reporting on demand"
    Ideally, the version should be returned on request:
    
    - from a public `/version` endpoint in web apps
    - from a `--version` flag for the rare console apps.
    
    !!! info "The returned version should be at least the SemVer complete with label."
    
    !!! tip "Refer to platform specific Standards and Guidelines for implementing version reporting."

!!! fail "Version reporting in the front-end"
    Our older web apps tend to have a version at the bottom of every page.
    
    This is acceptable for existing applications, but practically speaking most public users don't care what the version of an app is, so we should avoid this method in future.

!!! fail "Version reporting requiring authentication"
    Some of our web apps have a version page at an authenticated route, so we can confirm correct version deployment, but it's frustrating to have to log in.