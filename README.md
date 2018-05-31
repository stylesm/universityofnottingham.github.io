# App Dev Standards

Published docs: [http://dev-docs.nottingham.ac.uk/standards][published site]

## What is this?

This repository is the source of authority for documentation on Standards in App Development.

Refer to `docs/index.md` or the [published site] itself for more information on what's here.

## Why is it here?

It's in a git repo so it can be kept up-to-date and changes can be tracked, and is presented in a way more familiar to developers (unlike Workspace).

Anyone can propose updates or changes (via pull requests) and the Senior Developers can review and approve them, to see them added to the official docs (`master` branch).

## How does it work?

Please use `master` as the source of authority. Any other branch is a work in progress or preserved for historical reasons.

`master` is built using [MkDocs] and hosted by [Caddy] in a [Docker] container on our [Rancher] infrastructure.

For more information about how this works, refer to the [`docker.dev-docs`] repo, or ask the Senior Developers.

# Contributing

We welcome contributions from members of App Dev. These can be corrections, additions, or just suggestions.

1. Read the rest of this contributing section so you know your changes are appropriate.
1. Make a feature branch.
1. Make your changes / additions.
1. Submit a pull request to master, adding Senior Developers as reviewers.
1. Await comments, or approval.

## What should be here?

Information on the following:

- Team Policies on Software Development such as use of unit testing
- Team Processes to follow, such as TAB, code reviews etc.
- Team Standards such as language style guides, tools, frameworks, libraries etc.
- Team Guidance on adhering to the above items, and other recommendations for ways of working

## What should *not* be here?

- Tutorials for the tools we use.
    - While this site specifies tools and frameworks we use as a team, it doesn't go into detail on *how* to use those tools (from a practical perspective; there may be policies which do specify how; e.g. Git Flow is how we use Git as a tool).
    - Actual tutorials and in-depth guidance for tools (such as how to use Bamboo) should be in a separate documentation site (and will be in future).
- Documentation for individual applications
    - Individual applications should have a documentation site of their own e.g. `dev-docs.nottingham.ac.uk/biobanks`
    - Documentation can (should?) be standardised as markdown documents in a repo, available at `dev-docs.nottingham.ac.uk`

## What format should docs be in?

[Markdown]. All Markdown all the time.

- It's readable as source and readable when rendered.
- It's quick and easy to write without learning very much (unlike magic Atlassian fake markdown)
- Many editors provide rendered previews
    - [Visual Studio Code]
    - [Atom]
    - ...
- It's portable if we decide to move it elsewhere.

### Github Flavoured Markdown (GFM)

Mkdocs supports a couple of useful [GFM] features:

- Tables
- Syntax highlighted fenced code blocks

The rest of [GFM] doesn't work with [MkDocs] so we should avoid it.

## Filenames

If you use `kebab-case` filenames, [MkDocs] will replace dashes with spaces and capitalise the title for its navigation.

e.g. `c-sharp-style-guide.md` will appear in the Nav as `C sharp style guide`

Document URLs are based on the filename, so names ened to be URL friendly (e.g. don't use `#` in filenames)

## Images

Images can be added to the repo, provided they're not of a ridiculous size.

Add them to the `docs/images` so they can be easily linked to and will be included in the build

Link to images from a document relative to the document's location.


[published site]: http://dev-docs.nottingham.ac.uk/standards
[Markdown]: https://daringfireball.net/projects/markdown/syntax
[MkDocs]: http://www.mkdocs.org/
[Caddy]: https://caddyserver.com/
[Docker]: https://www.docker.com/
[Rancher]: http://rancher.com/
[`docker.dev-docs`]: https://bitbucket.org/nottinghamuniversity/docker.dev-docs
[Visual Studio Code]: http://code.visualstudio.com/
[Atom]: https://atom.io/
[Github flavoured Markdown]: https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown