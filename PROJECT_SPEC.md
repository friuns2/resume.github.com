# PROJECT_SPEC

## Project Purpose
`resume.github.com` provides a lightweight web app that generates a public resume-style view from a GitHub username and repository activity.

## Current Maintenance Posture
- Upstream (`resume/resume.github.com`) appears low-activity; default branch last pushed in 2023.
- Fork (`friuns2/resume.github.com`) is now serving as an active community-maintained branch.
- All currently open upstream pull requests that were fetchable were reviewed and merged into the fork in this run.

## Merged Pull Request Summary (This Run)
- #241: Fixed missing avatar. (https://github.com/resume/resume.github.com/pull/241) by @norchard
- #249: Create test (https://github.com/resume/resume.github.com/pull/249) by @Hemoroide
- #250: Update HTML5Shiv to latest version (https://github.com/resume/resume.github.com/pull/250) by @coliff
- #252: Code refactor, add gitignore file, add profile image. (https://github.com/resume/resume.github.com/pull/252) by @sbimochan
- #259: Update resume.css (https://github.com/resume/resume.github.com/pull/259) by @akbknight
- #263: Fix followers 404 (https://github.com/resume/resume.github.com/pull/263) by @spencerpogo
- #264: Update README.markdown (https://github.com/resume/resume.github.com/pull/264) by @shivamsinghraipur
- #265: Added some meta tags for better view. (https://github.com/resume/resume.github.com/pull/265) by @ritik1234
- #271: Correction of the "followers" link on the resume (https://github.com/resume/resume.github.com/pull/271) by @lgmgeo
- #275: grammar fix in views/contrib.html (https://github.com/resume/resume.github.com/pull/275) by @Daniel-Mietchen
- #294: changed (https://github.com/resume/resume.github.com/pull/294) by @MuhammadAdilMemon

## Deterministic Merge/Conflict Policy
- PRs are merged one-by-one in PR number order.
- Conflict strategy: prefer PR-side changes (`git merge -X theirs`) for deterministic outcomes.
- If fetch/checkout fails after retry, mark as skipped with reason. (No skips this run.)

## Unresolved Risks
- Legacy Ruby/Rack stack may have dependency drift and unpatched CVEs.
- Historical PRs were merged without full CI parity against original contributor environments.
- Project has no enforced modern CI gate in this fork yet.

## Setup Instructions
1. Install Ruby and `rack`.
2. Run `rackup config.ru`.
3. Open local server URL and test `/?<github-username>` rendering.

## Next Maintenance Actions
1. Add CI for linting/basic runtime smoke tests.
2. Audit merged PRs for styling and content regressions with snapshot checks.
3. Review GitHub API integration for rate-limit handling and schema changes.
4. Triage any new upstream PRs hourly and continue deterministic merge policy.

## Run Metadata
- Updated at: 2026-02-26 02:04:21Z
- Maintained fork: https://github.com/friuns2/resume.github.com
- Upstream scanned: https://github.com/resume/resume.github.com
