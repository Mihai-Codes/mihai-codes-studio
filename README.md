# mihai-codes-studio

Sanity Studio for [mihai.codes](https://mihai.codes) portfolio site.

[![Sanity](https://img.shields.io/badge/Sanity-F03E2F?style=flat-square&logo=sanity&logoColor=white)](https://sanity.io)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://typescriptlang.org)

## Live Studio

**URL**: [mihai-codes.sanity.studio](https://mihai-codes.sanity.studio/)

## Content Schema

### Blog Post (`post`)

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Post title (required) |
| `slug` | slug | URL slug, auto-generated from title |
| `description` | text | Short excerpt for previews |
| `date` | date | Publication date |
| `tags` | string[] | Category tags |
| `readingTime` | string | Estimated reading time |
| `draft` | boolean | Draft status (hidden from site) |
| `content` | text | Full post content in Markdown |

## Development

```bash
# Install dependencies
pnpm install

# Start dev server
pnpm dev

# Deploy to Sanity
pnpm deploy
```

## Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Sanity Studio  │────▶│   Sanity API    │◀────│   mihai.codes   │
│  (This repo)    │     │   (Content DB)  │     │  (Qwik + CF)    │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

## Related Repositories

- **Main Site**: [mihai.codes](https://github.com/chindris-mihai-alexandru/mihai.codes)

## Project Info

- **Sanity Project ID**: `76ahey7l`
- **Dataset**: `production`
- **Deployed via**: Sanity CLI (`sanity deploy`)

## License

MIT
