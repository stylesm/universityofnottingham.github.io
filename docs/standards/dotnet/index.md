!!! success "We use the latest stable version of C#."

!!! success "We target .NET Standard and .NET Core whenever possible."

!!! success "We follow the [JavaScript] and [CSS] standards when working with frontend code in a .NET environment."

!!! success "We maintain a list of approved technologies that solve common domain problems."
    
    **Approved Technologies:** [.NET Core](./core/approved-technologies.md) | [.NET Framework](./fx/approved-technologies.md)

    !!! fail "Don't reinvent the wheel."
        Check the list to see if your problem is already solved; if not, still investigate third party libraries.
    !!! fail "Don't proliferate technologies unnecessarily."
        Don't introduce a new technology that solves a problem that's already solved on the list.

!!! fail "We don't specify complex rules. Our tooling configurations do that for us."

!!! fail "We don't write new code in other CLR Languages, such as Visual BASIC or F#."

!!! danger "We have legacy applications written in VB.NET, or Classic VB."

## Tooling

!!! success "Use the latest stable version of [Visual Studio]."

!!! success "Use [Resharper] to automatically enforce and check code quality."

!!! tip "Working with older projects."
    - Upgrade the version of Visual Studio to the latest stable when possible
    - Feel free to use new language features once upgraded
        - But be consistent with the rest of the application where necessary
    - Consider everyone (or everything) that builds the project.
        - e.g. Make sure CI tools know how to build the new version.

## Doc Comments

!!! success "Use [XML Doc Comments] for doc commenting."

!!! success "Use [Swagger] with Swashbuckle for building and serving API documentation."

## Unit Testing

!!! info "Unit Testing is encouraged but not yet mandated."

!!! success "We use [XUnit] for unit testing."

!!! warning "Some older .NET Framework applications have unit tests in [Nunit] 2.x or 3.x."

[JavaScript]: ../javascript.md
[CSS]: ../css.md
[XML Doc Comments]: https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments
[Swagger]: https://swagger.io/
[Resharper]: https://www.jetbrains.com/resharper/
[Visual Studio]: https://visualstudio.com
[XUnit]: https://xunit.github.io/
[NUnit]: http://nunit.org/