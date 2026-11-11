## [1.0.8](https://github.com/marslo/ifonts-github/compare/v1.0.7...v1.0.8) (2026-11-11)

### Bug Fixes

* **github**: hide recent-pushes banner on PR list ([7ef31f1](https://github.com/marslo/ifonts-github/commit/7ef31f14ef3f3c7e847a508121bb2458b746a37e))
  - match `[data-testid*="recently-touched-branches"]` so the react wrapper on the PR list is hidden
  - force `display: none !important` to beat primer's `.d-flex` utility

### Others

* **pr**, **overview**: adjust font-size for pr overview page (preview feature) ([6bfd8d3](https://github.com/marslo/ifonts-github/commit/6bfd8d39e3604602e0612014943e2fa56d03f0a9))

## [1.0.7](https://github.com/marslo/ifonts-github/compare/v1.0.6...v1.0.7) (2026-11-10)

### Bug Fixes

* **font-size**: size review thread diff previews ([ebe222a](https://github.com/marslo/ifonts-github/commit/ebe222a3ba303d115e55b6a43b6279650535c6f2))
  - apply `--font-size-small-mono` to `StaticDiffPreview` tables in review threads
  - exclude `[class*="Overlay-"]` from the h2 heading size rule
  - add `--h1-size` to `--h5-size` variables alongside the existing font-size tokens
* **github**, **readme**: size AI suggestion diffs again ([4da0c58](https://github.com/marslo/ifonts-github/commit/4da0c588cc999fa684f18c9047de4386fdd20153))
  - match the suggested changeset via `data-testid="automated-review-suggestion"`
  - cover the camelCase `unifiedDiffLines` table code cells, line numbers and hunk header
  - align the readme options table columns

## [1.0.6](https://github.com/marslo/ifonts-github/compare/v1.0.5...v1.0.6) (2026-10-21)

### Bug Fixes

* **filter**: use mono font for the issues/PRs filter input to align the caret with the styled text ([12a5110](https://github.com/marslo/ifonts-github/commit/12a511038580ab653e191f237d61ca4a81739d87))
* **github**: hide the recent-pushes banner again by matching the hashed `RecentlyTouchedBranches` css-module class; and update readme ([655e540](https://github.com/marslo/ifonts-github/commit/655e54096337006a70c6bcae5fa70b99d8462622))
  - match `RecentlyTouchedBranches-module` and `Flash` as separate substrings
  - cover the new `…-module_<hash>_Flash` class and the old `…-module__Flash` one
  - convert `README.org` headings, lists, links and quote to markdown

### Documentation

* update README ([7a2f430](https://github.com/marslo/ifonts-github/commit/7a2f430830b78d463f5122afe5d694d53e758c82))

## [1.0.5](https://github.com/marslo/ifonts-github/compare/v1.0.4...v1.0.5) (2026-10-21)

### Bug Fixes

* **mono**, **pr**, **release**: enlarge mono font sizes, exclude PR semibold titles and truncated file names from header font rules, and clean up release-note and typos tooling ([88d60db](https://github.com/marslo/ifonts-github/commit/88d60db6c6df993cda97b91095e3a55f805fda55))

## [1.0.4](https://github.com/marslo/ifonts-github/compare/v1.0.3...v1.0.4) (2026-09-30)

### Bug Fixes

* **Blex**: fix the `Blex` local fonts in global variable; and using `--font-family-github-mono` instead of `--font-family-mono` for code blocks ([2de039c](https://github.com/marslo/ifonts-github/commit/2de039cac8ddc023c7b57f7400a2475dab94b144))

## [1.0.3](https://github.com/marslo/ifonts-github/compare/v1.0.2...v1.0.3) (2026-09-15)

### Others

* **BlexMonoLig**: customize the `BlexMonoLigNFM-*` to: Book(350) ⇾ normal; Text(450) ⇾ bold; ([105b1cb](https://github.com/marslo/ifonts-github/commit/105b1cb02ba861b0512433606e48ba28bbcbce8f))

## [1.0.2](https://github.com/marslo/ifonts-github/compare/v1.0.1...v1.0.2) (2026-09-15)

### Bug Fixes

* **pr**, **h2**: exclude `PR file change inline review header` (`InlineReviewThread-*`) from <h2> font settings ([e083263](https://github.com/marslo/ifonts-github/commit/e08326352870b647e040c8d46e6ac0b94e154673))

## [1.0.1](https://github.com/marslo/ifonts-github/compare/v1.0.0...v1.0.1) (2026-09-11)

### Bug Fixes

* **scope**: stop the style loading site-wide and repair malformed :not() lists ([94d7343](https://github.com/marslo/ifonts-github/commit/94d73430a5d7dec067a7dd33f8021b16516bef13))
  - move top-level @font-face and :root into the @-moz-document block so the style no longer injects a global section on every site
  - drop three unused google-fonts @import links
  - add/remove commas in :not() selector lists that Stylus flagged as "Unexpected )" parse errors


### Others

* **BlexMonoLig**, **githubusercontent**: using `"BlexMonoLig Nerd Font Mono"` as default mono font; enable `githubusercontent\\.(com|io)` domain ([3e24d4d](https://github.com/marslo/ifonts-github/commit/3e24d4d54cbc997356cffda981a568be5825100c))

## 1.0.0 (2026-09-11)

### Features

* **init**, **ifonts-github**: split github-dedicated userstyle out of ifonts with lint/release tooling ([a0f1f1a](https://github.com/marslo/ifonts-github/commit/a0f1f1abcee13fd66f4c1ae3954f4b9a858fa3a1))

    Split from marslo/ifonts@f52f9c8fed6a22b62fbae1eb9f76bf9489ba90e0 (tag v4.1.9).

    Split-from: https://github.com/marslo/ifonts/blob/f52f9c8fed6a22b62fbae1eb9f76bf9489ba90e0/ifonts.user.css
    Split-from-tag: https://github.com/marslo/ifonts/releases/tag/v4.1.9
