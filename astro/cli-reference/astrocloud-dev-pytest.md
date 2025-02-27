---
sidebar_label: "astrocloud dev pytest"
title: "astrocloud dev pytest"
id: astrocloud-dev-pytest
description: Reference documentation for astrocloud dev pytest.
---

## Description

Run unit tests for your data pipelines on Astro with `pytest`, a testing framework for Python. When you run this command, the Astro CLI creates a local Python environment that includes your DAG code, dependencies, and Astro Runtime Docker image. The CLI then runs any pytests in the `tests` directory of your Astro project and shows you the results of those tests in your terminal.

For more information on this functionality, see [Test and Troubleshoot Locally](test-and-troubleshoot-locally.md).

:::info

This command requires Astro Runtime version `4.1.0`+. For more information, see [Astro Runtime Release Notes](https://docs.astronomer.io/astro/runtime-release-notes#astro-runtime-410).

:::

## Usage

```sh
astrocloud dev pytest
```

## Options

| Option              | Description                                                                                   | Possible Values                                 |
| ------------------- | --------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| `<pytest-filepath>` | The filepath to an alternative pytest file or directory. Must be within the `tests` directory | Any valid filepath within the `tests` directory |
| `-e`, `--env`       | The filepath to your environment variables. The default is `.env`)                            | Any valid filepath within your Astro project    |

## Examples

```sh
$ astrocloud dev pytest --env=myAlternativeEnvFile.env
# Specify env file at root of Astro project
```

## Related Commands

- [`astrocloud dev init`](cli-reference/astrocloud-dev-init.md)
- [`astrocloud dev start`](cli-reference/astrocloud-dev-start.md)
- [`astrocloud deploy`](cli-reference/astrocloud-deploy.md)
