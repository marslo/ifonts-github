## [1.1.0](https://github.com/marslo/ifonts-github/compare/v1.0.10...v1.1.0) (2026-11-18)

### Features

* **docs**: widen docs.github.com article layout ([57c06c7](https://github.com/marslo/ifonts-github/commit/57c06c7b5e4f3f4057d66774a438621beb90283d))
  - add a `docs.github.com` block to the stylesheet
  - raise the `ArticleGridLayout_containerBox*` cap to `90cqw` and center it
  - uncap the article grid column across the 1012 / 1074 / 1400px breakpoints

### Bug Fixes

* **checks**: exclude checks list titles from h4 size ([4c0631c](https://github.com/marslo/ifonts-github/commit/4c0631c3f50d24b8b21540e8c9119be2f8da551d))
  - skip `h4[class*="titleHeader__"]` in the global `h4` font-size rule
  - keep github's native size for PR checks list row titles
* **pr**, **list**: use normal sans size for list row titles ([5036e0b](https://github.com/marslo/ifonts-github/commit/5036e0b89a411414a24325f70dc47bb146f6dca5))
  - override the `h3` size on PR / issue list rows via `listitem-title-link`
  - apply `--font-size-normal-sans` to the title and its children

## [1.0.10](https://github.com/marslo/ifonts-github/compare/v1.0.9...v1.0.10) (2026-11-17)

### Bug Fixes

* **commit**: keep mono for branch and sha ([d434b12](https://github.com/marslo/ifonts-github/commit/d434b124dea951dc987500dbffbc1a636d3e8c11))
  - exclude `.commit-ref` from the `.css-truncate a` sans rule so branch / ref pills keep the mono font
  - apply the mono font to `code a[href*="/commit/"]` short sha links
* **commit**: make inline `code` in the repo latest-commit message row inherit the surrounding link / span size instead of github's fixed `12px` ([ab948c4](https://github.com/marslo/ifonts-github/commit/ab948c4bd01f328a264d0f53495f0a1ab8ed33be))
* **layout**: baseline-align PR review and timeline headers ([78aaa53](https://github.com/marslo/ifonts-github/commit/78aaa53b1a0f1f83245de4314b099d9766784aae))
  - baseline-align the file name and `Line N` in the review thread header
  - baseline-align the author name and `Bot` label in timeline comment headers

### Code Refactoring

* **user**: apply handwritten font to user names ([002511b](https://github.com/marslo/ifonts-github/commit/002511b773f008627f4ad21b4d5aa69474d6de9b))
  - extend the handwritten font rule to the repo owner in the `rgh-repo-header-info` breadcrumb, `AuthorName__` links, `[data-hovercard-type="user"]` links and the adjacent full-name `span.css-truncate`
  - switch the shared font size from a fixed `24px` to `110%` so it scales with the surrounding text

### Others

* **pr**: apply the mono font to the PR number in the sticky PR header by matching `number__` without its hash suffix ([9462a1e](https://github.com/marslo/ifonts-github/commit/9462a1e2d26549e8d09c0d810a4e3b03205bfb69))

## [1.0.9](https://github.com/marslo/ifonts-github/compare/v1.0.8...v1.0.9) (2026-11-12)

### Bug Fixes

* **github**, **pr**: fix PR/issue comment body font-size by matching `safe-html-box` without its hash suffix, and drive comment/breadcrumb/markdown-section sizes from `--h5-size` ( now `17px`, with `--font-size-h5` at `18px` ) ([5c0898c](https://github.com/marslo/ifonts-github/commit/5c0898c923dfba2a8d90f986f4a4ee4c2af86020))
  - match the hashed `safe-html-box` css-module class by its stable name part and add `.comment-body`, with `.markdown-body` raising specificity over primer's `.f5`
  - drive comment body, breadcrumb and `.markdown-section` sizes from `--h5-size` instead of fixed `16px`/`17px`
  - bump `--h5-size` to `17px` and `--font-size-h5` to `18px`

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
