# ADR 0002: Homepage and Navigation Structure

Date: 2026-06-20

## Status

Accepted

## Context

The site should feel like a personal website while staying useful as a long-term archive. The homepage should not be a generic reverse-chronological blog list. The owner wants two primary ways to enter the site:

- Recent updates
- All categories

The existing Archives page duplicated part of this job and was less clear as a top-level navigation item.

## Decision

The homepage is a portal with two large links:

- `近期更新`: a time-ordered list of posts
- `所有分类`: the taxonomy-based category overview

The left sidebar keeps direct navigation to:

- Home
- Recent updates
- All categories
- Search
- Links

The Archives page remains available at `/archives/`, but it is removed from the main sidebar.

## Consequences

Visitors can choose whether to browse by time or by topic from the homepage.

The sidebar is shorter and better aligned with the site's real usage.

The old archive URL remains available, so existing links are not broken.
