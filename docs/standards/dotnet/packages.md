!!! success "We bundle reusable code into NuGet packages."

!!! success "We publish packages to [Nuget.org] from [Github] whenever possible."

!!! info "We host packages that cannot be public on private feeds in [Azure DevOps]."

!!! warning "Some older projects use older packages which are hosted on the private `dotnet-legacy` feed in [Azure DevOps]."

## UoN Packages

!!! info "Our common code packages are all in the `UoN` namespace."

??? summary "Standards for naming packages."
    Packages should be named (and namespaced) based on what they're used for. Sometimes this may make dependencies clear too.

    e.g.

    - Common code for ASP.NET Web API is in the UoN.AspNet.WebApi project
    - Common code for ASP.NET MVC5 would go in UoN.AspNet.Mvc
    - Common code for authentication in ASP.NET Core would go UoN.AspNetCore.Authentication
        - or possibly even further if it was specific to implementing a type of authentication: e.g.  UoN.AspNetCore.Authentication.BasicAuth

??? success "`UoN` Nuget packages target .NET Standard whenever possible."
    Try and target the lowest possible version that you require, in order to maximise compatibility.

    A library should only directly target a .NET implementation (i.e. Framework, Mono or Core) if it requires something that implementation provides that the others (or the netstandard spec) do not.

    This will almost never be true for us.

??? success "Package code lives in its own Git respository."
    Each package should have its own repository.

    - This makes versioning much easier.
    - The repo can contain version controlled documentation for the library.
    - It makes using Unit Test projects for individual libraries easier.

    If there are interdependencies on other `UoN` libraries, their packages (therefore specifically versioned) should be referenced.

!!! success "Packages should always use the `Master Branch Only` Git workflow."

!!! success "Packages are built and released via CI/CD."

## UoN.Common (deprecated)

The `UoN.Common` packages are still available on [Azure DevOps] on the `dotnet-legacy` feed, as they are used by a number of existing applications.

They should be considered deprecated and should not be used in new applications.

If there is code in a `UoN.Common` package that has not been migrated to a new package, then please migrate it before use.

[GitHub]: https://github.com
[Azure DevOps]: https://dev.azure.com/UniversityOfNottingham
[Nuget.org]: https://nuget.org