Git Commit Message
===============

All Git Commit Messages **MUST** meet this Text Format:
```
:emoji1: :emoji2: Subject
(Only One NewLine)
Message Body
(Only One NewLine)
Ref <###>
```

Rules
----
1. Message Subject **SHOULD** Begin with _at-least_ One Emoji(see below for [list of Suggested Emojis](#Suggested-Emojis)).
2. Message Summary **SHOULD** End with _at-least_ One [GitHub Issue](https://github.com/features#issues)/[Phabricator Task](http://phacility.com/phabricator/maniphest/) ID Reference, Ex. `Issue #27`, `Ref T27` or `Ref T27, T56` or `Fixes T8`.
3. Total Characters of the _Subject Line_ **MUST** be _Less_ than or _Equal_ to **72** Chars Long.
4. Use Valid [MarkDown](https://daringfireball.net/projects/markdown/basics) format in _Message Body_.
5. Use the **Present Tense** ("Add feature" not "Added feature").
6. Use the **Imperative Mood** ("Move cursor to..." not "Moves cursor to...").
7. All WIP(Work In Progress) Commits **MUST** have the WIP Emoji(see below).

Notes
----
+ (IMPORTANT) All **WIP** Commits **Should** be Avoided!.
+ (NOTE) Tasks with Commits in `Fixes T###` Format will be Automatically [_Closed as Resolved_](https://help.github.com/articles/closing-issues-via-commit-messages/)!.
+ (WARNING) There is a **Space** Character between Multiple Emojis!.
+ (WARNING) There is **NO** New-Line After the _Task ID Reference_ Line.
+ (NOTE) Every Raw Emoji Text(`:emoji:`) is Counted as One Char!.

---

Suggested Emojis
-------------

| Emoji | Raw Emoji Code | Description |
|:---:|---|---|
| :art: | `:art:` | when improving the **format**/structure of the code |
| :racehorse: | `:racehorse:` | when improving **performance** |
| :books: | `:books:` | when writing **docs** |
| :bug: | `:bug:` | when reporting a **bug** |
| :ambulance: | `:ambulance:` | when fixing a **bug** |
| :penguin: | `:penguin:` | when fixing something on **Linux** |
| :apple: | `:apple:` | when fixing something on **Mac OS** |
| :checkered_flag: | `:checkered_flag:` | when fixing something on **Windows** |
| :fire: | `:fire:` | when **removing code** or files |
| :white_check_mark: | `:white_check_mark:` | when adding **tests** |
| :green_heart: | `:green_heart:` | when fixing the **CI** build |
| :lock: | `:lock:` | when dealing with **security** |
| :arrow_up: | `:arrow_up:` | when upgrading **dependencies** |
| :arrow_down: | `:arrow_down:` | when downgrading **dependencies** |
| :shirt: | `:shirt:` | when removing **linter**/strict/deprecation warnings |
| :lipstick: | `:lipstick:` | when improving **UI**/Cosmetic |
| :construction: | `:construction:` | **WIP**(Work In Progress) Commits |
| :gem: | `:gem:` | New **Release** |
| :bookmark: | `:bookmark:` | Version **Tags** |
| :tada: | `:tada:` | **Initial** Commit |
| :speaker: | `:speaker:` | when Adding **Logging** |
| :mute: | `:mute:` | when Reducing **Logging** |
| :sparkles: | `:sparkles:` | when introducing **New** Features |
| :zap: | `:zap:` | when introducing **Backward-InCompatible** Features |
| :bulb: | `:bulb:` | New **Idea** |
| :snowflake: | `:snowflake:` | changing **Configuration**, Usually together with :penguin: or :ribbon: or :rocket: |
| :ribbon: | `:ribbon:` | Customer requested application **Customization** |
| :rocket: | `:rocket:` | Anything related to Deployments/**DevOps** |

Ask to Be [Creative](http://www.emoji-cheat-sheet.com/)!

There is Also a [nifty CLI tool](https://github.com/jakeasmith/commit) to aid in standardizing commit messages based on this document, thanks to [@jakeasmith](https://github.com/jakeasmith).
