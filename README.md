# saucier-app.com

The marketing site for [Saucier](https://apps.apple.com/us/app/saucier/id1535998412),
a recipe app for iPhone and iPad.

Jekyll, published by **GitHub Pages** from `main` at the repository root. Pages
uses its own pinned toolchain (the "legacy" build type — Jekyll 3.9.x), so
anything added here has to work on that version and on the
[plugin allowlist](https://pages.github.com/versions/). `jekyll-sitemap` is the
only plugin in use.

## Running it locally

```sh
bundle install
bundle exec jekyll serve
```

On a recent Ruby this may fail: Jekyll 3.9's Liquid calls `String#tainted?`,
which Ruby removed in 3.2. The site builds identically on Jekyll 4, so for a
local preview use a separate Gemfile pinning `jekyll ~> 4.3` together with
`jekyll-sass-converter ~> 2.2` — the 2.x converter is libsass, which is what
GitHub Pages compiles the stylesheets with.

## Layout

```
_config.yml              Site metadata, nav, and the App Store link
index.html               Home page — its own sections, not a layout
_layouts/
├── default.html         Shell: head, header, main, footer
├── page.html            Long-form pages (FAQ, help, policies, changelog)
└── landing.html         Keyword landing pages — brand hero + prose + CTA
_includes/
├── head.html            All SEO metadata. Rendered at build time, never by JS
├── schema.html          JSON-LD: WebSite, MobileApplication, FAQPage, HowTo
├── header.html          Nav. The mobile menu is a checkbox, so no JavaScript
├── footer.html          Footer nav, driven by _config.yml
├── faq.html             Renders page.faq — the same list schema.html uses
├── cta.html             Shared closing call to action
├── icon.html            Inline SVG icons
└── appstore-badge.html
_pages/                  Everything that is not the home page
_sass/
├── _tokens.scss         Mirrors SaucierUI's colour, type and spacing tokens
├── _base.scss           Reset, document defaults, light/dark palette
├── _layout.scss         Container, header, sections, footer
├── _components.scss     Buttons, hero, device shots, cards, FAQ
└── _prose.scss          Long-form page styles
assets/
├── icon/                App icon at favicon and touch-icon sizes
└── img/screens/         App screenshots, from the app repo's fastlane output
```

## Things worth knowing before editing

**Nothing in `<head>` depends on JavaScript.** An earlier version of this site
shipped with an empty `<title>` and no meta description, filling them in on load
from the iTunes lookup API with jQuery. Crawlers saw a page with no title at
all. Keep metadata server-rendered.

**`page.faq` drives two things at once.** The visible accordion and the
`FAQPage` structured data are both generated from the same front-matter list, so
they cannot drift apart. Add questions there, not in the page body.

**Existing URLs are load-bearing.** `/privacypolicy/`, `/termsofservice/`,
`/FAQ/` and `/changelog/` are linked from App Store Connect and from inside the
app. Do not change those permalinks without updating both.

**No `aggregateRating` in the structured data.** It is the one schema property
that cannot be verified from the page, and Google will render stars from it.
It stays out until there is a real review count to point at.

**Design tokens come from the app.** `_sass/_tokens.scss` carries the literal
values from `Packages/SaucierUI/Sources/SaucierUI/Tokens`. If the app's brand
colour or corner radii change, change them in both places.

**Screenshots come from the app repo**, captured in
`scripts/appstore-screenshots/shots/iphone/`. Resize to 900px wide when copying
them into `assets/img/screens/`, and keep `_includes/device.html` and the
`.device__screen` aspect ratio in sync with the exported dimensions. `planned.jpg`
shows the meal plan; `library.jpg` is a library capture, not an onboarding screen.

## Adding a landing page

Create a file in `_pages/` with `layout: landing` and front matter:

```yaml
---
layout: landing
permalink: /your-page/
title: Short nav title
heading: The H1
eyebrow: Section label
seo_title: "Under 60 characters"
description: "110–160 characters."
lead: One sentence under the H1.
screenshot: /assets/img/screens/hero.png
screenshot_alt: "What the screenshot shows."
faq:
  - q: A question?
    a: An answer.
---
```

Then add it to `nav` or `footer_nav` in `_config.yml`.
