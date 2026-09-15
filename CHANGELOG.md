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
