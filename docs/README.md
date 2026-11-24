# noralights.hu

Noralights is a five-piece band. The initial design studies for its placeholder homepage use photographs from the band's November 7, 2026 session at Pannonia Studio. The placeholder homepage announces the upcoming album with a five-photo montage and live HTML text.

## Studio photo studies

Each homepage study features one frame of each band member. The contact sheet also groups five candidate shots per member. Frame numbers refer to `DSCF####.JPG` in the owner's `2026 Noralights Pannonia Studio` folder.

| Study | Source frames in reading order |
| --- | --- |
| [Five in Time](../design/studio-session/01-five-in-time.jpg) · five vertical panels | 0506, 0539, 0587, 0571, 0637 |
| [Session Sleeve](../design/studio-session/02-session-sleeve.jpg) · central portrait with two stacked pairs | Left 0555 / 0541 · center 0638 · right 0595 / 0624 |
| [Through the Glass](../design/studio-session/03-through-the-glass.jpg) · wide piano frame with four smaller portraits | Lead 0603 · top right 0507 / 0543 · bottom right 0591 / 0651 |
| [Album Coming Soon](../design/studio-session/04-album-coming-soon.jpg) · approved desktop layout | Left DSCF0551.MOV at 3.1 seconds / 0541 · center 0638 · right [edited 0592](../design/studio-session/DSCF0592-greco-bound-headstock.png) / 0624 |
| [Performer selects](../design/studio-session/performer-selects.jpg) · five frames per row | Drummer, bassist, cap-wearing performer, pianist, vocalist |

## Technical direction

Astro generates static HTML and CSS. The five WebP crops in `public/images/` come from the owner’s studio material. The guitarist image incorporates the owner’s Greco reference. The desktop layout follows the approved montage. Portrait screens use a two-column composition with a wider tile for the guitarist. CSS handles the entrance and hover animations and respects reduced motion. The page uses system fonts.

## Local development

Use the Node version in `.nvmrc` and npm. From the repository root:

```sh
npm ci
npm run dev
```

Open the local address printed by Astro (normally `http://127.0.0.1:4350/`). Run `npm run check` for diagnostics and `npm run build` to generate `dist/`. Stop the development server before running `npm run preview` on the same port to serve the production build.

## Project documents

- [Roadmap](ROADMAP.md) — milestones, completion checks, and the inputs needed for the first release.
- [Agent instructions](../AGENTS.md) — repository conventions for implementation, content, and verification.

## Deploy on Cloudflare Pages

Connect the GitHub repository `kkubina/noralights.hu` using the [Pages Git integration](https://developers.cloudflare.com/pages/get-started/git-integration/). Select `main` as the production branch and Astro as the framework. Build from the repository root with `npm run build` and publish `dist`. Pages reads the Node version from `.nvmrc`.

Open the generated Pages URL and check the homepage on desktop and mobile. When ready to switch traffic, add `noralights.hu` in the Pages project's [Custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/) settings. The apex domain must be an active zone in the same Cloudflare account. Future pushes to `main` trigger production deployments.
