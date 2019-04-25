# Contributing to Cypherblock

Welcome, and thank you for your interest in contributing to Cypherblock!

Here are steps by steps guiding you to contribute your code to Cypherblock repo

## Prerequisites

You'll need the following tools to download and build Cypherblock locally:

- [Git](https://git-scm.com)
- [Node.JS](https://nodejs.org/en/), version `>=10.10.0 <=11.11.0`
- [Yarn](https://yarnpkg.com/en/), follow the [installation guide](https://yarnpkg.com/en/docs/install)
- [VSCode](https://code.visualstudio.com/) (Recommened)
  - [ESLint](https://github.com/Microsoft/vscode-eslint)
  - [Prettier - Code formatter](https://github.com/prettier/prettier-vscode)

## Setting Up a Development Environment

To prepare for contributing to Cypherblock project, you'll need to setup your own local development environment: Get the sources, build it, config some parameters, and run it locally.

### Getting the sources

First, [fork](https://help.github.com/en/articles/fork-a-repo) the [Cypherblock repository](https://github.com/Cypherman1/cypherblock-eos) so that you can make a pull request. Then, clone your fork locally:

```
git clone https://github.com/<<<your-github-account>>>/cypherblock-eos.git
```

### Build

Install and build all of the dependencies using `Yarn`:

```
cd cypherblock-eos
yarn
```

### Configuring

Get a [Coinmarketcap API Key](https://coinmarketcap.com/api/)

Locate the file `./src/server/config/dev.js` and config the parameters:

```
module.exports = {
  chainURL: 'https://eos.greymass.com',//Change to your favorite BP API end point
  chainURL_ALT1: 'https://mainnet.eoscanada.com',//Change to your favorite BP API end point
  historyURL: 'https://eos.greymass.com',//Change to your favorite BP API end point
  mongoHistoryURL: 'https://history.cryptolions.io',
  cmcAPIKey: '18edf1e2-6d7d-4c5a-82fe-bde94fc02e61' //Change to your own Coinmarketcap API Key
};
```

### Run

To start the development server, run:

```
yarn dev
```

Give a minute for the server to start and go to [http://localhost:3000](http://localhost:3000)

## Contributing

Now, It's time to write your code and contribute to Cypherblock repo

### Work Branches

Before writing your code, you should create a personal fork and create feature branches there when you need them. This keeps the main repository clean and your personal workflow cruft out of sight.

```
git checkout -b your_branch_name
```

### Write your code

:honeybee: :ok_hand:

### Pull Requests

Merge changes in the upstream repository (the official Cypherblock repo) with your local clone off your fork

```
git checkout master
git pull https://github.com/Cypherman1/cypherblock-eos master
```

Merge your branch to master, manage any conflicts, commit them and push to your fork

```
git checkout your_branch_name
git rebase master
git push --set-upstream origin your_branch_name
```

Finally, go to GitHub and [Make a Pull Request](https://help.github.com/en/articles/creating-a-pull-request) :D

Ensure the changesets you introduced are included. Fill in some details about your potential contributions including a meaningful title. The Cypherblock core team will be notified about your submission.

# Thank You!

Your contributions to open source, large or small, make great projects like this possible. Thank you for taking the time to contribute.
