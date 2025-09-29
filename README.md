# Git for designers

⚠️ Document status: **Draft**

## Description

The goal of this project is to help those in non-technical (or not *primarily* technical) roles, such as designers, understand and practice the basics of using Git through collaborative editing of documentation. This repo contains text files and associated media, rather than code.

## Main topics to be covered

1. [Forking and branching](docs/1-fork-and-branch.md)
	- Fork an existing repo
	- Create a branch in your forked repo
2. [Editing and committing](docs/2-edit-and-commit.md)
	- Make changes using the basic editor
	- Make changes using the online code editor
3. [Opening a pull request to the original project](docs/3-open-pull-request.md)
4. Syncing your fork once the PR is accepted

```mermaid
graph TD
    subgraph GITHUB
        ORIGINAL_REPO["Original Repo<br>Project on GitHub"]
        FORK[Fork]
        PULL_REQUEST["Pull Request<br>How you contribute your changes"]
    end

    subgraph YOUR_BROWSER
        BROWSER_BRANCH[Branch]
        URL("https://github.com/username/repo/tree/branch")
    end

    ORIGINAL_REPO -- "Your GitHub Account" --> FORK
    FORK --> BROWSER_BRANCH
    BROWSER_BRANCH -- "Make Changes" --> BROWSER_BRANCH
    BROWSER_BRANCH --> PULL_REQUEST
    PULL_REQUEST -.-> ORIGINAL_REPO
```

## Advanced topics

1. Cloning a fork to your local machine
2. Choosing and installing an editor
3. Pushing your branch from local to remote

```mermaid
graph TD
    subgraph GITHUB
        ORIGINAL_REPO["Original Repo<br>Project on GitHub"]
        FORK[Fork]
        PULL_REQUEST["Pull Request<br>How you contribute your changes"]
    end

    subgraph YOUR_COMPUTER
        LOCAL_CLONE[Local Clone]
        BRANCH[Branch]
    end

    ORIGINAL_REPO -- "Your GitHub Account" --> FORK
    FORK --> LOCAL_CLONE
    LOCAL_CLONE -- "Make Changes" --> BRANCH
    BRANCH --> PULL_REQUEST
    PULL_REQUEST -.-> ORIGINAL_REPO
```

## Maintainers

* [Adrian Cooke](https://github.com/adriancooke)
* [Daniel Mundra](https://github.com/dmundra)

## Credits

Special thanks to [Daniel Mundra](https://github.com/dmundra) for assistance.
