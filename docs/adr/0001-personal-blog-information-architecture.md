# ADR 0001: Personal Blog Information Architecture

Date: 2026-06-20

## Status

Accepted

## Context

This Hugo site started from the Hugo Theme Stack starter template. The first real article is a paper-reading note about a magnetically driven soft continuum microrobot. The site still contained template posts, template link-page copy, a sample Disqus shortname, and mixed category naming.

The near-term site should work as a personal academic blog rather than a theme demo.

## Decision

Use `content/post` as the only homepage content section for now.

Keep these top-level navigation items:

- Home
- Archives
- Search
- Links

Use these content categories as the initial publishing model:

- `Research`: research notes, paper reading, technical ideas
- `Paper Reading`: paper-reading series and journal-club notes
- `Diary`: personal logs
- `Travel`: travel notes
- `Cooking`: cooking records

Template posts remain in the repository as examples, but are marked `draft: true` so they do not publish to the site.

Comments are disabled until there is a real provider choice. The template Disqus shortname must not be used in production.

## Consequences

The homepage now highlights actual personal content instead of Stack theme examples.

Future content can be added without changing routing because post permalinks already use `/p/:slug/`.

The site can still use the template files as local authoring references by enabling drafts during local preview.

## Open Questions

- Should the primary writing language be Chinese, Japanese, English, or mixed by article type?
- Should the site brand remain `Jonathan Lee`, or use a Chinese/Japanese display name?
- Should `Research` and `Paper Reading` be separate categories long term, or should `Paper Reading` become a tag under `Research`?
- The current deployment path is `/JonathanLee/`, matching the repository and project directory name.
