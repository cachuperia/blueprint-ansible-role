# {{ cookiecutter.git_repo_name }}

![checks][checks] ![release][release]

## Table Of Contents

* [About](#about)
* [Usage](#usage)
* [Contributing](#contributing)

## About

{{ cookiecutter.project_short_description }}

## Usage

### Requirements

- Minimum Ansible version: `2.10`

### Role Variables

```yaml
var: default value
```

### Role Tags

- **_tag_** - Description.


### Usage Example

Create `requirements.yml` file:

```yaml
# requirements.yml
roles:
  - src: git+ssh://git@github.com/{{ cookiecutter.github_organization }}/{{ cookiecutter.git_repo_name }}.git
    scm: git
    version: v0.0.0
```

Install role:

```shell
ansible-galaxy install -r requirements.yml
```

Create `playbook.yml`:

```yaml
# playbook.yml
- hosts: servers
  roles:
    - role: {{ cookiecutter.git_repo_name }}
      var: value
```

Run playbook:

```shell
ansible-playbook playbook.yml --extra-vars "ansible_sudo_pass=<sudo password>" --tags "<tag1>,<tag2>" --skip-tags "<tag>"
```

## Contributing

Commit message style - [Conventional Commits][cc].

### Prerequisites

Tools to install: [git][g], [pre-commit][pk], [vagrant][vg] and [detect-secrets][ds].

You can use [this][a] playbook for automated tools installation.

### Setup Local Environment

```shell
git clone git@github.com:{{ cookiecutter.github_organization }}/{{ cookiecutter.git_repo_name }}.git
cd {{ cookiecutter.git_repo_name }}
make init
```

Run `make` to list all available targets.

### Testing

```shell
make test
```

### CD/CI

- `check` GitHub [workflow][wch].
- `release` GitHub [workflow][wr]. Release commit types: `fix`, `feat`.


[a]: https://github.com/IaroslavR/ansible-role-server-bootstrap
[ans]: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-ubuntu
[cc]: https://www.conventionalcommits.org/en/v1.0.0/
[ds]: https://github.com/Yelp/detect-secrets#installation
[g]: https://www.atlassian.com/git/tutorials/install-git
[pk]: https://pre-commit.com/#install
[vg]: https://www.vagrantup.com/

[wch]: .github/workflows/checks.yml
[wr]: .github/workflows/release.yml

[checks]: https://github.com/{{ cookiecutter.github_organization }}/{{ cookiecutter.git_repo_name }}/actions/workflows/checks.yml/badge.svg
[release]: https://github.com/{{ cookiecutter.github_organization }}/{{ cookiecutter.git_repo_name }}/actions/workflows/release.yml/badge.svg

[//]: # (Project cutted from https://github.com/cachuperia/blueprint-ansible-role/tree/v0.1.1)
