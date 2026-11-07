# JUC SDC (`juc_sdc`)

A modular, framework-agnostic collection of reusable Single Directory Components (SDC) for Drupal 10.3 and Drupal 11.

## Components

- **[Box](components/box/README.md)** (`juc_sdc:box`): Single-item layout and styling wrapper for positioning (centering, alignment), padding, max-width, background, and borders.
- **[Grid](components/grid/README.md)** (`juc_sdc:grid`): Lightweight, responsive CSS Grid layout container for 1 to 6 equal-width columns and automatic equal-height card rows without page-section overhead.
- **[Group](components/group/README.md)** (`juc_sdc:group`): Flexible, responsive flexbox layout container supporting responsive directions (`responsive-md`, `responsive-lg`), gaps, alignments, and padding.
- **[Section](components/section/)** (`juc_sdc:section`): Powerful CSS Grid page section container supporting 1 to 4 column layouts (`33-33-33`, `25-25-25-25`), header/main/footer slots, backgrounds, margins, and padding.
- **[Icon](components/icon/README.md)** (`juc_sdc:icon`): Accessible SVG icon component supporting the Phosphor icon set, semantic color mapping, sizing presets, and optional link wrapping.
- **[WaveSurfer Audio Player](components/wavesurfer/README.md)** (`juc_sdc:wavesurfer`): Interactive SoundCloud-style audio waveform player powered by WaveSurfer.js with progressive streaming, 15-second skip buttons, and optional file download.

## Installation

Add to your Drupal project's custom modules directory (`web/modules/custom/juc_sdc`) or install via Composer:

```bash
composer require juc1/juc_sdc
```

Enable the module via Drush:

```bash
./vendor/bin/drush en juc_sdc -y
```
