# Contributing to VitalsDA

Every VitalsDA repository follows this workflow. A repository's own CONTRIBUTING.md or CLAUDE.md adds
its build and test commands.

## Workflow

1. Open an issue from a template (blank issues are disabled). For multi-step work, use a parent issue
   with ordered sub-issues. Every open issue sits on a milestone: the release it ships in, or `vNext`.
2. Branch from the default branch as `<type>/<issue#>-<slug>` (for example `feat/12-add-listener`).
   Never commit directly to the default branch.
3. Commit using Conventional Commits (`type(scope): description`), one change per commit. No
   attribution trailers, and no emoji in source, commit messages, issues or pull requests. README
   files and the release-drafter category headings are the only places emoji appear.
4. Open a PR with a Conventional Commit title. Fill in the PR template and reference the issue:
   `Closes #N` when the PR fully resolves it, `Refs #N` when it only does part. Add a closing summary
   before merge.
5. PRs squash-merge once CI is green and a maintainer approves.

Keep one concern per PR, even small ones.

## Releases

Nothing releases automatically. Each repository drafts its release notes with release-drafter, and a
maintainer publishes the draft by hand.

## Local setup

Install the governance hooks once per clone, where the repository provides them:

```
bash .claude/hooks/install.sh
```

They check Conventional Commits and the hygiene rules before you commit and push; CI checks the same.

## Conduct

Everyone taking part follows the [Code of Conduct](CODE_OF_CONDUCT.md).
