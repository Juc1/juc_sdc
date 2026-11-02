# Group (`juc_sdc:group`)

A flexible, responsive flexbox layout container component for Drupal Single Directory Components (SDC).

## Origins & Evolution
Originally forked from `byte_theme/components/group` and enhanced for cross-application layout needs.

## Features & Enhancements
1. **Responsive Flex Directions**:
   - `column`: Vertical stack (`flex-col`).
   - `row`: Horizontal row (`flex-row`).
   - `responsive-md`: Vertical on mobile devices, switching to horizontal on desktop screens (`flex-col md:flex-row`).
   - `responsive-lg`: Vertical on mobile/tablet devices, switching to horizontal on large screens (`flex-col lg:flex-row`).
2. **Alignment & Spacing**:
   - Customizable item alignment (`items_align`: `start`, `center`, `end`).
   - Customizable self alignment (`flex_align`: `start`, `center`, `end`).
   - Configurable gaps (`sm`, `md`, `lg`, `xl`).
3. **Container Styling**:
   - Padding options (`sm`, `md`, `lg`, `xl`).
   - Border radius options (`sm`, `md`, `lg`, `xl`).
   - Semantic background colors (`primary`, `secondary`, `accent`).
4. **Drupal Attribute Support**:
   - Seamlessly accepts and merges caller HTML attributes using Drupal's `create_attribute()`.

## Usage in Twig

```twig
{% embed 'juc_sdc:group' with {
  flex_direction: 'responsive-md',
  flex_gap: 'md',
  items_align: 'center'
} %}
  {% block group_slot %}
    <div>Item 1</div>
    <div>Item 2</div>
  {% endblock %}
{% endembed %}
```
