# Contributing to sca-templates

Thanks for your interest in improving the `sca-templates` ecosystem. These
are the organization-wide defaults; a repository that ships its own
`CONTRIBUTING.md` takes precedence for that repository.

## Ground rules

- **English only** for repository content, commits, and pull requests.
- **Conventional Commits**: `feat(scope): …`, `fix(scope): …`,
  `docs(scope): …`, `ci(scope): …`, `chore(scope): …`.
- **No secrets, tokens, or credentials** in the repository or in CI logs.
  Secrets live in the repository/organization secret store, or in Vault.
- **Changes land through reviewed pull requests.** `main` is protected;
  direct pushes are not allowed.

## Developer Certificate of Origin (DCO)

All commits **must** be signed off, certifying that you have the right to
submit the contribution under the project's license. This implements the
[Developer Certificate of Origin](https://developercertificate.org/).

Add `-s` when committing:

```bash
git commit -s -m "feat(scope): describe the change"
```

A commit missing its `Signed-off-by:` line cannot be merged.

## Pull requests

Every repository provides a pull request template. A mergeable PR:

- [ ] has a conventional-commit title (squash merge uses it as the commit message);
- [ ] is in English, with a clear description of the change and why;
- [ ] passes all required status checks (validation, security, tests);
- [ ] contains no secrets or generated artifacts;
- [ ] updates documentation in the same change when behavior or the public
      surface changes.

## CI/CD

Organization repositories share reusable workflows and composite actions from
[CI-CD-Templates](https://github.com/sca-templates/CI-CD-Templates). Prefer
those over per-repository copies, and pin reusable workflows and actions to a
released commit SHA with a `# vX.Y.Z` comment.

## Questions

Use [GitHub Discussions](https://github.com/orgs/sca-templates/discussions) for
questions. Report security issues privately — see [SECURITY.md](SECURITY.md).

## License

Unless a repository states otherwise, contributions are licensed under that
repository's `LICENSE` (MIT for most `sca-templates` repositories).
