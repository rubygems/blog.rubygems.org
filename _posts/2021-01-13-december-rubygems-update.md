---
title: December 2020 RubyGems Updates
layout: post
author: Gift Egwuenu
author_email: laurandidi21@gmail.com
---
Welcome to the RubyGems monthly update! As part of our efforts at [Ruby Together](http://rubytogether.org/), we publish a recap of the work that we’ve done the previous month. Read on to find out what updates were made to RubyGems and RubyGems.org in December.

## RubyGems News

In December, we finally released `bundler 2.2` and `Rubygems 3.2` 🎉. On the Bundler side, this minor release provides some major enhancements in how Bundler treats platforms, and also a few extra features. Check [this blog post about bundler-v2-2 release](https://bundler.io/blog/2020/12/09/bundler-v2-2.html) for details. On the RubyGems side, the release provides a lot of bug fixes, a noticeable boot time speed-up, better integration in ruby-core and alternative implementations, and adds support for a change in the server side that allows using scoped API keys.

After the releases, we also received the corresponding feedback and regression reports, and addressed almost everything reported through 4 patch level releases of each library. In particular, we made it on time for Ruby's Christmas release and managed to include `rubygems 3.2.3` and `bundler 2.2.3` with the final release of `ruby 3.0`.

This month, [RubyGems](https://github.com/rubygems/rubygems) gained [203 new commits](https://github.com/rubygems/rubygems.org/compare/master@%7B2020-12-01%7D...master@%7B2020-12-21%7D), contributed by 13 authors. There were 4191 additions and 2066 deletions across 1184 files.

## RubyGems.org News
This month, we published a guide on RubyGems.org about [API keys, their scopes, and CLI usage](https://guides.rubygems.org/api-key-scopes/) - [#275](https://github.com/rubygems/guides/pull/275). We also investigated and removed `ruby-bitcoin` and `pretty_color` gems for  containing malicious code which could steal sensitive information; this issue was reported by [@mensfeld](https://github.com/mensfeld) for obfuscated code. - [Gems yanked and Accounts Locked Wiki](https://github.com/rubygems/rubygems.org/wiki/Gems-yanked-and-accounts-locked#14-dec-2020)

In addition to that, we made the following improvements and fixes:

* deployed a PR to update `versions_downloads` in elastic search and reindex to fix the mismatch in downloads count. [#2534](https://github.com/rubygems/rubygems.org/pull/2534)
* deployed an API key with scopes and migrated legacy per account keys to the new API keys with encrypted storage. [#1962](https://github.com/rubygems/rubygems.org/pull/1962)
* setup insecure.rubygems.org to not redirect dependency endpoints to HTTPS. [#2590](https://github.com/rubygems/rubygems.org/pull/2590)
* worked on a PR to block throw-away domains from signup. [#2579](https://github.com/rubygems/rubygems.org/pull/2579)
* merged a PR to update a failing test on ruby 2.7. [#2580](https://github.com/rubygems/rubygems.org/pull/2580)
* worked on a PR to update to Rails 6.1. [#2584](https://github.com/rubygems/rubygems.org/pull/2584)
* worked on a PR to update gem dependencies to support elastic search 6. [#2585](https://github.com/rubygems/rubygems.org/pull/2585)
* updated a PR to update clearance. [#2446](https://github.com/rubygems/rubygems.org/pull/2446)
* enabled a few more Rails 6 defaults. [#2583](https://github.com/rubygems/rubygems.org/pull/2583)
* updated the rubygems.org TLS certificate to support TLS 1.3.

* deployed a PR and backfilled `canonical_versions` to disallow publishing of duplicate canonical version numbers. It resolves the issue of clients installing potentially malicious versions of existing releases. [#2559](https://github.com/rubygems/rubygems.org/pull/2559)
* updated `version_downloads` to use the most_recent version implementation. [#2534](https://github.com/rubygems/rubygems.org/pull/2534)
* fixed a script to block users with handles that had uppercase letters. [#2570](https://github.com/rubygems/rubygems.org/pull/2570)
* merged a PR to enable Rails 6 default for `return_false_on_aborted_enqueue`. [#2571](https://github.com/rubygems/rubygems.org/pull/2571)

As always, we continue to fix bugs, review and merge PR’s and reply to support tickets.

In total, [RubyGems.org](https://github.com/rubygems/rubygems.org) gained [77 new commits](https://github.com/rubygems/rubygems.org/compare/master@%7B2020-12-01%7D...master@%7B2020-12-31%7D), contributed by 10 authors. There were 2154 additions and 596 deletions across 96 files.

---

Learn more about contributing to RubyGems by visiting the [RubyGems Contributing Guide](https://github.com/rubygems/rubygems/blob/master/CONTRIBUTING.md#how-to-contribute). We welcome all kinds of contributions, including bug fixes, feature implementation, writing and updating documentation, and bug triage.
