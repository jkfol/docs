---
title: "Repository Management"
---

# Repository Management

While the following guidelines are not an absolute requirement, writing your code by these standards will ensure greater compatibility with the Ark Ecosystem and increases the likelihood your pull request will be accepted.

## Structure

Repositories across an organisation should have a consistent basic structure to make it easy to find everything across different repositories.

**At a bare minimum a repository should contain the following:**

1. **README.md** - Should contain at least a description, installation instructions and a contact address for security issues.
2. **LICENSE** - Should contain the software license of the project, commonly the MIT License for open-source projects.
3. **.editorconfig** - Should contain a configuration that is enforced by everyones editor if an appropriate plugin is installed.
4. **.gitignore** - Should contain a list of files and directories that should not be commited with `git push`.
5. **.travis.yml** - Should contain a configuration for TravisCI to run tests.

## Development

When a new repository is created for a project, the first thing you should do is create a `develop` branch and set it as default. This will indicate to developers that this project is not stable yet. This branch should be used until the initial implementation is done, and merged to `master` without squashing. `master` should then be set as the default branch.

Once the initial implementation is done and merged, only squash merging should be enabled and all future PRs should be squashed with meaningful commit messages.

## Squashing Pull-Requests

**When working on any project all pull-requests must be squashed.**

The goal of doing so first and foremost is to keep PRs small and focused on a single issue. If you think to yourself `all my hard work and organized commits are going to be lost` then your PR is most likely out of scope and trying to solve more then one issue at a time which means you should split it up into multiple PRs that are meaningful even after being squashed.

Another benefit of squashing is to have a clean & flat git history which allows to easily blame changes without having to go through 100 commits to finally reach what you were looking for.

**We only care about the net effect of the pull-requests, i.e. "feat: wallet integration". We don't care about the 30 commits of "bugfix, added, removed, refactored". We want a clear and concise history without any noise.**

## How to organize GitHub Issues & Pull Requests

**Status**
- ![#000000](https://placehold.it/15/000000/000000?text=+) `Status: Abandoned`
  - The issue or pull request has been abandoned.
- ![#000000](https://placehold.it/15/000000/000000?text=+) `Status: Won't Fix`
  - The issue is legitimate, but it is not something the team is currently able or willing to work on.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Status: Resolved`
  - The issue has been resolved.
- ![#043a96](https://placehold.it/15/043a96/000000?text=+) `Status: Accepted`
  - The proposed solution has been accepted.
- ![#d2dae1](https://placehold.it/15/d2dae1/000000?text=+) `Status: Available`
  - The issue is not assigned to anyone and available to be worked on.
- ![#d2dae1](https://placehold.it/15/d2dae1/000000?text=+) `Status: In Progress`
  - The issue or pull request is being worked on.
- ![#d2dae1](https://placehold.it/15/d2dae1/000000?text=+) `Status: On Hold`
  - The issue or pull request is not being worked on for the time being.
- ![#b60205](https://placehold.it/15/b60205/000000?text=+) `Status: Blocked`
  - The pull request is blocked from being merged for the time being.
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Status: Cannot Reproduce`
  - The issue cannot be reproduced by an engineer of the team.
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Status: Reverted`
  - The pull request was reverted after an initial merge.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Status: Needs Information`
  - The issue needs more information before it can be verified and resolved.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Status: Needs Investigation`
  - The issue needs more investigation before it can be verified and resolved.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Status: Needs Review`
  - The issue or pull request needs a review by an engineer of the team.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Status: Needs Testcase`
  - The issue or pull request relates to a feature that needs test coverage.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Status: Needs Changes`
  - The pull request needs additional changes before it can be merged.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Status: Needs Discussion`
  - The issue or pull request needs more discussion before it can be closed or merged.

**Bounty**
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Bounty: Tier 0`
  - The pull request has been assigned a T0 reward. Needs specialized, in-depth review.
- ![#ff9900](https://placehold.it/15/ff9900/000000?text=+) `Bounty: Tier 1`
  - The pull request has been assigned a T1 reward.
- ![#ff9900](https://placehold.it/15/ff9900/000000?text=+) `Bounty: Tier 2`
  - The pull request has been assigned a T2 reward.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Bounty: Tier 3`
  - The pull request has been assigned a T3 reward.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Bounty: Tier 4`
  - The pull request has been assigned a T4 reward.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Bounty: Tier 5`
  - The pull request has been assigned a T5 reward.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Bounty: Tier 6`
  - The pull request has been assigned a T6 reward.

**Severity**
- ![#b60205](https://placehold.it/15/b60205/000000?text=+) `Severity: Critical`
  - The issue is blocking an upcoming release.
- ![#ff9900](https://placehold.it/15/ff9900/000000?text=+) `Severity: High`
  - The issue causes data loss, crashes or hangs processes, makes the system unresponsive, etc.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Severity: Medium`
  - The issue reports bad or incorrect functionality, a confusing user experience, etc.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Severity: Low`
  - The issue reports cosmetic items, formatting, spelling, colors, etc.

**Platform**
- ![#dddddd](https://placehold.it/15/dddddd/000000?text=+) `Platform: Windows`
  - The issue reports incorrect functionality on Windows.
- ![#dddddd](https://placehold.it/15/dddddd/000000?text=+) `Platform: Linux`
  - The issue reports incorrect functionality on Linux.
- ![#dddddd](https://placehold.it/15/dddddd/000000?text=+) `Platform: macOS`
  - The issue reports incorrect functionality on macOS.

**Type**
- ![#1144ff](https://placehold.it/15/1144ff/000000?text=+) `Type: Feature`
  - The issue is a request for new functionality including changes, enhancements, refactors, etc.
- ![#1144ff](https://placehold.it/15/1144ff/000000?text=+) `Type: Release`
  - The issue or pull request is related to an upcoming release.
- ![#44bbff](https://placehold.it/15/44bbff/000000?text=+) `Type: Maintenance`
  - The pull request updates dependencies or configuration files.
- ![#44bbff](https://placehold.it/15/44bbff/000000?text=+) `Type: Performance`
  - The issue or pull requests relates to performance issues.
- ![#44bbff](https://placehold.it/15/44bbff/000000?text=+) `Type: Refactor`
  - The pull requests improves an existing implementation.
- ![#c7def8](https://placehold.it/15/c7def8/000000?text=+) `Type: Duplicate`
  - The issue is a duplicate of another feature request or bug report.
- ![#c7def8](https://placehold.it/15/c7def8/000000?text=+) `Type: Expected Behavior`
  - The issue is a bug report but the behaviour is intended.
- ![#b60205](https://placehold.it/15/b60205/000000?text=+) `Type: Breaking Change`
  - The issue or pull request documents or introduces a breaking change.
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Type: Bug`
  - The issue documents broken, incorrect, or confusing behavior.
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Type: Bugfix`
  - The pull request fixes an incorrect functionality or behaviour.
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Type: Bug`
  - The issue documents broken, incorrect, or confusing behavior.
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Type: Regression`
  - The issue is a bug that breaks functionality known to work in previous releases.
- ![#b60205](https://placehold.it/15/b60205/000000?text=+) `Type: Security`
  - The issue documents broken functionality that could expose private data or cause harm otherwise.
- ![#fef2c0](https://placehold.it/15/fef2c0/000000?text=+) `Type: Discussion`
  - The issue is a discussion about a generic topic.
- ![#fef2c0](https://placehold.it/15/fef2c0/000000?text=+) `Type: Documentation`
  - The issue or pull request relates to documentation.
- ![#fef2c0](https://placehold.it/15/fef2c0/000000?text=+) `Type: Information`
  - The issue is a blob of information for users by an engineer of the team.
- ![#fef2c0](https://placehold.it/15/fef2c0/000000?text=+) `Type: Question`
  - The issue is more of a question than a request for new features or a report of broken features.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Type: Good First Contribution`
  - The issue appears to have a simple solution.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Type: Standards`
  - The issue reports problems with the compliance of contribution guidelines or code standards.

**Difficulty**
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Difficulty: Challenging`
  - The issue requires extensive understanding of the code base.
- ![#ff9900](https://placehold.it/15/ff9900/000000?text=+) `Difficulty: Advanced`
  - The issue requires advanced understanding of the code base.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Difficulty: Intermediate`
  - The issue requires minimal understanding of the code base.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Difficulty: Beginner`
  - The issue doesn't require any specific knowledge about the code base.

**Priority**
- ![#b60205](https://placehold.it/15/b60205/000000?text=+) `Priority: Critical`
  - The issue will be seen by all users.
- ![#ff9900](https://placehold.it/15/ff9900/000000?text=+) `Priority: High`
  - The issue will be seen by most users.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Priority: Medium`
  - The issue will be seen by about half of users.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Priority: Low`
  - The issue will not be seen by most users.

**Test**
- ![#7936a5](https://placehold.it/15/7936a5/000000?text=+) `Test: General`
  - The issue or pull request is related to tests.
- ![#7936a5](https://placehold.it/15/7936a5/000000?text=+) `Test: Functional`
  - The issue or pull request is related to functional tests.
- ![#7936a5](https://placehold.it/15/7936a5/000000?text=+) `Test: Integration`
  - The issue or pull request is related to integration tests.
- ![#7936a5](https://placehold.it/15/7936a5/000000?text=+) `Test: Unit`
  - The issue or pull request is related to unit tests.

**Complexity**
- ![#e11d21](https://placehold.it/15/e11d21/000000?text=+) `Complexity: Undetermined`
  - Needs specialized, in-depth review.
- ![#ff9900](https://placehold.it/15/ff9900/000000?text=+) `Complexity: High`
  - More than 256 lines changed.
- ![#ffdd44](https://placehold.it/15/ffdd44/000000?text=+) `Complexity: Medium`
  - Less than 256 lines changed.
- ![#007700](https://placehold.it/15/007700/000000?text=+) `Complexity: Low`
  - Less than 64 lines changed.

**Environment**
- ![#f9d0c4](https://placehold.it/15/f9d0c4/000000?text=+) `Environment: Development`
  - The issue reports incorrect functionality in the development environment.
- ![#f9d0c4](https://placehold.it/15/f9d0c4/000000?text=+) `Environment: Production`
  - The issue reports incorrect functionality in the production environment.
- ![#f9d0c4](https://placehold.it/15/f9d0c4/000000?text=+) `Environment: Test`
  - The issue reports incorrect functionality in the test environment.
- ![#f9d0c4](https://placehold.it/15/f9d0c4/000000?text=+) `Environment: Continuous Integration`
  - The issue reports incorrect functionality in the CI environment.

## Assigning Bounty Tiers after merging a Pull Request

After a developer merges a PR it is *required* to assign one of the 7 bounty labels. Those labels will be used by the ArkEcosystem Bot to calculate bounty rewards and inform the contributors about those.

**Tier 1 - $100**

Tier 1 pull requests cover large code changes that usually bring new functionality and have a higher impact on the codebase.

Examples of this include a new API endpoint, resolving structural issues that cause circular dependencies, or adding a new bigger features to our codebase (an example would be settings page to the explorer, adding new identicons package to the desktop wallet or a new small non-essential plugin in the Core).

**Tier 2 - $50**

This tier covers medium features and improvements to the codebase that bring in new functionality, have a big impact on the performance of the product or biggest optimizations and refactors of the code.

An example would be optimizing some parts of the Core for improved performance of a specific function, implementing a medium, non-critical new feature in the desktop wallet or writing large documentation files that require understanding of the ARK code.

**Tier 3 - $25**

These pull requests cover smaller refactors or optimizations of the code or small non-essential features.

An example of this would be reducing complexity or improving performance of existing code, improving the readability of the code or writing new documentation files, full translations of the projects aka desktop wallet or mobile wallet.

**Tier 4 - $10**

Normal small tier pull requests that fix small bugs or add a new test.

Examples of this include adding more test coverage for existing functionality or resolving small bugs that usually get reported by users.

**Tier 5 - $5**

Small documentation updates or improvements that don’t have much code or smaller refactors of the code.

**Tier 6 - $1**

The lowest tier is for items that don’t usually have much to do with the code, but rather, are considered cosmetics.

An example would be a typo, language corrections, grammar corrections, dependency update, link updates or broken links.

**Tier 0 - Custom**

If you want to work on much bigger changes or custom projects that you don’t think fit any of the above tiers contact us at bounty@ark.io.

Some examples of what a custom tier 0 could cover — developing new modules for core that bring in new functionalities (PoW module instead of DPoS), different voting systems, proxy voting, implementing AIPs …

Some issues will also have labels with custom (usually higher) values that you can take on. Labels on those issues will have a defined monetary value, so if you see these available you can request to take point on resolving them. Upon completion and review you will receive payment in ARK.
