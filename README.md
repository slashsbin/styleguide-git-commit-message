<p align="center">
  <img src="https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png" alt="Git" height="128">
  <span>&amp;</span>
  <img src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f984.png" alt="Unicorn" height="128">
</p>

<p align="center">
  <a href="https://en.wikipedia.org/wiki/Emoji#Unicode_blocks"><img src="https://img.shields.io/badge/emoji-%F0%9F%A6%84%20%F0%9F%92%9F-lightgrey.svg" alt="Powered by Emojis!"></a>
  <a href="https://github.com/slashsbin/styleguide-git-commit-message/graphs/contributors"><img src="https://img.shields.io/github/contributors/slashsbin/styleguide-git-commit-message.svg" alt="GitHub contributors"></a>
  <a href="https://github.com/slashsbin/styleguide-git-commit-message/stargazers"><img src="https://img.shields.io/github/stars/slashsbin/styleguide-git-commit-message.svg" alt="GitHub stars"></a>
  <a href="https://github.com/slashsbin/styleguide-git-commit-message/blob/master/LICENSE"><img src="https://img.shields.io/github/license/slashsbin/styleguide-git-commit-message.svg" alt="license"></a>
</p>

# Git Commit Message StyleGuide

##### TOC
- [About](#about)
- [Commit Message Format](#commit-message-format)
- [Suggested Emojis](#suggested-emojis)
- [Tools](#tools)
- [References](#references)
- [Fun Emoji Usages](#fun-emoji-usages)
- [Contributing](#contributing)
- [License](#license)


## About
This is an attempt to standardize the format of commit messages, for the sake of **uniformity** in git log, **best practices** for writing commit messages & **fun**!

Using emojis at the beginning of commit messages, other than being fun, provides a simple way to indicate the intention of that commit, an ease for the eyes when browsing/reviewing git log. It's also a simple measure of the fact that how much that commit is focused on a single purpose, which is a good practice.

If these rules and/or using emojis is an [overkill](/../../issues/21) for your productivity or simply losing its purposes, please tailor them to your needs or don't use them.

### Summary of the reasons for these conventions:
- Fun!
- Simple navigation through git history (e.g. ignoring style changes).
- Automatic generating of the changelog.


## Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Message Subject(first line)
- Capitalize the `<subject>`.
- Do not end the first line with a period.
- Total characters of the first line **MUST** be _Less_ than or _Equal_ to **50** characters Long.
- Use the **present tense** ("Add feature" not "Added feature").
- Use the **imperative mood** ("Move cursor to..." not "Moves cursor to...").
- Use `<type>` to identify what type of changes introduced in this commit; Allowed `<type>` keywords:
  - An Emoji(see below for [list of Suggested Emojis](#suggested-emojis))
  - Or a Text:
    - feat: new feature for the user(or :sparkles: emoji)
    - fix: bug fix for the user(or :ambulance: emoji)
    - docs: changes to the documentation(or :books: emoji)
    - style: formatting, missing semi colons, etc; no production code change(or :art: emoji)
    - refactor: refactoring production code, eg. renaming a variable(or :tractor: emoji)
    - test: adding missing tests, refactoring tests; no production code change(or :microscope: emoji)
    - chore: updating grunt tasks etc; no production code change
- If you need more than one keyword or emoji to use, you should probably think twice!. This usally means you need to break this commit into more smaller commits; If thats not the case then separate each emoji with a space.
- Use `<scope>` to identify which component this `<type>` is related to; Example `<scope>` values:
  - init
  - runner
  - watcher
  - config
  - web-server
  - proxy
  - etc.
- The `<scope>` can also be empty (e.g. if the change is a global or difficult to assign to a single component), in which case the parentheses are omitted.

### Message Body
- Includes **motivation** for the change and contrasts with previous behavior.
- Use the body to explain **whats** and **whys** vs. *hows*.
- Wrap each line of the body at **72** characters.

### Message Footer
- Reference issues this commit is related to with the status of that Issue; Ex. `Issue #27`, `Ref T27` or `Ref T27, T56` or `Fixes T8`.
- Supported issue tracker status keywords:
  - Fixes
  - Fixed
  - Closes
  - Closed
  - Resolves
  - Resolved
  - Ref
  - Issue
  - Issues
- More info on issue tracker status keywords:
  - [GitHub Issues](https://help.github.com/articles/closing-issues-using-keywords/)
  - [GitLab Issues](https://docs.gitlab.com/ee/user/project/issues/automatic_issue_closing.html)
  - [Phabricator Tasks](https://secure.phabricator.com/book/phabricator/article/diffusion_autoclose/)
- It's also [recommended](/../../issues/19) to use _Full URL to the Issues_, instead of just issue ID Number; Doing so will ease browsing issues from terminal.
- In the case of multiple issues separate them with commas, Ex. `Closes #27, #56`.

### Notes
- Use valid [MarkDown](https://daringfireball.net/projects/markdown/basics) format in the `<body>`.
- All **WIP**(Work In Progress) commits **SHOULD** have the :construction: Emoji.
- All **WIP** commits **SHOULD** be avoided!.
- Referencing Issues by using special keywords like `Fixes` or `Resolves` will mark them as closed automatically! For more  information about automatic issue closing using ketwords see their documentation(linked above).
- There is **NO** new-line after the `<footer>`.
- Every emoji text(`:emoji:`) is counted as one character!.
- See [ToDo Grammar StyleGuide](https://github.com/slashsbin/styleguide-todo-grammar) for more Information on `@XXX` Comment Tags.


## Suggested Emojis

| Emoji | Raw Emoji Code | Description |
|:---:|:---:|---|
| :art: | `:art:` | when improving the **format**/structure of the code |
| :newspaper: | `:newspaper:` | when creating a **new file** |
| :pencil: | `:pencil:` | when **performing minor changes/fixing** the code or language |
| :racehorse: | `:racehorse:` | when improving **performance** |
| :books: | `:books:` | when writing **docs** |
| :bug: | `:bug:` | when reporting a **bug**, with [`@FIXME`](https://github.com/slashsbin/styleguide-todo-grammar#bug-report)Comment Tag |
| :ambulance: | `:ambulance:` | when fixing a **bug** |
| :penguin: | `:penguin:` | when fixing something on **Linux** |
| :apple: | `:apple:` | when fixing something on **Mac OS** |
| :checkered_flag: | `:checkered_flag:` | when fixing something on **Windows** |
| :fire: | `:fire:` | when **removing code** or files, _maybe_ with `@CHANGED` Comment Tag |
| :tractor: | `:tractor:` | when **change file structure**. Usually together with :art: |
| :hammer: | `:hammer:` | when **refactoring** code |
| :umbrella: | `:umbrella:` | when adding **tests** |
| :microscope: | `:microscope:` | when adding **code coverage** |
| :green_heart: | `:green_heart:` | when fixing the **CI** build |
| :lock: | `:lock:` | when dealing with **security** |
| :arrow_up: | `:arrow_up:` | when upgrading **dependencies** |
| :arrow_down: | `:arrow_down:` | when downgrading **dependencies** |
| :fast_forward: | `:fast_forward:` | when **forward-porting features** from an older version/branch |
| :rewind: | `:rewind:` | when **backporting features** from a newer version/branch |
| :shirt: | `:shirt:` | when removing **linter**/strict/deprecation warnings |
| :lipstick: | `:lipstick:` | when improving **UI**/Cosmetic |
| :wheelchair: | `:wheelchair:` | when improving **accessibility** |
| :globe_with_meridians: | `:globe_with_meridians:` | when dealing with **globalization**/internationalization/i18n/g11n |
| :construction: | `:construction:` | **WIP**(Work In Progress) Commits, _maybe_ with `@REVIEW` Comment Tag |
| :gem: | `:gem:` | New **Release** |
| :egg: | `:egg:` | New **Release** with Python egg|
| :ferris_wheel: | `:ferris_wheel:` | New **Release** with Python wheel package |
| :bookmark: | `:bookmark:` | Version **Tags** |
| :tada: | `:tada:` | **Initial** Commit |
| :speaker: | `:speaker:` | when Adding **Logging** |
| :mute: | `:mute:` | when Reducing **Logging** |
| :sparkles: | `:sparkles:` | when introducing **New** Features |
| :zap: | `:zap:` | when introducing **Backward-InCompatible** Features, _maybe_ with `@CHANGED` Comment Tag |
| :bulb: | `:bulb:` | New **Idea**, with `@IDEA` Comment Tag |
| :snowflake: | `:snowflake:` | changing **Configuration**, Usually together with :penguin: or :ribbon: or :rocket: |
| :ribbon: | `:ribbon:` | Customer requested application **Customization**, with `@HACK` Comment Tag |
| :rocket: | `:rocket:` | Anything related to Deployments/**DevOps** |
| :elephant: | `:elephant:` | **PostgreSQL** Database specific (Migrations, Scripts, Extensions, ...)  |
| :dolphin: | `:dolphin:` | **MySQL** Database specific (Migrations, Scripts, Extensions, ...) |
| :leaves: | `:leaves:` | **MongoDB** Database specific (Migrations, Scripts, Extensions, ...) |
| :bank: | `:bank:` | **Generic Database** specific (Migrations, Scripts, Extensions, ...) |
| :whale: | `:whale:` | **Docker** Configuration |
| :handshake: | `:handshake:` | when **Merge files** |
| :cherries: | `:cherries:` | when Commit Arise from one or more [**Cherry-Pick**](https://git-scm.com/docs/git-cherry-pick) Commit(s) |


## Tools

- [Commit](https://github.com/jakeasmith/commit)(CLI): This is a nifty CLI tool to aid in standardizing commit messages based on this document, thanks to @jakeasmith.
- [gitMoji](https://gitlab.com/louisgrasset/git-moji)(Firefox & Chrome Extension): Enhance your commits with emojis!, thanks to [@louisgrasset](https://twitter.com/louisgrasset).


## Fun Emoji Usages
- [CodeEmoji](https://codemoji.org/): Mozilla’s Codemoji enciphers your messages with emoji for fun and profit
- [Emoji Based Diagram](https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service/#send_data): Emoji Based Diagram of Data Bearing Subscription Updates(WebPush VAPID)


## Contributing

[Ask](https://github.com/slashsbin/styleguide-git-commit-message/issues/new) to Be [Creative](https://www.emojicopy.com/)!

To add a new Emoji to the list: [Create an Issue](https://github.com/slashsbin/styleguide-git-commit-message/issues/new) & Send a [PR]().


## License

The Code is licensed under the [MIT License](http://slashsbin.mit-license.org/).
