# @anjunar/ui

CSS-first design foundation for Anjunar projects.

`@anjunar/ui` has no dependency on consuming libraries or applications. Consumers may depend on this package, but this package must never depend on, import, or name its consumers.

## Layers

- `theme.css` defines the Tailwind theme and runtime CSS variables.
- `base.css` defines global document defaults.
- `components.css` defines generic `aj-*` primitives.
- `index.css` imports Tailwind and all Anjunar UI layers.

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

## Boundary

This package is the visual root. It may expose generic names like `aj-panel`, `aj-button`, and `aj-shell`. It must not expose consumer-specific names.
