# Contribution Guidelines

Contributions are welcome from anyone who is interested in improving this project and there are multiple ways in which
you can contribute.

Be it code, documentation, or whatever, every contribution helps this project.

## Code of Conduct

GleamyDocker follows the
[GitHub Community Code of Conduct](https://docs.github.com/en/site-policy/github-terms/github-community-code-of-conduct).
By participating in this project, you agree to abide by its terms.

## License

By contributing to this project, you agree that your contributions will be licensed under the
[MIT license](https://github.com/patrik-kuehl/gleamydocker/blob/main/LICENSE.md).

## Code Style Guide

GleamyDocker doesn't come with a strict code style guide. Everything is checked by [Prettier](https://prettier.io/) and
the formatter that comes with Gleam.

You can run `npm run check` to check if everything is formatted accordingly and `npm run format` to run the formatters.

Apart from this, just keep your code readable. Remember, code is read more often than written. Everything else is just a
matter of someone's personal taste, and the heavy usage of opinionated formatters just prevents such (useless)
discussions.

## Git Branching Strategy

This project utilizes the [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow).

Additionally, make sure to rebase onto the remote main branch in case new changes have been merged onto this branch.
This will ensure the Git history is kept flat.

## Commit Messages

This project employs [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

## Changelog

[git-cliff](https://git-cliff.org/) is used to help writing the changelog of this project. Although git-cliff does the
heavy lifting, you should always adjust the content (e.g., changing the tense, or removing entries irrelevant for a
changelog).

You can refer to the [npm scripts](#npm-scripts) section to find out how to update and commit the changelog.

## Development Environment

### Setup

|            Dependency             | Version  |
| :-------------------------------: | :------: |
|    [Gleam](https://gleam.run/)    | \>= 1.1  |
|  [Node.js](https://nodejs.org/)   | \>= 20.0 |
| [Docker](https://www.docker.com/) | \>= 24.0 |
|  [act](https://nektosact.com/)\*  | \>= 0.2  |

You need to run `npm ci` to set up all required npm dependencies. This ensures
[Husky](https://typicode.github.io/husky/) configures all Git hooks and that all npm scripts are executable.

\* act is optional but recommended because act enables you to run the GitHub workflows of this project locally via
Docker before even pushing anything to GitHub.

### npm Scripts

|      Script      |                       Description                       |
| :--------------: | :-----------------------------------------------------: |
|      check       |      checks if everything is formatted accordingly      |
|      format      |                   applies formatting                    |
| update-changelog |                  updates the changelog                  |
| commit-changelog | commits the changelog using a predefined commit message |
