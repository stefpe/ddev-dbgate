[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/stefpe/ddev-dbgate/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/stefpe/ddev-dbgate/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/stefpe/ddev-dbgate)](https://github.com/stefpe/ddev-dbgate/commits)
[![release](https://img.shields.io/github/v/release/stefpe/ddev-dbgate)](https://github.com/stefpe/ddev-dbgate/releases/latest)

# DDEV Dbgate

## Overview

This add-on integrates Dbgate into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get stefpe/ddev-dbgate
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Dbgate |
| `ddev logs -s dbgate` | Check Dbgate logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.dbgate --dbgate-docker-image="ddev/ddev-utilities:latest"
ddev add-on get stefpe/ddev-dbgate
ddev restart
```

Make sure to commit the `.ddev/.env.dbgate` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `DBGATE_DOCKER_IMAGE` | `--dbgate-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@stefpe](https://github.com/stefpe)**
