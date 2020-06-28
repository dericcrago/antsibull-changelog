# antsibull-changelog -- Ansible Changelog Tool

A changelog generator used by Ansible and Ansible collections.

- Using the
  [`antsibull-changelog` CLI tool](https://github.com/ansible-community/antsibull-changelog/tree/main/docs/changelogs.rst).
- Documentation on the
  [`changelog.yaml` format](https://github.com/ansible-community/antsibull-changelog/tree/main/docs/changelog.yaml-format.md).

## Installation

It can be installed with pip:

    pip install antsibull-changelog

For more information, see the
[documentation](https://github.com/ansible-community/antsibull-changelog/tree/main/docs/changelogs.rst).

## Using directly from git clone

Scripts are created by poetry at build time.  So if you want to run from
a checkout, you'll have to run them under poetry:

    python3 -m pip install poetry
    poetry install  # Installs dependencies into a virtualenv
    poetry run antsibull-changelog --help

If you want to create a new release:

    poetry build
    poetry publish  # Uploads to pypi.  Be sure you really want to do this

Note: When installing a package published by poetry, it is best to use pip >= 19.0.
Installing with pip-18.1 and below could create scripts which use pkg_resources
which can slow down startup time (in some environments by quite a large amount).

## License

Unless otherwise noted in the code, it is licensed under the terms of the GNU
General Public License v3 or, at your option, later. See
[LICENSE](https://github.com/ansible-community/antsibull-changelog/tree/main/LICENSE)
for a copy of the license.
