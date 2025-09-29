# 3. Opening a pull request (PR)

🍞 [Outline](../README.md) → 3. Opening a pull request

⚠️ Document status: **Draft**

## Contributing to the original project

When you fork a project, GitHub keeps track of the relationship between the original and the fork. This maintains a pathway for you to contribute your changes if would like to offer an update to the original (as opposed to taking your version in a different direction). 

## What is a pull request?

A pull request (PR)—which may also be called a merge request (MR) in some systems—is an offer to patch the original project. You send your changes in a branch to the maintainer of the original repository for their review. They may accept the PR as-is, request changes, decline with reasons, and so on.

PRs are not a built-in part of the git version control system. Rather they are a social practice of offering to patch the original project for which hosting platforms like GitHub and GitLab have built their own tools. 

PRs don’t have to be made via the source hosting platform (e.g. they may be sent by email), but when working in GitHub it is expected practice to open a pull request.

## Open a PR to the original

*Task: Open a pull request to contribute your work back to the original project.*

Remember to always work in separate branch rather than editing main.

1. Visit your forked repo at `/<your-username>/<project-name>`.
2. Switch to the [branch](1-fork-and-branch.md) that has your [changes](2-edit-and-commit.md) so that you are viewing the README.md file. 
3. Confirm you are viewing the separate branch at `/<your-username>/<project-name>/tree/<branch-name>`.
4. Towards the top-right of the main column you will see two buttons: Contribute and Sync fork. Click **Contribute** then **Open  pull request**.
5. You’ll be taken to a page called **Comparing changes**. Below the title you will see a representation of the proposed changes: 
	- the original project and the branch of it you’re submitting to, 
	- a leftwards arrow pointing to it, and
	- your project and the branch you’re submitting.
6. Write a message to the maintainer. Provide an appropriate title and description. The description may be templated to guide you about what information to provide. Make edits as appropriate and refer to the [GitHub syntax guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) if you need help.
7. Switch to the Preview tab to make sure your message will render correctly.
8. Scroll down below your message to see a summary of the changes you’ll be sending to the project.
9. Make sure “Allow edits by maintainers” is selected and click the **Create pull request** button.
10. You may wish to request a review from a specific individual if that option is available to you. Find their name towards the top right of screen under Reviewers and select it.
11. Finally, you can also tag someone in a comment towards the bottom of your PR or send them a separate message.
	- Use your judgement about the appropriate amount of communication.
	- It is good practice to search for information the maintainer may have already provided about how they prefer to receive PRs.

That’s it! You’ve opened a pull request against the original project.

## Further reading

For more information on pull requests see:

*	[GitHub: Contributing to a project — Git community site](https://git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project)
*	[About pull requests — GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)
