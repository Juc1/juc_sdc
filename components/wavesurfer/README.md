# WaveSurfer Audio Player (`juc_sdc:wavesurfer`)

An interactive SoundCloud-style audio waveform player component for Drupal Single Directory Components (SDC) powered by [WaveSurfer.js](https://wavesurfer.xyz/).

## Features

- **Progressive Streaming**: Plays immediately in 1–2 seconds via native HTML5 `<audio>` while generating the visual waveform concurrently.
- **Waveform Canvas Visualization**: Renders interactive, seekable audio waveform bars matching your theme's semantic colors (`primary` / `secondary`).
- **Interactive Controls**:
  - Circular play/pause toggle button with Phosphor icons.
  - Rewind 15 seconds & Fast Forward 15 seconds jump buttons.
  - Live tabular elapsed time and total duration readouts.
  - Scrub hover indicator showing timestamp preview under cursor.
  - Optional inline direct file download button.
- **Responsive**: Adapts gracefully across mobile, tablet, and desktop viewports.
- **Self-Contained Library**: Bundles its own CSS and minified WaveSurfer.js behavior via `juc_sdc/wavesurfer`.

## Props

| Prop | Type | Required | Default | Description |
| :--- | :--- | :---: | :---: | :--- |
| `src` | `string` | **Yes** | &mdash; | URL or relative path to the MP3 audio file |
| `downloadable` | `boolean` | No | `true` | Show or hide the inline download button |

## Usage in Twig

```twig
{# Basic usage #}
{{ include('juc_sdc:wavesurfer', {
  src: 'https://example.com/audio/episode-1.mp3'
}) }}

{# Without download button #}
{{ include('juc_sdc:wavesurfer', {
  src: node.field_mp3_link.0.url,
  downloadable: false
}) }}
```

## Usage in Canvas

Add the **WaveSurfer Audio Player** component into any page or Content Template and bind the `src` prop to:
`[entity:node:podcast_episode -> field_mp3_link]`
