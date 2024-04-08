[![tests](https://github.com/Metadrop/ddev-pa11y/actions/workflows/tests.yml/badge.svg)](https://github.com/Metadrop/ddev-pa11y/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2024.svg)

# DDEV Pa11y Add-on <!-- omit in toc -->

* [What is DDEV Pa11y Add-on?](#what-is-ddev-pa11y-add-on)
* [Components of the repository](#components-of-the-repository)
* [Getting started](#getting-started)
* [How to debug in Github Actions](#how-to-debug-tests-github-actions)

## What is DDEV Pa11y Add-on?
This repository provides a [DDEV](https://ddev.readthedocs.io) add-on for the Pa11y service. Pa11y is an automated accessibility testing tool that helps developers make their web applications more accessible.

In DDEV, addons can be installed from the command line using the `ddev get` command, for example, `ddev get Metadrop/ddev-pa11y`.

## Components of the repository

* The fundamental contents of the Pa11y addon. For example, in this template there is a [docker-compose.pa11y.yaml](docker-compose.pa11y.yaml) file.
* An [install.yaml](install.yaml) file that describes how to install the Pa11y service.
* A test suite in [test.bats](tests/test.bats) that makes sure the Pa11y service continues to work as expected.
* [Github actions setup](.github/workflows/tests.yml) so that the tests run automatically when you push to the repository.

## Getting started

1. Install the Pa11y service in your DDEV project by running `ddev get Metadrop/ddev-pa11y`.
2. Start the DDEV project with `ddev start` or `ddev restart`if already started.
3. Run the Pa11y service with `ddev pa11y http://metadrop.net --reporter=junit --standard WCAG2A`.

4. **Contributed and maintained by [@Metadrop](https://github.com/Metadrop)**