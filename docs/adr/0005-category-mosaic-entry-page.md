# ADR 0005: Category Mosaic Entry Page

Date: 2026-06-21

## Status

Accepted

## Context

The all-categories page should be a visual entry page for the site's content categories. It should not be a deep hierarchy. The intended design is a slightly irregular set of rectangular cards. Each card should show an optional image on top and the category name below.

The site owner will prepare category images manually.

## Decision

Replace the default Stack tile list on `layouts/categories/terms.html` with a custom `category-mosaic` grid.

Each category card:

- Links to the category page
- Uses the category bundle image from front matter when available
- Falls back to a solid color from `style.background`
- Shows the category title
- Shows the article count

Use a lightly irregular height pattern through modifier classes:

- `category-mosaic__card--0`
- `category-mosaic__card--1`
- `category-mosaic__card--2`
- `category-mosaic__card--3`
- `category-mosaic__card--4`

On mobile, all category cards become a single-column list.

## Consequences

The categories page becomes a stronger visual entry point while remaining simple to maintain.

Future category images can be added by placing images in each category bundle and setting `image: filename`.
