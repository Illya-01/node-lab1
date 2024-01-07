# Lab 1

## Goals

- setup environment

## Task

Create project in GitHub with minimal code-quality checks and auto deploy.

### Requirements

- new repo in GitHub ✅
- initial empty commit ✅
- add ESlint (as strict as possible using `extends: 'eslint:all'`) ✅
- add Sonar-Lint to ESLint ✅
- add Prettier ✅
- Add check on pre-commit hooks ✅
- Add GitHub action to run checks\tests on commit or PR ✅
- Add AutoDeployment to any hosting provider ([I used Vercel](https://node-lab1-roan.vercel.app/)) ✅
- Add Editorconfig ✅
- Bonus: the same with TypeScript [I don't use TS]
- Bonus: SonarCloud, https://github.com/SonarSource/sonarcloud-github-action [I don't use TS]

## Questions

- dev Deps vs Deps:
  - dependencies are the packages that everyone runs or when a project is deployed, like Express.
  - devDependencies are packages that are only needed during development, like nodemon, ESlint, Prettier, Jest etc.
- Why we have separate tooling for formatting/linting:
  - Formatting is used to make the code look consistent and more readable.
  - Linting is used to analyze code for potential errors, bugs, and code quality issues.
- Difference with VPS/FaaS?
  - VPS is a virtual private server that can used to host an application. We have to configure everything by ourselves.
  - FaaS is a serverless architecture. We don't have to configure anything, just write code and deploy it.
    It's cheaper and easier to use.
- Why we need peerDeps?
  - Peer dependencies are a special type of dependency that would only ever come up if we are to publish our own package/module/library.
    They are dependencies that our module needs in order to work, but which will be installed by whoever is using our module.
- `npm i` vs `npm ci`
  - `npm i` installs all dependencies and devDependencies, modifying package.json, package-lock.json, and node_modules folder.
  - `npm ci` ("clean install") deletes the node_modules folder and installs exactly what's in the package-lock.json for consistency.
