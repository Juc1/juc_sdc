# Icon Text (`juc_sdc:icon-text`)

A reusable Single Directory Component that displays an inline icon alongside a text label or clickable link. Ideal for contact details, addresses, phone numbers, email links, and feature callouts.

## Features
- **Phosphor Icon Support**: Directly integrates with `juc_sdc:icon` and any Phosphor icon name (`map-pin`, `phone`, `envelope`, `clock`, `check`, etc.).
- **Optional Link**: When `url` is provided (e.g. `tel:...`, `mailto:...`, or web URL), the text automatically wraps in an accessible, hover-styled link.
- **Semantic Colors**: Supports DaisyUI semantic color variables (`primary`, `secondary`, `accent`, `neutral`, `inherit`).
- **Flexible Sizing**: Configurable icon size (`extra-small`, `small`, `medium`, `large`) and typography sizing (`text-sm`, `normal`, `text-lg`, `text-xl`).

## Usage in Twig

```twig
{{ include('juc_sdc:icon-text', {
  icon: 'phone',
  text: '020 7250 3340',
  url: 'tel:02072503340',
  icon_color: 'primary',
  icon_size: 'small'
}) }}
```
