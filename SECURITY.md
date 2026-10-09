# Security Policy

This policy applies to all repositories in the
[sca-templates](https://github.com/sca-templates) organization unless a
repository ships its own `SECURITY.md`.

## Reporting a vulnerability

Do **not** open a public issue for anything security related. Report it
privately:

1. Open the **Security** tab of the repository where the issue lives and choose
   **Report a vulnerability** (GitHub private advisory).
2. Describe the impact and, when known, the affected file(s) and a minimal
   reproduction.
3. Keep the advisory private until a fix has been released.

The maintainers triage across the ecosystem, so a report filed against one
repository may be moved to wherever the flaw actually lives.

## What we do

- Reproduce and assess severity, then fix through a normal pull request that
  must pass the repository's required checks before merging.
- If a leaked credential is involved, the secret is treated as **compromised**:
  it is rotated at the source, not merely removed from git.

## Supported versions

Most repositories are maintained as a single track on the tip of `main`.
Release tags are snapshots for consumers; they are not support branches unless
the repository says otherwise.

## Automated posture

Organization repositories run shared security workflows — secret scanning
(gitleaks), dependency scanning (osv-scanner), and optional infrastructure-as-code
posture (checkov) — from
[CI-CD-Templates](https://github.com/sca-templates/CI-CD-Templates). Never commit
secrets: CI blocks the push.
