> 😉 Use gitmoji commit in your workflow

# Gitmoji Commit Workflow

[![Gitmoji][gitmoji]][gitmoji-url] [![lerna][lerna]][lerna-url] [![Build With father][father]][father-url] [![semantic-release][semantic-release]][semantic-release-repo] ![][license-url]

[![Test CI status][test-ci]][test-ci-url] [![Release CI][release-ci]][deploy-ci-url] [![Coverage][coverage]][codecov-url]

<!-- badge -->

[father]: https://img.shields.io/badge/build%20with-father-028fe4.svg
[father-url]: https://github.com/umijs/father/
[lerna]: https://img.shields.io/badge/maintained%20with-lerna-cc00ff.svg
[lerna-url]: https://lernajs.io/
[gitmoji]: https://img.shields.io/badge/gitmoji-%20😜%20😍-FFDD67.svg
[gitmoji-url]: https://gitmoji.carloscuesta.me/
[semantic-release]: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
[semantic-release-repo]: https://github.com/semantic-release/semantic-release
[license-url]: https://img.shields.io/github/license/arvinxx/gitmoji-commit-workflow

<!-- Github CI -->

[test-ci]: https://github.com/arvinxx/gitmoji-commit-workflow/workflows/Test%20CI/badge.svg
[release-ci]: https://github.com/arvinxx/gitmoji-commit-workflow/workflows/Release%20CI/badge.svg
[test-ci-url]: https://github.com/arvinxx/gitmoji-commit-workflow/actions?query=workflow%3A%22Test+CI%22
[deploy-ci-url]: https://github.com/arvinxx/gitmoji-commit-workflow/actions?query=workflow%3A%22Release+CI%22
[coverage]: https://codecov.io/gh/arvinxx/gitmoji-commit-workflow/branch/master/graph/badge.svg
[codecov-url]: https://codecov.io/gh/arvinxx/gitmoji-commit-workflow/branch/master

## What is Gitmoji Commit Workflow?

English(TODO) | [中文](https://www.yuque.com/arvinxx-fe/workflow/gitmoji-commit-workflow)

# Introduction

## Overview

Gitmoji Commit Workflow is a tool designed to streamline and standardize the commit process using Gitmoji. It aims to provide a consistent and visually appealing way to manage commits, making it easier to understand the purpose of each commit at a glance.

## Key Features

- **Standardized Commit Messages**: Enforces a consistent commit message format using Gitmoji.
- **Shareable Configurations**: Provides shareable configurations for commitlint, conventional-changelog, and semantic-release.
- **Helper Packages**: Includes helper packages for parser options, commit types, and Gitmoji regex.

## Installation and Setup

To install and set up Gitmoji Commit Workflow, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/arvinxx/gitmoji-commit-workflow.git
   cd gitmoji-commit-workflow
   ```

2. Install dependencies:
   ```sh
   pnpm install
   ```

3. Configure your project to use the provided packages and configurations.

## Basic Usage

Here are some basic usage examples to get you started:

- **Commitlint Configuration**:
  ```sh
  echo "module.exports = {extends: ['gitmoji']};" > commitlint.config.js
  ```

- **Conventional Changelog Configuration**:
  ```js
  // .releaserc.js
  module.exports = {
    extends: ['semantic-release-config-gitmoji'],
  };
  ```

- **Semantic Release Configuration**:
  ```js
  // .releaserc.js
  const { createConfig } = require('semantic-release-config-gitmoji/lib/createConfig');

  const config = createConfig({ monorepo: true });

  module.exports = config;
  ```

## Template

Refer to this repository to get a [template](https://github.com/arvinxx/gitmoji-commit-workflow-template) of Gitmoji Commit Workflow

## Packages

### Shareable Configuration

Here are some packages for gitmoji commit workflow

| Packages                                                      | Status                                                     | Description                                                                              |
| ------------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| [commitlint-config-gitmoji](packages/commitlint-config)       | [![NPM version][config-image]][config-url]                 | a shareable commitlint configuration to enforcing gitmoji commit                         |
| [conventional-changelog-gitmoji-config](./packages/changelog) | [![NPM version][changelog-image]][changelog-url]           | a shareable conventional-changelog configuration to generate changelog of gitmoji commit |
| [semantic-release-config-gitmoji](packages/release-config)    | [![NPM version][release-module-image]][release-module-url] | a shareable conventional-changelog configuration to generate changelog of gitmoji commit |

[config-image]: http://img.shields.io/npm/v/commitlint-config-gitmoji.svg?style=flat-square&color=deepgreen&label=latest
[config-url]: http://npmjs.org/package/commitlint-config-gitmoji
[config-download]: https://img.shields.io/npm/dm/commitlint-config-gitmoji.svg?style=flat-square
[config-monorepo-image]: http://img.shields.io/npm/v/commitlint-config-gitmoji-monorepo.svg?style=flat-square&color=deepgreen&label=latest
[config-monorepo-url]: http://npmjs.org/package/commitlint-config-gitmoji-monorepo
[config-monorepo-download]: https://img.shields.io/npm/dm/commitlint-config-gitmoji-monorepo.svg?style=flat-square
[changelog-image]: http://img.shields.io/npm/v/conventional-changelog-gitmoji-config.svg?style=flat-square&color=deepgreen&label=latest
[changelog-url]: http://npmjs.org/package/conventional-changelog-gitmoji-config
[changelog-download]: https://img.shields.io/npm/dm/conventional-changelog-gitmoji-config.svg?style=flat-square
[release-module-image]: http://img.shields.io/npm/v/semantic-release-config-gitmoji-module.svg?style=flat-square&color=deepgreen&label=latest
[release-module-url]: http://npmjs.org/package/semantic-release-config-gitmoji-module
[release-module-download]: https://img.shields.io/npm/dm/semantic-release-config-gitmoji-module.svg?style=flat-square

### Helper

| Packages                                                | Status                                     | Description                                          |
| ------------------------------------------------------- | ------------------------------------------ | ---------------------------------------------------- |
| [commitlint-plugin-gitmoji](packages/commitlint-plugin) | [![NPM version][plugin-image]][plugin-url] | a commitlint plugin to add gitmoji check rule        |
| [@gitmoji/parser-opts](./packages/parser-opts)          | [![NPM version][parser-image]][parser-url] | a shareable parser options for gitmoji styles commit |
| [@gitmoji/commit-types](./packages/commit-types)        | [![NPM version][types-image]][types-url]   | gitmoji styles commit types                          |
| [@gitmoji/gitmoji-regex](./packages/gitmoji-regex)      | [![NPM version][regex-image]][regex-url]   | a gitmoji regex                                      |

<!-- npm url -->

[plugin-image]: http://img.shields.io/npm/v/commitlint-plugin-gitmoji.svg?style=flat-square&color=deepgreen&label=latest
[plugin-url]: http://npmjs.org/package/commitlint-plugin-gitmoji
[parser-image]: http://img.shields.io/npm/v/@gitmoji/parser-opts.svg?style=flat-square&color=deepgreen&label=latest
[parser-url]: http://npmjs.org/package/@gitmoji/parser-opts
[types-image]: http://img.shields.io/npm/v/@gitmoji/commit-types.svg?style=flat-square&color=deepgreen&label=latest
[types-url]: http://npmjs.org/package/@gitmoji/commit-types
[regex-image]: http://img.shields.io/npm/v/@gitmoji/gitmoji-regex.svg?style=flat-square&color=deepgreen&label=latest
[regex-url]: http://npmjs.org/package/@gitmoji/gitmoji-regex

## About this Repo

The commitlint gitmoji repo is managed as a [monorepo](https://github.com/babel/babel/blob/master/doc/design/monorepo.md); it's composed of many npm packages.

The original `commitlint-config-gitmoji` repo can be found in [packages/config](packages/commitlint-config).

## License

[MIT](./LICENSE) ® Arvin Xu
