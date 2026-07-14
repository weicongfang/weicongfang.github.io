# Academic Profile Identity and Navigation Design

## Goal

Refine the shared academic identity shown across the site, update the About achievement paragraph, and prioritize Publications in the primary navigation without changing publication lists, CV content, or the downloadable PDF.

## Approved content

Replace the third paragraph of the About biography with exactly:

> My work has been published in the *International Journal of Human–Computer Interaction* and *News and Writing* (in Chinese). My research has been presented at the annual conferences of the International Association for Media and Communication Research (IAMCR) and the International Communication Association (ICA), as well as at the International Conference on Chinese-Language Media and Huaxia Civilisations and the Annual Conference of the Health Communication Committee of the Chinese Association for History of Journalism and Communication.

The paragraph retains the journal publications, marks *News and Writing* as Chinese-language work, and lists conference venues in this order: IAMCR, ICA, the International Conference on Chinese-Language Media and Huaxia Civilisations, and the Health Communication Committee annual conference.

## Shared identity design

- Add canonical display fields under `author` in `_config.yml` for the masthead name (`Weicong FANG`) and Chinese name (`方炜聪`).
- The masthead displays only `Weicong FANG`; remove the masthead pronouns.
- Keep `he/him` in every left-side profile area.
- Every page that renders a left-side profile area, including About, Publications, Research, CV, and Sitemap, displays the same profile hierarchy:
  1. `Weicong Fang` with `he/him`
  2. `方炜聪` on a separate line
  3. `M.A. Student in Communication`
- Make the About profile and shared child-page author profile read identity values from `site.author` rather than duplicating names or roles.
- Style the Chinese name with a modern system sans-serif stack: `"PingFang SC"`, `"Noto Sans CJK SC"`, `"Microsoft YaHei"`, sans-serif.
- Give the Chinese name exactly the same `font-size` and `font-weight` as the role line while preserving the existing color palette and responsive layout; only the Chinese font family and the spacing required for the separate line differ.

## Navigation

Set the primary navigation order to:

1. About
2. Publications
3. Research
4. CV

Keep the existing labels and URLs.

## Scope boundaries

- Do not change the Publications page content.
- Do not change the web CV content, `files/cv.tex`, or `files/cv.pdf`.
- Do not change research descriptions, contact links, portrait, colors, typography outside the new Chinese-name rule, or other layout behavior.
- Visual brainstorming files under `.superpowers/` remain local and are not committed.

## Verification

- Run a production Jekyll build.
- Confirm every page masthead contains `Weicong FANG` and no masthead pronouns.
- Confirm every generated page with a left-side profile area, including About, Publications, Research, CV, and Sitemap, renders the same three-line identity hierarchy and retains `he/him` in the profile area.
- Confirm the Chinese name uses the intended font stack and the same computed `font-size` and `font-weight` as the role line at desktop and mobile widths.
- Confirm the About achievement paragraph matches the approved wording.
- Confirm the navigation order is About, Publications, Research, CV on all four pages.
- Confirm Publications, web CV, and downloadable PDF content are unchanged.
