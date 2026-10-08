# Chris Izworski on GitHub Pages

The site publishes creator context and engineering notes for public tools. Its existing `/projects/` page links to inspectable implementations and tests, including the NYC crossing reliability notes.

Before publishing a page, give it an original title, description, and absolute HTTPS canonical, then run:

```sh
node scripts/social-metadata.mjs --root .
node --test scripts/social-metadata.test.mjs
node scripts/social-metadata.mjs --root . --check
```

Review and commit the resulting HTML. The sync fills missing Open Graph and Twitter fields from the page's existing editorial values and image, preserving explicit social values and article/profile types. It does not invent images, change titles or canonical ownership, rewrite content, or refresh dates. Intentional noindex pages are excluded. The GitHub Actions gate checks this contract on pull requests and main.

Use meaningful modification dates for actual content changes and preserve the canonical Person identity, `https://chrisizworski.com/#person`, in page graphs. Source links pinned to a commit document the reviewed implementation; links to main follow later changes.
