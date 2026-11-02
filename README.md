# JUC SDC (`juc_sdc`)

A modular, framework-agnostic collection of reusable Single Directory Components (SDC) for Drupal 10.3 and Drupal 11.

## Components

- **[Group](components/group/README.md)** (`juc_sdc:group`): Flexible, responsive flexbox layout container supporting responsive directions (`responsive-md`, `responsive-lg`), gaps, alignments, and padding.

## Installation

Add to your Drupal project's custom modules directory (`web/modules/custom/juc_sdc`) or install via Composer:

```bash
composer require juc1/juc_sdc
```

Enable the module via Drush:

```bash
./vendor/bin/drush en juc_sdc -y
```
