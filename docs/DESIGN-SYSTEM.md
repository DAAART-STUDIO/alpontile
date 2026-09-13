# Design System

## Purpose

This document describes the visual system inherited from the donor landing-page architecture and its intended adaptation for Ristorante al Pontile.

The design should communicate a premium Italian lakeside restaurant experience while remaining consistent with the existing implementation.

## Design principles

### Editorial hospitality

The interface should feel closer to an editorial hospitality experience than to a generic restaurant template.

Key characteristics:

- strong visual hierarchy;
- large photographic areas;
- restrained typography;
- generous spacing;
- deliberate section transitions;
- cinematic presentation of the restaurant and lake setting.

### Real location first

Visual storytelling must represent the actual Ristorante al Pontile environment.

Do not transfer donor-specific:

- buildings;
- mountains;
- churches;
- roads;
- terraces;
- interiors;
- landscapes;
- landmarks.

Only verified or supplied imagery should be used as factual representation.

### Existing visual language

The donor's:

- layout system;
- component structure;
- responsive behavior;
- animation patterns;
- navigation behavior;
- spacing logic;
- typography hierarchy;
- design tokens

should be preserved during normal content adaptation.

## Components

The current architecture contains reusable styles for areas including:

- hero;
- navigation;
- buttons;
- cuisine;
- dishes;
- events;
- experience;
- footer;
- menu;
- moments;
- place;
- reservation modal;
- scroll progress;
- section scroll cues;
- view/gallery;
- visit/contact sections.

Component classes should not be renamed or removed without a functional reason.

## Color and tokens

The authoritative implementation is:

```text
css/tokens.css
```

Do not duplicate token values in individual components when an existing design token is available.

## Typography

Typography should follow the existing donor hierarchy. Content changes must not require arbitrary changes to font sizing, spacing or responsive rules.

## Imagery

Image selection is content work, not a substitute for CSS changes.

Images should be:

- current;
- relevant to the restaurant;
- physically accurate;
- appropriately cropped for the existing component;
- optimized for web delivery.

## Motion

Existing animation and transition behavior should be preserved.

Motion should support:

- orientation;
- hierarchy;
- atmosphere;
- section transitions.

It should not be removed or redesigned merely during content replacement.

## Responsive behavior

The existing responsive system is part of the donor architecture. Adapt content to available structures rather than rewriting responsive CSS.

## Accessibility

Preserve:

- semantic HTML;
- `aria-*` attributes;
- keyboard interaction;
- focus behavior;
- meaningful alternative text;
- existing interactive states.
