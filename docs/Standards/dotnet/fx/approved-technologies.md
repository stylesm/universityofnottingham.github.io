!!! danger ".NET Framework is no longer an approved target platform."

    **.NET Core** should now take precedence.
    
    The **Senior Developers** will only approve the use of **.NET Framework** for projects that require it.

!!! info "Approved Technologies"
    The Senior Developers have discussed and chosen certain frameworks, libraries and technologies that we prefer to use as a solution for a given need or problem.

    Please consult this list when you are looking to solve a problem in your application, to see if we have a preferred way of doing things.

    This list can be debated and must evolve, but to see new technologies used or approved, the Senior Developers must be consulted and a case must be made.

## Technologies by use case

!!! tip "These use cases include"
    !!! success "approved technologies"
    !!! info "notes on optional supporting libraries"
    !!! warning "legacy technologies you might come across, but mustn't use on new apps."

??? summary "Active Directory User Authentication"
    !!! success "ASP.NET Identity 2.x"
    !!! info "UoN libraries for authentication and authorisation"

??? summary "Local User Accounts"
    !!! success "ASP.NET Identity 2.x"
    !!! success "Entity Framework 6.x"
    !!! info "UoN libraries for authentication and authorisation"

??? summary "SQL Server Database ORM"
    !!! success "Entity Framework 6.x"
        Use **Code First Migrations** for new projects
    !!! warning "NHibernate"
    !!! warning "Dapper"

??? summary "Inversion of Control (IoC) / Dependency Injection (DI)"
    !!! success "Castle.Windsor 3.x"
    !!! info "UoN libraries for dependency resolution"

??? summary "Scheduled Tasks"
    !!! success "Hangfire"

??? summary "Queued Tasks"
    !!! success "Hangfire"

??? summary "Email sending"
    !!! success "Postal MVC5"

??? summary "Error Logging"
    !!! success "Elmah"

??? summary "Unit Testing"
    !!! success "NUnit 3.x"
    !!! info "Moq"
    !!! warning "NUnit 2.x"

??? summary "JSON"
    !!! success "Newtonsoft.JSON"

??? summary "Profiling"
    !!! success "Glimpse"
        Has a plugin for Elastic Search too.

??? summary "Image Processing"
    !!! success "ImageResizer"

??? summary "Sitemaps / Breadcrumbs"
    !!! success "MVC Sitemap"

??? summary "Object mapping"
    !!! success "AutoMapper"
        e.g. ViewModels -> DTOs -> Entities or vice versa

??? summary "Reading / writing CSV files"
    !!! success "CsvHelper"