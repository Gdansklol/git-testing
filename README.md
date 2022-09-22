# Understanding GitHub Actions

## Overview
> GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline. You can create workflows that build and test every pull request to your repository, or deploy merged pull requests to production.

GitHub Actions goes beyond just DevOps and lets you run workflows when other events happen in your repository. For example, you can run a workflow to automatically add the appropriate labels whenever someone creates a new issue in your repository.

GitHub provides Linux, Windows, and macOS virtual machines to run your workflows, or you can host your own self-hosted runners in your own data center or cloud infrastructure.

# What are Git Hooks?
> Git hooks are scripts that you can set up to run at certain events in the Git lifecycle. These events include different stages of a commit, like before a commit (pre-commit) and after a commit (post-commit).

These are useful in that they allow developers to run custom code tasks or even enforce standards by automating other scripts to run those tasks.

# Hwat is Husky?
> Husky is a tool that allows us to easily wrangle Git hooks and run the scripts we want at those stages.

It works by including an object right within our package.json file that configures Husky to run the scripts we specify. After that, Husky handles managing at which point in the Git lifecycle our scripts will run.

# Manual
## Install

1. Instll husky
```
npm install husky --save-dev
```

2. Enable Git hooks

>  npx husky install

3. To automatically have Git hooks enabled after install, edit package.json

```
npm pkg set scripts.prepare "husky install"
```

You sholud have :

```
// package.json
{
  "scripts": {
    "prepare": "husky install"
  }
}

```


