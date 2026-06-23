# ADR 0003: Homepage Tab Navigation

Date: 2026-06-21

## Status

Accepted

## Context

The homepage needs two prominent cards: `近期更新` and `所有分类`. The initial implementation showed both recent updates and all categories on the homepage, which made the page longer and did not match the intended navigation model.

The intended behavior is:

- Opening the homepage shows the two cards and recent updates only.
- Clicking `所有分类` opens the categories page.
- The categories page still shows the same two cards at the top, so users can return to recent updates.
- The card for the current page appears visually active.
- The left sidebar does not need `近期更新` or `所有分类`.

## Decision

Create a reusable partial at `layouts/partials/home/portal-nav.html`.

Use it in:

- `layouts/home.html` with `Active = updates`
- `layouts/page/updates.html` with `Active = updates`
- `layouts/categories/terms.html` with `Active = categories`

Remove the categories list from the homepage body. The homepage body now shows recent updates only.

Style the active card with `.home-portal__card.is-active`.

## Consequences

The homepage and categories page share the same top navigation, so their UI remains consistent.

The homepage stays focused on recent updates, while categories have a dedicated page.

The left sidebar remains simpler and only needs global navigation such as Home, Search, and Links.
