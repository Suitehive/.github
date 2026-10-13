# Contributing to Suitehive

Thanks for helping build Suitehive. This guide applies to every repository in the organization
unless a repository has its own `CONTRIBUTING.md`.

## Ways to help

- **Report a bug:** open an issue in the repository it belongs to (not sure which? use
  [suitehive](https://github.com/Suitehive/suitehive)). Include what you did, what you expected and what happened.
- **Suggest a feature:** open a feature request and describe the problem you're trying to solve.
- **Improve the docs:** documentation lives in the [website](https://github.com/Suitehive/website) repository.
- **Write code:** pick an issue labelled `good first issue` or `help wanted`, comment that you're on it,
  then open a pull request.

## Before you write code

1. Read the developer guide **"Your first 15 minutes"** in the website docs. It gets all three apps running
   locally with demo data.
2. Skim the engineering principles in
   [architecture/docs/design/00-engineering-principles.md](https://github.com/Suitehive/architecture/blob/main/docs/design/00-engineering-principles.md).
   The short version:
   - each service keeps business rules in `domain/`, use cases in `app/`, and databases, HTTP and protocols in `adapters/`
   - services never import each other's code; they talk through
     [contracts](https://github.com/Suitehive/contracts) (RPC and events)
   - every table carries `org_id` and is protected by row-level security
3. For anything bigger than a small fix, open an issue first so we can agree on the approach.

## Pull requests

- Keep each PR focused on one change. Small PRs get reviewed faster.
- Add or update tests: unit tests for domain logic, integration tests against the dev Postgres for adapters.
- Go: `go build ./... && go vet ./... && go test ./...` must pass. Web: `npm run typecheck` and `npm run build`.
- Changing an API? Update the contract in `contracts/` first, then the service and the web client.
- UI changes: include a screenshot (light and dark) and follow the design system in
  [07-ui-design-system.md](https://github.com/Suitehive/architecture/blob/main/docs/design/07-ui-design-system.md).
- Write commit messages in the imperative ("Add DKIM rotation endpoint"), explaining *why* when it isn't obvious.

## Code of conduct

Everyone taking part is expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
