# Profile Links Unification Design

## Goal

Present the same academic contact information on About, Research, Publications, and CV, with one canonical data source and no GitHub link.

## Canonical information

Display the following five items in this order:

1. Beijing, China
2. Renmin University of China
3. Email
4. Google Scholar
5. ORCID

The first two items are text. Email, Google Scholar, and ORCID are links. ORCID uses the Academicons `ai-orcid` icon already bundled with the site.

## Implementation design

- Keep the profile values under `author` in `_config.yml` and add the ORCID URL there.
- Remove the GitHub author field and GitHub social metadata.
- Make the About profile and the shared child-page author profile read these values from `site.author`.
- Preserve the existing page-specific layout and CSS classes while ensuring both render the five items in the same order.
- Remove the separate institution line from the About identity block so the institution appears once, in the unified profile list.
- Do not change navigation, typography, biography, research content, or other links elsewhere in the site.

## Accessibility and metadata

- Retain visible text labels beside every icon.
- Mark decorative icons as hidden from assistive technology.
- Keep the email link as `mailto:` and use the supplied Google Scholar and ORCID URLs.
- Add the ORCID URL to the site's person-level social metadata.

## Verification

- Build the site with the production Jekyll configuration.
- Confirm About, Research, Publications, and CV each show the same five items in the specified order.
- Confirm GitHub is absent from all four profile areas.
- Confirm the ORCID icon renders and the Email, Google Scholar, and ORCID links resolve to the intended destinations.
- Check desktop and mobile layouts for wrapping or alignment regressions.
