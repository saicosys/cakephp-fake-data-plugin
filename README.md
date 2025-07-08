# Saicosys CakePHP 5 Fake data generator plugin

*A lightweight CakePHP 5 plugin to generate and insert fake data into valid models only.*

## Table of contents

[TOC]

## Introduction

`Saicosys/FakeData` is a CakePHP 5 plugin designed to help developers and testers quickly generate and populate fake data into any existing model. It uses the own dummy content to generating realistic test data, while ensuring only valid models are targeted to maintain safety and structure.

## Features

- Smart model detection — only generates data for existing models.
- Fully CLI-based — simple to run with options.
- Supports customizable record count.
- Perfect for local development, testing, and demo environments.

## Use Cases

- Quickly populate your development database.
- Simulate large datasets for performance testing.
- Replace manual data entry with one command.

## Installation

1. Install the Plugin via Composer
You can install the plugin using Composer by running the following command at the root of your CakePHP 5 project:

```bash
composer require saicosys/cakephp-fake-data-plugin --dev
```

2. Load the Plugin

After installation, load the plugin:

```bash
bin/cake plugin load Saicosys/FakeData
```

## Usage

### List available models

```bash
bin/cake fake --list-models
```

### Generate fake data for a model

```bash
bin/cake fake <model> <count>
```

Example:

```bash
bin/cake fake users 10
```

### Preview (dry run) fake data

```bash
bin/cake fake users 5 --dry-run
```

### Specify custom special fields

```bash
bin/cake fake users 10 --special-fields=avatar,logo,thumbnail
```

### Options

- `--list-models, -l` : List available models for fake data generation.
- `--dry-run, -d` : Show what would be generated without saving to the database.
- `--special-fields, -s` : Comma-separated list of additional special fields (e.g., `avatar,logo`).

## License

This plugin is licensed under the MIT License.
