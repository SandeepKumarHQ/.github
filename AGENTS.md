# Organization-wide agent safety — SandeepKumarHQ

**MANDATORY for all AI assistants and developers modifying any SandeepKumarHQ repository.**

Canonical private policy (authorized organization agents): `SandeepKumarHQ/Security-Guardrails/docs/policies/GITHUB-SAFETY-GUARDRAILS.md`. Machine policy and offline preflight: `SandeepKumarHQ/Automation/policy/github-guardrails.json` and `scripts/check_github_actions_policy.py`.

## Hard rules
1. GitHub is for repositories, issues, pull requests, reviews, releases and *human-approved lightweight repository CI only*. GitHub Actions is NOT an agent runtime or free general compute.
2. No autonomous agents, model inference, recurring research, scheduled business jobs, crawlers/scrapers, queue workers, persistent services, backups, mirroring, media rendering or heavy test/benchmark/fuzz workloads on Actions. Use authorized local/controlled VPS infrastructure.
3. Do not create or modify `.github/workflows/*` or add self-hosted Actions runners, workflow secrets, permissions or production deployment without **explicit owner approval** and local scanner evidence. Cron/schedule forbidden by default.
4. Internal CI default: job timeout <=15 minutes, <=2 parallel jobs, <=8 matrix expansions, zero retries, required concurrency, read-only permissions, artifact retention <=3 days.
5. Restriction-/abuse-/suspension-/flagging-related 403, HTTP 429, secondary rate limit, repeated permission failure or unexpected hidden repo: **STOP ALL GitHub writes and retries.** Preserve exact error, do not create alternate accounts/runners/workflows to evade restrictions, and require human authorization to resume.
6. Org-wide mutation affecting >3 repos or >20 GitHub writes requires scoped owner approval. Do not spam branches, issues, comments or API calls.
7. GitHub Pages is not implicitly approved commercial hosting. Production host must be designated separately.
8. Agents cannot approve their own policy exceptions; exceptions must be documented, narrowly scoped and expiring.
9. Preserve existing stronger safeguards, validate before writes, and document verified commit SHAs and test results. Never claim the cause of GitHub enforcement without confirmation from GitHub.

This file is deliberately self-contained because some public agents cannot read the private canonical policy. In disagreement, stronger applicable protections win.
