# job-tapout

Job Sinke's Founder Associate application page for Tap Out, hosted on Cloudflare Workers.

## Workflow for every change

1. Edit `src.html` (copy, layout, styles, scripts). Screenshots live in `public/shots/`, fonts in `fonts/`, the portrait in `img/`.
2. Rebuild the hosted page: `python3 build.py` (writes `public/index.html`).
3. Commit and push to `main`. Cloudflare Workers Builds deploys the Worker `job-tapout` automatically:
   https://job-tapout.sinke-job.workers.dev
4. After pushing, confirm the new build shows as Ready in Cloudflare (Workers & Pages → job-tapout → Deployments) and that the live page shows the change.

## Rules

- Never edit `public/index.html` by hand; it is generated.
- Keep personal and partner data blurred in screenshots; never add unblurred originals.
- Only `public/` is served (see `wrangler.jsonc`). Keep source, fonts and build files outside it.
