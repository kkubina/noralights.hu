# noralights.hu — Agent instructions

## Project context

Start with the [project overview](docs/README.md) and [roadmap](docs/ROADMAP.md). Keep accepted scope, technical decisions, and working commands in the overview. Update the roadmap when a milestone or its completion criteria change.

Use the sibling repositories `../kristofkubina.com`, `../peterkubina.com`, and `../kvadrat-art.hu` as read-only references for layouts, structured content, styling, and build workflows. Choose conventions that fit the noralights.hu brief. Derive public copy, visual identity, routes, and hosting settings from this project's own sources.

## Implementation and content

- Prefer small reusable layouts, semantic HTML, plain CSS, and minimal client-side JavaScript. Keep content easy for the owner to edit.
- Use supplied facts and assets. Record missing copy or media in the roadmap. Track the source, license, and attribution for third-party assets and dependencies as they are added.
- Keep essential navigation usable with a keyboard and without JavaScript. Provide visible focus, readable contrast, meaningful image alternatives, and reduced-motion support.

## Verification and handoff

Once implementation exists, run the documented build and the checks relevant to the change. For visual work, inspect desktop and narrow mobile layouts against the project references. For route changes, verify links and direct navigation in the built site.

Report what changed, what was checked, and any remaining gaps. Keep credentials outside version control. Deployments and DNS changes require a release request from the owner.
