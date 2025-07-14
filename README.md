[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/netz98/ddev-webhook-tester/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/netz98/ddev-webhook-tester/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/netz98/ddev-webhook-tester)](https://github.com/netz98/ddev-webhook-tester/commits)
[![release](https://img.shields.io/github/v/release/netz98/ddev-webhook-tester)](https://github.com/netz98/ddev-webhook-tester/releases/latest)

# DDEV Webhook Tester

## Overview

This add-on integrates Webhook Tester into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get netz98/ddev-webhook-tester
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Webhook Tester |
| `ddev logs -s webhook-tester` | Check Webhook Tester logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.webhook-tester --webhook-tester-docker-image="busybox:stable"
ddev add-on get netz98/ddev-webhook-tester
ddev restart
```

Make sure to commit the `.ddev/.env.webhook-tester` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `WEBHOOK_TESTER_DOCKER_IMAGE` | `--webhook-tester-docker-image` | `busybox:stable` |

## Credits

**Contributed and maintained by [@netz98](https://github.com/netz98)**
