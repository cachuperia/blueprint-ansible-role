# blueprint-general

![checks][checks] ![release][release]

## Table of contents

* [About](#about)
* [Usage](#usage)
* [Contributing](#contributing)

## About

Basic language agnostic repo template for [cookiecutter][cook].

## Usage

```shell
cookiecutter https://github.com/cachuperia/blueprint-general
```

## Contributing

Commit message style - [Conventional Commits][cc].

### Prerequisites

Tools to install: [git][g], [pre-commit][pk], and [detect-secrets][ds].

You can use [this][a] playbook for automated tools installation.

### Setup local environment

```shell
git clone git@github.com:cachuperia/blueprint-general.git
cd blueprint-general
make init
```

Run `make` to list all available targets.

[a]: https://github.com/cachuperia/ansible-role-server-bootstrap
[cc]: https://www.conventionalcommits.org/en/v1.0.0/
[ds]: https://github.com/Yelp/detect-secrets#installation
[g]: https://www.atlassian.com/git/tutorials/install-git
[pk]: https://pre-commit.com/#install
[cook]: https://cookiecutter.readthedocs.io/en/stable/

[wch]: .github/workflows/checks.yml
[wr]: .github/workflows/release.yml

[checks]: https://github.com/cachuperia/blueprint-general/actions/workflows/checks.yml/badge.svg
[release]: https://github.com/cachuperia/blueprint-general/actions/workflows/release.yml/badge.svg
