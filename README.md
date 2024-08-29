# sdk-examples

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

Code examples for JPYC Node SDKs

## 🌈 Available Code Examples

Please refer to `README`s of each SDK for the version specific details.

| SDK Version | `README`                               |
| ----------: | :------------------------------------- |
|        `v1` | [packages/v1](./packages/v1/README.md) |

## 🔨 Development

### Git Submodules

This repo uses [Git Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to be in sync with [JPYCv2](https://github.com/jcam1/JPYCv2/tree/main) repo.

To include submodules when cloning the repo, add `--recursive` option like below.

```sh
$ git clone --recursive https://github.com/jcam1/sdk-examples.git
```

### Yarn Workspaces

This repo uses [Yarn Workspaces](https://yarnpkg.com/features/workspaces) primarily as a monorepo management tool. Please refer to the inserted link for details.

> [!NOTE]
> Please use Node `v20.12.0` for this repo.

To install dependencies for all the workspaces, run the following.

```sh
# cd into this repo
$ cd sdk-examples
# Install dependencies
$ yarn
```

### Yarn Scripts

To run yarn scripts defined in workspaces, run the following.

```sh
$ yarn workspace ${workspace_name} run ${command_name}
```

### Dependencies

To add dependencies, run one of the following. To prevent unexpected behaviors, always pin the exact versions of the dependencies to be installed.

```sh
# Add dependencies to the specified workspace
$ yarn workspace ${workspace_name} add -E ${dependencies}

# Add dev dependencies to the specified workspace
$ yarn workspace ${workspace_name} add -E -D ${dependencies}

# Add dev dependencies to the workspaces root
$ yarn add -E -D -W ${dependencies}
```

To remove dependencies, run one of the following.

```sh
# Remove dependencies from the specified workspace
$ yarn workspace ${workspace_name} remove ${dependencies}

# Remove dependencies from the workspaces root
$ yarn remove -W ${dependencies}
```
