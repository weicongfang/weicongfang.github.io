# Academic Website Redesign

Date: 2026-07-14  
Project: `ghostie0831.github.io`  
Primary audience: prospective PhD advisors, academic peers, and potential collaborators

## 1. Objective

Redesign the existing Academic Pages/Jekyll site into a modern, restrained academic website that communicates Weicong Fang's scholarly identity within a few seconds. The site should foreground research fit, verified outputs, and Fall 2027 PhD availability while preserving an appropriately modest M.A.-student identity.

The latest CV at `/Users/fangweicong/Documents/个人/个人简历/phd/cv_phd_optimized.pdf` and its TeX source are the factual source of truth. Existing uncommitted updates in `_includes/head/custom.html`, `_pages/cv.md`, `_pages/publications.md`, `files/cv.pdf`, and `files/cv.tex` must be preserved and reconciled rather than overwritten.

## 2. Success Criteria

1. The first screen clearly shows:
   - Weicong Fang, `he/him`.
   - `M.A. Student in Communication` rather than `researcher`.
   - A visually highlighted `Seeking PhD opportunities for Fall 2027` status.
   - A concise account of past work and current interests.
2. Advisors can find research interests, publications, methods, current CV, and contact links without searching through unrelated material.
3. All public website HTML claims use the latest CV for authorship order, dates, venues, GPA, ranking, and roles. Where the CV's conference type and status conflict, the website uses the conservative status policy in Section 3.2.
4. The site has four primary routes: `/`, `/research/`, `/publications/`, and `/cv/`. The navigation labels are `About`, `Research`, `Publications`, and `CV`; `About` links to `/` and there is no separate `Home` item.
5. Placeholder and non-academic template content is no longer published.
6. The site builds with GitHub Pages-compatible Jekyll and works at desktop and mobile widths without JavaScript-dependent content.

## 3. Content Strategy

### 3.1 Homepage

The homepage is research-first but retains familiar academic conventions: portrait, institutional identity, email/Google Scholar/GitHub links, and concise navigation.

Order:

1. Compact site header with `Weicong Fang`, `he/him`, and four navigation links.
2. Profile column with the existing portrait, degree status, institution, location, and academic/contact links.
3. Highlighted Fall 2027 PhD availability badge.
4. Introductory bio.
5. Two actions: `View research` and `Download CV`.
6. Three research-interest cards:
   - Misinformation Correction
   - Human-AI Communication
   - Health Communication
7. Two selected journal publications.
8. Academic snapshot: M.A. program, GPA/rank, Tampere exchange.
9. One restrained personal sentence: `Outside academic work, I enjoy photography, tennis, and cycling.`

No question-style hero headline will appear.

### 3.2 Approved Bio Direction

Use the following copy, with journal titles styled typographically rather than surrounded by quotation marks:

> I am an M.A. student in Communication at Renmin University of China. My work lies at the intersection of misinformation correction, health communication, and human-AI communication. I have examined how human, AI, and hybrid sources, corrective strategies, and reasoning structures shape audience responses to health misinformation and fact-checking. Building on this work, my current interests focus on how people engage with generative AI for information and support during health-related uncertainty, and what these interactions mean for trust, judgment, help-seeking, and well-being.
>
> My work has been published in the *International Journal of Human-Computer Interaction* and *News and Writing*. I have presented earlier work at the Annual Conference of the Health Communication Committee of the Chinese Association for History of Journalism and Communication; related conference papers have been submitted to IAMCR and the International Conference on Chinese-Language Media and Huaxia Civilisations.

The venue sentence follows a common academic-introduction pattern: research focus first, then a short publication and conference signal. This was informed by the public introductions of Bingjie Liu and Lucy March, without copying their prose.

The generative-AI, health uncertainty, help-seeking, and well-being sentence is a user-confirmed prospective research direction. It describes interests rather than completed findings and therefore intentionally goes beyond the completed-work entries in the CV.

Factual guardrail: the latest CV labels the 2025 Singapore and IAMCR 2026 entries `[Out for review]`, despite also calling them `Conference presentation` and listing past conference dates. Until the user explicitly confirms acceptance and actual presentation and updates the CV source of truth, the website HTML must use the exact display label `Submitted paper — Out for review` for both items. It must not call either item `presented` or `conference presentation`. The confirmed 2024 item uses `Poster presentation`. These labels must be identical on the Publications page, web CV summary, and any structured metadata. The neutral bio wording `related conference papers have been submitted to...` is permitted and consistent with this policy.

The downloadable CV PDF is a user-authored source artifact and is explicitly exempt from the website display-label policy; this redesign copies it unchanged and does not rewrite its internal labels. The implementation handoff must flag the PDF's `Conference presentation`/`Out for review` inconsistency for the user, but the website must not reproduce the contradictory `Conference presentation` wording.

### 3.3 Methods Language

The homepage methods line may list:

- experiments
- surveys
- computational text analysis
- social network analysis
- sentiment analysis
- thematic analysis

`Social media data collection` must not be described as a research method. It may appear only inside the relevant project description as a data-acquisition responsibility.

### 3.4 Research Page

The Research page should explain substance rather than repeat the publication list.

Sections:

1. Research focus: the three interests above and the health-related generative-AI direction.
2. Selected research experience:
   - Social Media Data Collection Project, 2024 — Student Team Lead; Python-based collection, cleaning, SQL storage, and cross-platform data integration.
   - Contemporary Chinese Internet Nationalism from the Perspective of Mediatized Olympics, 2022 — first author and first prize; use the CV's verified 18,575-comment count and method description.
3. Relevant professional experience:
   - Xinhua News Agency, China Internet Rumor-Refuting Platform — retain a concise research-relevant description of fact-checking communication, correction framing, and dissemination metrics.
   - Kingsoft Cloud Technology — one concise line based on the CV.
   - Kuaishou Technology — one concise line based on the CV.

The page must not turn the two corporate internships into large project cards or reproduce detailed non-academic duties.

### 3.5 Publications Page

Use the latest CV and remove the extra coauthored 2025 Singapore conference paper currently present on the website but absent from that CV.

Sections:

1. Journal Articles — two items, including the IJHCI DOI and the online link for the Chinese-language article.
2. Conference Papers and Presentations — the three CV-listed items with exact dates, roles, locations, and status labels.

The page should use semantic publication entries with title, authors, venue, year, type/status, and action links. No emoji headings and no repeated decorative rules.

### 3.6 CV Page

Replace the stale downloadable PDF with the July 2026 PDF from the CV source folder. The page will provide:

1. A prominent `Download CV` action.
2. A concise, responsive web summary of Education, Publications, Conference Papers and Presentations, Research Experience, Professional Experience, Awards, and Methods/Skills.
3. Exact CV wording where precision matters, while avoiding redundant long internship bullets already available in the PDF.

The repository's existing `files/cv.tex` has local font paths and is not required to build the website. Do not rely on it during the Jekyll build.

## 4. Visual System

### 4.1 Direction

Use the approved hybrid of the research-first editorial layout and the conventional academic profile layout.

- Warm white page background.
- Ink/forest primary text and actions.
- Restrained terracotta accent for the PhD badge edge, research-card rules, and small highlights.
- Light neutral green/gray section surfaces.
- Fine borders and very subtle shadows.
- Generous whitespace, short line lengths, and strong typographic hierarchy.
- No dark full-page theme, gradients as decoration, emoji headings, zoom effects, or gallery styling.

### 4.2 Typography

Use the approved modern humanist sans direction:

```css
font-family: "Avenir Next", Avenir, -apple-system, BlinkMacSystemFont,
             "Segoe UI", sans-serif;
```

Use tighter letter spacing for display headings, normal spacing for body text, and uppercase tracking only for compact labels. Do not use Arial or the current global `Lucida Grande` override. Do not add a remote-font dependency.

### 4.3 Responsive Behavior

- Desktop: portrait/profile column beside the main bio; three research cards; two-column publications/snapshot block.
- Tablet: preserve the profile/bio relationship where space permits; reduce gaps and card padding.
- Mobile: stack portrait and profile above the bio; make research cards one column; stack selected publications and snapshot; keep actions large enough to tap; prevent publication metadata and long venue names from overflowing.

## 5. Technical Architecture

Retain the existing Jekyll/Academic Pages foundation and GitHub Pages compatibility. Do not introduce React, a new static-site generator, a package-heavy design system, or client-side content fetching.

Implementation units:

1. `_config.yml`: accurate site metadata, author identity, pronouns, SEO description, and only required collections/defaults.
2. `_data/navigation.yml`: About, Research, Publications, CV.
3. `_pages/about.md`: custom homepage markup using reusable semantic CSS classes.
4. `_pages/research.md`: new research route.
5. `_pages/publications.md`: verified publication entries.
6. `_pages/cv.md`: current CV link and web summary.
7. `_includes/author-profile.html`, `_includes/masthead.html`, and footer/head includes only where necessary for identity, navigation, metadata, and a professional footer.
8. `assets/css/main.scss` plus focused partial changes: design tokens, layout, cards, typography, responsive rules, and removal of obsolete custom overrides.
9. `files/cv.pdf`: latest downloadable CV.

Route and profile behavior:

- `_pages/about.md` owns `/`, keeps redirects from `/about/` and `/about.html`, and sets `author_profile: false` because it renders the approved custom portrait/profile column.
- `_pages/research.md`, `_pages/publications.md`, and `_pages/cv.md` set `author_profile: true` and use the compact shared author sidebar.
- The custom homepage must not render the shared sidebar include, preventing a duplicated profile or unintended three-column layout.
- The masthead uses the exact labels and URLs stated in the success criteria.

Data flow is static:

`latest CV -> curated Markdown/YAML content -> Jekyll build -> static HTML/CSS -> GitHub Pages`

No runtime API or database is involved. Content remains readable if JavaScript or external CDNs fail.

## 6. Cleanup Scope

Delete the following tracked placeholder content files after confirming none is referenced by the four retained pages:

- `_drafts/post-draft.md`
- `_posts/2012-08-14-blog-post-1.md`
- `_posts/2013-08-14-blog-post-2.md`
- `_posts/2014-08-14-blog-post-3.md`
- `_posts/2015-08-14-blog-post-4.md`
- `_posts/2199-01-01-future-post.md`
- `_talks/2012-03-01-talk-1.md`
- `_talks/2013-03-01-tutorial-1.md`
- `_talks/2014-02-01-talk-2.md`
- `_talks/2014-03-01-talk-3.md`
- `_teaching/2014-spring-teaching-1.md`
- `_teaching/2015-spring-teaching-2.md`
- `_portfolio/portfolio-1.md`
- `_portfolio/portfolio-2.html`
- `_publications/2009-10-01-paper-title-number-1.md`
- `_publications/2010-10-01-paper-title-number-2.md`
- `_publications/2015-10-01-paper-title-number-3.md`
- `_publications/2024-02-17-paper-title-number-4.md`
- `_pages/archive-layout-with-content.md`
- `_pages/category-archive.html`
- `_pages/collection-archive.html`
- `_pages/markdown.md`
- `_pages/non-menu-page.md`
- `_pages/page-archive.html`
- `_pages/portfolio.html`
- `_pages/tag-archive.html`
- `_pages/talkmap.html`
- `_pages/talks.html`
- `_pages/teaching.html`
- `_pages/terms.md`
- `_pages/year-archive.html`
- `files/paper1.pdf`, `files/paper2.pdf`, and `files/paper3.pdf`
- `files/slides1.pdf`, `files/slides2.pdf`, and `files/slides3.pdf`
- `_data/comments/` and all sample comment records under it

Delete these obvious demo images only after a repository reference search confirms they are unused: `images/500x300.png`, `images/3953273590_704e3899d5_m.jpg`, `images/editing-talk.png`, `images/foo-bar-identity.jpg`, `images/foo-bar-identity-th.jpg`, every `images/image-alignment-*` file, `images/paragraph-indent.png`, and `images/paragraph-no-indent.png`.

Do not delete reusable source tools in this redesign. Keep `markdown_generator/`, `talkmap.py`, `talkmap.ipynb`, and `talkmap/` in the repository, but add them to Jekyll's `exclude` list so they are not copied into `_site`. Likewise exclude `.superpowers/` and `tmp/`.

Retain infrastructure that still serves the site, including the 404 page, sitemap support, core Jekyll layouts/includes, icons used by academic/contact links, the current portrait, and build configuration.

Add both `.superpowers/` and `tmp/` to `.gitignore` during implementation so visual brainstorming and local render artifacts remain untracked. Verify that neither directory exists in generated `_site` output.

Preserve and reconcile the pre-existing working-tree changes explicitly:

- `_includes/head/custom.html`: retain the icon-font preload/initial-load fix unless the redesigned header no longer uses those fonts; if removed, verify every remaining icon before dropping it.
- `_pages/publications.md`: preserve the added 2026 IJHCI publication while restructuring the page.
- `_pages/cv.md`: preserve the added 2026 IJHCI publication while replacing stale or CV-inconsistent content.
- `files/cv.pdf`: intentionally replace with the designated July 2026 source PDF and verify equality by checksum.
- `files/cv.tex`: do not overwrite or delete; it is not a website build dependency.

Before deleting any include, font, icon, or image not in the exact manifest above, run a repository reference search. Anything still referenced by retained pages, layouts, CSS, metadata, or favicons must remain.

## 7. Accessibility, SEO, and Failure Handling

- Preserve semantic heading order and visible keyboard focus.
- Use `header`, `nav`, `main`, `aside`, and `footer` landmarks with one page-level `h1`.
- Provide meaningful alt text for the portrait.
- Meet WCAG AA contrast: at least 4.5:1 for normal text and 3:1 for large text and essential interface boundaries.
- Do not encode essential meaning through color alone.
- Use descriptive link text rather than bare URLs where practical.
- Set a specific site description and person metadata for search/social previews.
- Use no remote font dependency; system fallbacks prevent missing-font failures.
- Keep the CV download link valid even if icon fonts fail.
- Hide or remove routes whose content is deleted rather than leaving empty archive pages.
- Keep navigation usable when JavaScript is disabled: desktop and wrapped narrow-width links remain visible, or a CSS fallback exposes them if the enhanced greedy-navigation script is unavailable.
- If the mobile menu button is retained, give it an accessible name, maintain `aria-expanded`, expose focus visibly, and keep a logical keyboard/focus order.
- Apply the same rule to the shared author sidebar on Research, Publications, and CV: contact links must be visible in the `.no-js` fallback; any enhanced disclosure button must have an accessible name, `aria-expanded`, and `aria-controls` tied to the contact-link container.

## 8. Verification Plan

1. Run a clean development build and a production GitHub Pages-compatible build (including safe-mode constraints) and treat warnings about missing pages, includes, collection references, or unsupported plugins as failures to resolve.
2. Inspect Home, Research, Publications, CV, and 404 pages locally.
3. Test desktop, tablet, and mobile widths, including 320px reflow and long publication/conference titles. Test at 200% browser zoom without horizontal page overflow.
4. Verify:
   - latest CV downloads successfully and `files/cv.pdf` has the same checksum as the designated source PDF
   - DOI and article links resolve to the intended destinations
   - email, Google Scholar, and GitHub links are correct
   - all images, fonts, and icons load without console or network errors attributable to the site
   - no sample post, fake publication, talk, teaching, portfolio, or demo route remains in navigation or sitemap
   - no occurrence of `researcher` is used as Weicong Fang's title
   - `he/him` and the Fall 2027 status are visible
   - `social media data collection` is not listed as a method
   - navigation is keyboard-operable, focus order is logical, the mobile menu has an accessible name/state, and the four primary links remain usable with JavaScript disabled
   - on Research, Publications, and CV, the shared sidebar contact links remain directly visible and usable with JavaScript disabled; the enhanced disclosure is keyboard-operable and exposes correct name/state/control relationships
   - heading and landmark structure is valid and color contrast meets the thresholds above
   - `.superpowers/`, `tmp/`, `markdown_generator/`, and talk-map source tools are absent from `_site`
5. Verify SEO output in the production build: page-specific descriptions, canonical URLs, Open Graph/social metadata, and Person JSON-LD contain the correct name, institution, profile URL, and academic links.
6. Compare all public claims against `cv_phd_optimized.tex` immediately before completion.

## 9. Non-Goals

- No blog, teaching portfolio, personal photography gallery, or hobby page.
- No publication database, CMS, analytics dashboard, search feature, or contact form.
- No inflated claims such as `leading`, `top-tier`, or `expert`.
- No redesign of the CV source document itself.
- No push, deployment, or GitHub Pages publication unless separately requested.
