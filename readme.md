# Git Commit Messages

## Summary

The commit message should be structured as follows:

```bash
(emoji) <type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

The commit contains the following structural elements, to communicate intent to the consumers of your library:

* fix: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning).
* feat: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
* BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.
* types other than fix: and feat: are allowed, for example @commitlint/config-conventional (based on the the Angular convention) recommends build:, chore:, ci:, docs:, style:, * refactor:, perf:, test:, and others.
* footers other than BREAKING CHANGE: <description> may be provided and follow a convention similar to git trailer format.
  
Additional types are not mandated by the Conventional Commits specification, and have no implicit effect in Semantic Versioning (unless they include a BREAKING CHANGE). A scope may be provided to a commitโs type, to provide additional contextual information and is contained within parenthesis, e.g., feat(parser): add ability to parse arrays.

## Emoji List

Fork and modify to suit your needs. Don't forget to "star" and share the love.

| Text | Image | GFM shortcode* | Windows 10 picker name | When to use it |
|:--:|:-----:|:--------- |:-------------- |:-------------- |
| `๐` | :tada: | `:tada:` | `party popper` | initial commit |
| `โจ` | :sparkles: | `:sparkles:` | `sparkles` | when adding a new user-facing feature |
| `๐จ` | :art: | `:art:` | `artist palette` | when improving UI |
| `๐ฆ` | :package: | `:package:` | `package` | when refactoring or improving code |
| `๐` | :racehorse: | `:racehorse:` | `horse` | when improving performance |
| `๐` | :lock: | `:lock:` | `locked` | when improving security |
| `๐ง` | :wrench: | `:wrench:` | `wrench` | when updating configs |
| `โฟ` | :wheelchair: | `:wheelchair:` | `wheelchair symbol` |  when improving accessibility |
| `๐` | :rocket: | `:rocket:` | `rocket` | when improving dev tools |
| `๐` | :pencil: | `:pencil:` | `pencil` | when writing docs (e.g. README, code comments) |
| `๐` | :gem: | `:gem:` | `gem stone` | when cutting a new release / version bump |
| `๐` | :bug: | `:bug:` | `bug` | when fixing a bug |
| `๐ฅ` | :boom: | `:boom:` | `collision` | when fixing a crash |
| `๐ฑ` | :non-potable_water: | `:non-potable_water:` | `non-potable water` | when fixing a memory leak |
| `๐ฅ` | :fire: | `:fire:` | `fire` | when removing code or files |
| `โ` | :white_check_mark: | `:white_check_mark:` | `check mark button` | when adding new tests |
| `๐` | :green_heart: | `:green_heart:` | `green heart` | when fixing the CI build |
| `๐` | :shirt: | `:shirt:` | `t-shirt` | when fixing linter warnings |
| `๐ก` | :satellite: | `:satellite:` | `satellite antenna` | when adding instrumentation or metrics |
| `๐` | :loud_sound: | `:loud_sound:` | `speaker high volume` | when adding logging |
| `๐` | :mute: | `:mute:` | `muted speaker` | when removing logging |
| `โฌ` | :arrow_up: | `:arrow_up:` | `up arrow` | when upgrading dependencies |
| `โฌ` | :arrow_down: | `:arrow_down:` | `down arrow` | when downgrading dependencies |
| `๐` | :crossed_flags: | `:crossed_flags:` | `crossed flags` | when adding an A/B test or feature flag** |
| `โก` | :zap: | `:zap:` | `high voltage` | when making a backwards-incompatible change** |
| `๐ง` | :construction: | `:construction:` | `construction` | when the change is a work in progress (do not merge)** |

## Examples

### Commit message with description and breaking change footer

```bash
๐ง feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```

### Commit message with ! to draw attention to breaking change

```bash
โจ feat!: send an email to the customer when a product is shipped
```

### Commit message with scope and ! to draw attention to breaking change

```bash
โจ feat(api)!: send an email to the customer when a product is shipped
```

### Commit message with both ! and BREAKING CHANGE footer

```bash
๐ chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```