!!! info "What are Policies?"
    **Policies** are brief formal statements that describe a mandatory action or behaviour, along with its purpose and desired results.

    The [homepage] has a glossary of associated terms.

## 1. Code Quality and Style

??? success "1.0.1 We write high quality code."
    Ensuring the **quality** of our code is both **consistent** and to a **high standard** makes the following easier:

    - To have confidence that our code will perform as expected.
    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.

??? success "1.0.2 We write code in a consistent style."
    Ensuring the **style** of our code is both **consistent** and **follows accepted conventions** makes the following easier:

    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.
    - For third party documentation and guidance to be more likely to be directly useful.

??? success "1.0.3 We use tooling to enforce quality and style."
    Ensuring we use **tooling** and **automated processes** wherever possible to enforce **code quality** and **style** makes the following easier:

    - To be confident that quality and style will be as intended.
    - To avoid having to manually document quality and style rules.
    - To avoid having to manually ensure code meets quality and style rules.
    - To avoid arguments over quality and style rules.

### 1.1 Code Comments

??? success "1.1.1 We use doc comments to document code."
    Ensuring we use **conventional documentation comments** wherever possible makes the following easier:

    - To be confident our code's behaviour and intention is well understood.
    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.
    - To produce API documentation sites automatically.

??? success "1.1.2 We use task comments to indicate work to be done."
    Ensuring we use **task comments** such as `TODO:` and `HACK:` to indicate **work to be done** makes the following easier:

    - To track work to be done at a location within the codebase. Many editors support highlighting or listing outstanding tasks.
    - To indicate why a sub-optimal or questionable practice is temporary.

??? success "1.1.3 We use code comments to explain unexpected or complex behaviour."
    Ensuring we use **comments** to document **unexpected** behaviour, **unconventional (but necessary)** approaches, or **complex** code makes the following easier:

    - To be confident our code's behaviour and intention is well understood.
    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.

??? fail "1.1.4 We don't comment code where behaviour is clear."
    Ensuring we **don't comment** code where the code's **behaviour and intention** are **already clear** makes the following easier:

    - To read large methods which have clear, readable behaviour. Unnecessary comments would provide noise.
    - To save time. No need to type an explanation for something that is self-explanatory.
    - To encourage clear code. Good code is self-documenting (to a degree) and so developers should try and write code that is clear enough without comments whenever possible.

### 1.2 Structure

??? success "1.2.1 We follow common conventional architectural structures, like MVC."
    Ensuring our **applications** are **structured** architecturally following **common conventions**, such as **MVC** and its derivatives, makes the following easier:

    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.

## 2. Target Platforms

??? success "2.1 We target a specific limited set of approved platforms."
    Ensuring we write code for a specific set of approved platforms makes the following easier:

    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.
    - To focus training needs within the confines of those platforms.
    - To avoid unnecessary proliferation of technologies.

??? success "2.2 We build web apps."
    Ensuring we build **web applications** whenever possible makes the following easier:
    
    - To avoid dependencies on specific client runtime environments.
    - To avoid the need to update the application to work with newer or different client runtime environments.

## 3. Source / Version Control

??? success "3.1 We use a distributed version control system."
    Ensuring we use a **distributed version control** system to **manage our codebase** makes the following easier:

    - To be confident that code changes are broken down into small manageable chunks.
    - To be comfortable making experimental code changes in isolation from the stable branch.
    - To manage the release of changes to production.
    - To be confident that code is in multiple locations, with no single point of failure to cause loss of work.

??? success "3.2 We use a clearly defined branching workflow."
    Ensuring we use a **clearly defined** and conventional **branching workflow** makes the following easier:

    - To manage the release of changes to production.
    - For any developer (even those not familiar with the codebase) to maintain the code, or extend it.

## 4. Versioning

??? success "4.1 We use a clearly defined versioning system that conveys semantic information."
    Ensuring we use a **clearly defined** system for **versioning** software that conveys **semantic information** about the **changes** in a version makes the following easier:

    - For developers to know when to version bump software, and to what version.
    - For people to understand the implications of a change from one version to another.


??? success "4.2 We use a clearly defined versioning system suitable for continuous releases."
    Ensuring we use a **clearly defined** system for **versioning** software that is suitable for **continuous releases** makes the following easier:

    - For developers and testers to refer to a specific release, regardless of whether it is otherwise semantically different to another release.
    - For automated tooling to appropriately version releases.

## 5. Code Reviews

??? success "5.1 We peer review code changes."
    Ensuring we **peer review code changes** makes the following easier:

    - To be confident that code is meeting **Standards** and complying with **Policies**.
    - To discuss and advise on implementations or designs.
    - To share knowledge between team members.
    - To ensure implementations are appropriate for a given project's requirements.

??? success "5.2 We support reviews with automated tooling."
    Ensuring that we use **automated tooling** to assist with **code reviews** makes the following easier:

    - For developers to not manually have to check that code is compliant with **Policies**.
    - To be confident that the code is in a state to be reviewed and merged.

## 6. Continuous Integration

??? success "6.1 We use Continuous Integration services to regularly build code."
    Ensuring that we **regularly build** changes to **our code** using **automated services** makes the following easier:

    - For developers to be confident that their changes build.
    - To avoid the need to manually run builds regularly, or for reviews.
    - To be confident of the quality of delivered releases.

??? success "6.2 We use Continuous Integration services to run tests automatically."
    Ensuring that we **automatically test** changes to **our code** whenever we **build** it makes the following easier:

    - For developers to be confident that their changes have not broken tests.
    - To avoid the need to manually run tests for reviews.
    - To be confident of the quality of delivered releases.

??? success "6.3 We use Continuous Integration services to release software."
    Ensuring that we **release our software** using the **same automated tools** we used to **build and test** makes the following easier:

    - To be confident we are releasing the exact same code that was successfully built and tested.
    - To avoid manual steps in releases.
    - To guarantee that repeatable release tasks are done the same way every time.
    - To provide a clear audit trail of releases to environments, of specific code versions.
    - To be confident of the quality of delivered releases.

[homepage]: index.md