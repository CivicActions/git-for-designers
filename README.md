# Git for designers

⚠️ Document status: **Draft**

## ❓ Project goal

The goal of this project is to help those in non-technical (or not *primarily* technical) roles, such as designers, understand and practice the basics of using Git through collaborative editing of documentation. This repo contains text files and associated media, rather than code.

## 🚙 Main topics

1. [Forking and branching](docs/1-fork-and-branch.md)
	- Fork an existing repo
	- Create a branch in your forked repo
2. [Editing and committing](docs/2-edit-and-commit.md)
	- Make changes using the basic editor
	- Make changes using the online code editor
3. [Opening a pull request to the original project](docs/3-open-pull-request.md)
4. [Syncing your fork once the PR is accepted](4-sync-from-original.md)

### GitHub-only workflow

```mermaid
---
config:
  theme: 'base'
  themeVariables:
    darkMode: 'true'
    background: '#000'
    primaryColor: '#212121'
    primaryTextColor: '#fff'
    primaryBorderColor: '#fff'
    lineColor: '#ccc'
    secondaryColor: '#000'
    tertiaryColor: '#333'
---
flowchart LR
    style GitHub fill:black,color:#fff;
    style Maintainer fill:#212121,stroke-width:3px,stroke:#FA8400,color:#fff;
    style You fill:#212121,stroke-width:3px,stroke:#FF2974,color:#fff;
    style ORIGINAL fill:#303030,stroke-width:3px,stroke:#CCC,color:#fff;
    style FORKED fill:#303030,stroke-width:3px,stroke:#CCC,color:#fff;
    linkStyle default stroke:#fff,color:#fff
    subgraph GitHub
        subgraph You
            direction TB
            subgraph FORKED[Forked repo]
                direction TB
                F_MAIN{{Main branch}}
                F_BRANCH{{Working branch}}
            end
            PR@{ shape: doc, label: "Pull Request" }
        end
        subgraph Maintainer
            direction TB
            subgraph ORIGINAL[Original repo]
                O_MAIN{{Main branch}}
            end
        end
        ORIGINAL ==>|1. Fork the repo| FORKED
        F_MAIN -->|2. Create and edit a branch| F_BRANCH
        F_BRANCH ---|3. Make a PR| PR
        O_MAIN -->|4. Sync the fork| F_MAIN
        PR -.->|merges Working branch| O_MAIN
    end
```

## 🚗 Intermediate topics

5. Working with images
6. Resolving merge conflicts

## 🏎️ Advanced topics

7. Cloning a fork to your local machine
8. Choosing and installing an editor
9. Pushing your branch from local to remote

### Local to GitHub workflow

```mermaid
---
config:
  theme: 'base'
  themeVariables:
    darkMode: 'true'
    background: '#000'
    primaryColor: '#212121'
    primaryTextColor: '#fff'
    primaryBorderColor: '#fff'
    lineColor: '#ccc'
    secondaryColor: '#000'
    tertiaryColor: '#333'
---
flowchart BT
    style GitHub fill:black,color:#fff,stroke-width:3px,stroke:CornflowerBlue;
    style L_MACHINE fill:black,color:#fff,stroke-width:3px,stroke:#FF2974;
    style Maintainer fill:#212121,stroke-width:3px,stroke:#FA8400,color:#fff;
    style You fill:#212121,stroke-width:3px,stroke:#FF2974,color:#fff;
    style ORIGINAL fill:#303030,stroke-width:3px,stroke:#CCC,color:#fff;
    style FORKED fill:#303030,stroke-width:3px,stroke:#CCC,color:#fff;
    style L_CLONE fill:#303030,stroke-width:3px,stroke:#CCC,color:#fff;
    subgraph L_MACHINE[Local machine]
        subgraph L_CLONE[Forked clone]
            direction TB
            L_MAIN{{Main branch}}
            L_BRANCH{{Working branch}}
        end
    end
    subgraph GitHub
        direction TB
        subgraph Maintainer
            subgraph ORIGINAL[Original repo]
                O_MAIN{{Main branch}}
            end
        end
        subgraph You
            subgraph FORKED[Forked repo]
                direction TB
                F_MAIN{{Main branch}} 
                F_BRANCH{{Working branch}}
                PR@{ shape: doc, label: "Pull Request" }
            end
        end
    end
    O_MAIN ===>|1. Fork the repo| F_MAIN
    F_MAIN ==>|2. Clone to local| L_MAIN
    L_MAIN --->|3. Create and edit a branch| L_BRANCH
    L_BRANCH --->|4. Push to remote| F_BRANCH
    F_BRANCH ---|5. Make a PR| PR
    PR -.->|merges Working branch| O_MAIN
    O_MAIN -->|6. Sync the repo| F_MAIN
```

## 📖 Further reading

* [GitHub glossary](https://docs.github.com/en/get-started/learning-about-github/github-glossary)
* [Git reference](https://git-scm.com/docs)
* [Git commmands cheat sheet](https://git-scm.com/cheat-sheet)

## 🙋 Maintainers

* [Adrian Cooke](https://github.com/adriancooke)
* [Daniel Mundra](https://github.com/dmundra)

## ✨ Credits

Special thanks to [Daniel Mundra](https://github.com/dmundra) for assistance.
