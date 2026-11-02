# Icon (`juc_sdc:icon`)

An accessible, customizable icon component rendering SVG icons from the [Phosphor Icons](https://phosphoricons.com) library.

## Origins & Evolution
Originally forked from `byte_theme/components/icon` and enhanced for richer color mapping, link wrapping, and accessibility.

## Features & Enhancements over `byte_theme/components/icon`
1. **Semantic Color Mapping**:
   - `byte_theme` only accepted a raw string `icon_color` defaulting to `currentColor`.
   - `juc_sdc:icon` supports semantic theme color tokens: `current`, `primary`, `secondary`, `accent`, `neutral`, `muted`, `destructive` (mapped to Tailwind / daisyUI CSS variables like `var(--color-primary)` and utility classes `text-primary`).
   - Backward compatibility: direct `icon_color` override is still accepted.
2. **Optional Link Wrapper**:
   - Wrap the icon in an `<a>` tag by supplying `url` (or `href`/`link`).
   - Configurable link target (`target: _self` or `_blank`). Automatically adds `rel="noopener noreferrer"` for `_blank`.
3. **Accessibility**:
   - Dedicated `alt` prop.
   - When wrapped in a link, `alt` becomes an accessible `aria-label`.
4. **Size Options**:
   - Supports: `extra-extra-small` (16px), `extra-small` (20px), `small` (24px), `medium` (32px), `large` (48px), and `extra-large` (64px).

## Usage in Twig

```twig
{# Simple icon #}
{% include 'juc_sdc:icon' with {
  icon: 'play-fill',
  icon_size: 'small',
  color: 'primary'
} %}

{# Linked icon with accessible label #}
{% include 'juc_sdc:icon' with {
  icon: 'download-simple',
  icon_size: 'medium',
  url: 'https://example.com/file.mp3',
  target: '_blank',
  alt: 'Download episode audio'
} %}
```
