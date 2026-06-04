# fp-iac

Infrastructure-as-Code repo for Kafka topics, Redis, alerts, and redirects in Team Foreldrepenger.

## Shared context

- Source of truth for shared domain, architecture, and conventions: `navikt/fp-context`
- Copilot Space: `navikt/TeamForeldrepenger`

## Repo-specific context

| Topic              | Details                                                                                               |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Role               | Owns Kafka topic definitions, Redis config, alert rules, redirect config, and Kafka manager manifests |
| Main areas         | `kafka-aiven/`, `redis/`, `alert/`, `redirect/`, `fp-kafka-manager-*.yml`                             |
| Tech stack         | YAML and config only; no application code; NAIS and Aiven in namespace `teamforeldrepenger`                                                           |

## Verification

- Manual after deployment.
