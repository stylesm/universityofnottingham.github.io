!!! tip
    We use two versioning systems. One of them can be considered optional depending on the [Git workflow] in use.

[git workflow]: ./version-control

## Semantic Versioning

!!! success "We use [Semantic Versioning] (&quot;SemVer&quot;)"
    **SemVer** provides application (or API) **versions** that contain **meaningful semantic information** by themselves.

    We use them so that developers, testers and, sometimes, users can compare version numbers and get a sense of the scope of the change.

    They are very much a **public** versioning system intended for **humans**.

!!! summary "A summary of Semantic Versioning"
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

## Version discovery

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