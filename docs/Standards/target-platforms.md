We currently offer three platforms for solutions built by Application Development, and they should be chosen based on project needs:

!!! warning "Each platform's own Standards and Guidelines must be followed."

!!! success "We use .NET Core"
    .NET Core can be used to fulfill the following use cases:

    !!! info "Client-facing Web Applications"
        - ASP.NET Core MVC
    
    !!! info "Application / Integration APIs (over HTTP or WebSocket)"
        - ASP.NET Core MVC (no frontend)

    !!! info "Scheduled tasks (when necessary)"
        - Console application
        
!!! success "We use PHP"
    PHP can be used to fulfill the following use cases:

    !!! info "Client-facing Web Applications"

    !!! info "Application / Integration APIs (over HTTP or WebSocket)"

!!! success "We use SharePoint"
    SharePoint can be used to fulfill the following use cases:

    !!! info "Client facing Office 365 Apps"
        - Client-side Angular application

!!! warning "We use node.js (internal only)"
    Node JS may be used at the Senior Developers discretion for internal projects.

## Legacy platforms

We still support and maintain some older applications on legacy platforms.

!!! danger "New projects MUST NOT target these platforms."

??? fail "Windows Forms, WPF"
    We don't use this anymore because:

    - We prefer to write Web Applications.
    - Supports Windows clients only.

??? fail "ASP.NET 4.x or earlier"
    We don't use this anymore because:

    - ASP.NET Core has succeeded it.
    - It no longer gets adequate security updates and support.

??? fail "ASP.NET WebForms"
    We don't use this anymore because:

    - ASP.NET Core Razor Pages has succeeded it.
    - It no longer gets adequate security updates and support.
    - We have a lack of team expertise in this technology.
    - Code behind convention encourages mixing of presentation and logic
    - ASP.NET Core MVC serves the same use case: Client facing web apps in .NET

??? fail "Windows Communication Foundation (WCF)"
    We don't use this anymore because:

    - We have a lack of team expertise in this technology.
    - ASP.NET Core MVC serves the same use case: Web Services over HTTP or WebSocket

    This could be reconsidered:

    - If we have a need for web services over other transport protocols as per [MSDN][WCF Docs]

??? fail "Classic ASP"
    We don't use this anymore because:

    - ASP.NET Core has succeeded it.
    - It no longer gets adequate security updates and support.
    - We have a lack of team expertise in this technology.

??? fail "Visual BASIC 6"
    We don't use this anymore because:

    - We prefer to write Web Applications.
    - Supports Windows clients only.
    - It no longer gets adequate security updates and support.
    - We have a lack of team expertise in this technology.

??? fail "Java"
    We don't use this anymore because:

    - We have a lack of broad team expertise in this technology.
    - We lack modern processes and workflow in the team for this technology
        - e.g. web frameworks, package management, web servers

 [WCF Docs]: https://msdn.microsoft.com/en-us/library/jj823172