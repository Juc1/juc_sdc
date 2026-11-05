# Grid (`juc_sdc:grid`)

A lightweight, responsive CSS Grid layout container for creating equal-width columns and equal-height card rows without page-section overhead.

---

## Why Use `juc_sdc:grid`?

* **Equal-Height Rows by Default**: Sets `items-stretch` out of the box so child cards automatically match the height of the tallest card in the row.
* **Equal-Width Columns**: Uses native CSS Grid tracks (`1fr 1fr 1fr`) ensuring cards don't shrink or stretch unevenly based on content.
* **Lightweight & Nestable**: Pure `<div>` container with zero background or margin overhead. Can be dropped anywhere: inside a `section`, inside an accordion, inside tabs, or in a modal.
* **Turnkey Canvas UI UX**: An editor simply selects `columns: 3` and drops cards into the `content` slot.

---

## Props

| Prop | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `columns` | `enum` (`"1"`–`"6"`) | `"3"` | Desktop columns (>= 1024px). |
| `columns_tablet` | `enum` (`auto`, `"1"`–`"3"`) | `auto` | Tablet columns (768px - 1023px). Auto defaults to 2 cols for multi-column desktop. |
| `columns_mobile` | `enum` (`"1"`, `"2"`) | `"1"` | Mobile columns (< 768px). |
| `gap` | `enum` (`none`, `sm`, `md`, `lg`, `xl`) | `md` | Space between items (`none`: 0, `sm`: 16px, `md`: 24px, `lg`: 32px, `xl`: 48px). |
| `items_align` | `enum` (`stretch`, `start`, `center`, `end`) | `stretch` | Vertical alignment. `stretch` ensures cards match the tallest card's height. |
| `grid_classes` | `string` | `""` | Additional CSS utility classes. |

---

## Slots

| Slot | Description |
| :--- | :--- |
| `content` | Main slot for dropping cards, teaser cards, feature blocks, or any components. |

---

## Twig Usage Example

```twig
{% embed 'juc_sdc:grid' with {
  columns: '3',
  gap: 'md',
} %}
  {% block content %}
    {{ include('daisyui_sdc:daisy-card-teaser', {
      heading_text: 'Card 1',
      text: '<p>Short description.</p>',
    }) }}
    {{ include('daisyui_sdc:daisy-card-teaser', {
      heading_text: 'Card 2',
      text: '<p>Longer description that makes this card the tallest in the row...</p>',
    }) }}
    {{ include('daisyui_sdc:daisy-card-teaser', {
      heading_text: 'Card 3',
      text: '<p>Another card matching the tallest card height.</p>',
    }) }}
  {% endblock %}
{% endembed %}
```
