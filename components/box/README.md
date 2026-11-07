# Box (`juc_sdc:box`)

A dedicated single-item layout and styling wrapper component for Drupal Single Directory Components (SDC).

## Purpose
While `juc_sdc:group` orchestrates **multiple** items (with flex direction, flex gap, and multi-child distribution), `juc_sdc:box` is designed specifically to wrap a **single** component or content item to provide:
1. **Positioning & Alignment**: Center an SDC (e.g., centering a button, badge, or card) or align it left/right.
2. **Inner Padding**: Add padding (`xs` / 8px, `sm` / 16px, `md` / 32px, `lg` / 64px, `xl` / 128px) around an element.
3. **Max Width & Boundaries**: Constrain an element with responsive max-width presets (`sm`, `md`, `lg`, `xl`, `2xl`, `prose`, etc.) and optional centering (`mx-auto`).
4. **Visual Styling**: Add daisyUI semantic background colors (`base-100`, `primary`, etc.), corner rounding (`radius`), drop shadows, and subtle borders.

## Properties

| Prop | Type | Default | Options | Description |
| :--- | :--- | :--- | :--- | :--- |
| `align` | `string` | `stretch` | `stretch`, `start`, `center`, `end` | Horizontal alignment of the wrapped child |
| `box_align` | `string` | `default` | `default`, `start`, `center`, `end` | Positioning of the box container within its parent |
| `padding` | `string` | `none` | `none`, `xs`, `sm`, `md`, `lg`, `xl` | Inner padding around the item |
| `max_width` | `string` | `none` | `none`, `xs`, `sm`, `md`, `lg`, `xl`, `2xl`, `3xl`, `prose`, `full` | Maximum width constrain |
| `radius` | `string` | `none` | `none`, `sm`, `md`, `lg`, `xl`, `full` | Corner radius |
| `background` | `string` | `default` | `default`, `base-100`, `base-200`, `base-300`, `primary`, `secondary`, `accent`, `neutral`, `info`, `success`, `warning`, `error` | DaisyUI semantic background |
| `shadow` | `string` | `none` | `none`, `sm`, `md`, `lg`, `xl` | Drop shadow elevation |
| `border` | `string` | `none` | `none`, `default`, `primary`, `neutral` | Border styling |

## Slots

- `content` (or `box_slot`): The single component or content item being wrapped.

## Usage in Twig

### Centering a Button
```twig
{% embed 'juc_sdc:box' with {
  align: 'center',
  padding: 'sm'
} %}
  {% block content %}
    <a href="/contact" class="btn btn-primary">Contact Us</a>
  {% endblock %}
{% endembed %}
```

### Wrapping a Card with a Background, Padding, and Max-Width
```twig
{% embed 'juc_sdc:box' with {
  max_width: 'md',
  box_align: 'center',
  padding: 'md',
  radius: 'lg',
  background: 'base-200'
} %}
  {% block content %}
    {{ include('daisyui_sdc:card', { ... }) }}
  {% endblock %}
{% endembed %}
```
