# BL tracker app: waitlist

Interest form page for a BL tracker Android app (in development), hosted on Cloudflare Pages:
https://bltracker.pages.dev/

The form is an embedded Tally form. Add `?source=reddit` (or any value) to the address to record where a visitor came from.

## Deploying

Pushing to GitHub does not update the Cloudflare page. From this folder:

```sh
d=$(mktemp -d) && cp index.html "$d" && npx wrangler@3 pages deploy "$d" --project-name bltracker --branch main
```

Pushing to `main` does still update the GitHub Pages copy at https://yahani.github.io/bl-tracker-waitlist/.
