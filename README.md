# @anjunar/ui

CSS-first design foundation for Anjunar projects.

`@anjunar/ui` has no dependency on consuming libraries or applications. Consumers may depend on this package, but this package must never depend on, import, or name its consumers.

## Layers

- `theme.css` defines the Tailwind theme and runtime CSS variables.
- `base.css` defines global document defaults.
- `utilities.css` defines low-level reusable visual utilities.
- `components.css` defines generic `aj-*` primitives.
- `index.css` imports all Anjunar UI layers.

## Usage

```css
@import "tailwindcss";
@import "@anjunar/ui";
```

Set the active theme on the document root:

```html
<html data-theme="light">
```

or:

```html
<html data-theme="dark">
```

## Language

Use Tailwind for composition and `aj-*` classes for repeated Anjunar primitives:

```html
<section class="aj-card-glass aj-stack">
  <p class="aj-label">Context</p>
  <h1 class="aj-heading">A clear surface</h1>
  <p class="aj-copy">Project-specific layout can stay local while shared structure remains reusable.</p>
</section>
```

Core primitives:

- `aj-glass`, `aj-glass-soft`, `aj-glass-dense`, `aj-card-glass`
- `aj-card`, `aj-card-quiet`, `aj-panel`, `aj-panel-muted`
- `aj-toolbar`, `aj-floating`, `aj-menu`, `aj-menu-item`
- `aj-tabs`, `aj-tab`, `aj-tab-active`
- `aj-button`, `aj-button-primary`, `aj-button-quiet`, `aj-button-ghost`
- `aj-input`, `aj-chip`, `aj-badge`, `aj-empty`, `aj-table-shell`

Page primitives:

- `aj-page`, `aj-page-layout`, `aj-page-shell`
- `aj-page-hero`, `aj-page-panel`, `aj-page-panel-shell`
- `aj-kicker`, `aj-page-title`, `aj-page-copy`
- `aj-action-pill`, `aj-action-pill-primary`, `aj-action-pill-ghost`
- `aj-icon-badge`, `aj-quick-row`, `aj-quick-icon`, `aj-quick-copy`

Shared recipe tokens:

- `--aj-floating-*` for menus, popovers, dropdowns, and small detached controls.
- `--aj-overlay-*` for larger elevated surfaces, notifications, dialogs, and transient panels.
- `--aj-chrome-*` for bars, headers, footers, and application frame seams.
- `--aj-control-*` for compact interactive controls and active/hover states.

## Boundary

This package is the visual root. It may expose generic names like `aj-panel`, `aj-button`, and `aj-shell`. It must not expose consumer-specific names.
