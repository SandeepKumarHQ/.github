# GitHub organization defaults

The public organization introduction is in profile/README.md. Canonical strategy belongs in the private HQ repository, factual research in private Knowledgebase, and approved publishing in public project repos. No GitHub Actions schedulers or scraping jobs are introduced.

## Mandatory agent guardrails

Every repository's `AGENTS.md` must follow the common safety circuit breaker. See [organization-wide agent safety](AGENTS.md). The authoritative full policy lives in private Security-Guardrails and the executable local preflight in Automation. We do not use Actions for agents, schedulers, research crawlers or persistent business automation.
