# .github

Shared GitHub Actions for Crucible repositories.

## Actions

- **set-version** determines project version metadata from Git history.
Outputs `version` (semver from the latest tag, `v` prefix stripped), `stage`
(current branch name), and `commit` (short commit hash).

- **verify-go-modules** ensures Go module files are tidy, downloaded, and
verified. Fails the build if `go.mod` or `go.sum` would change after running `go mod tidy`.

- **go-test-coverage** runs `go test` with coverage, checks a minimum threshold
(default 50%), and uploads an HTML report and a JSON badge as build artifacts.
Accepts a `coverage-threshold` input and outputs the `coverage` percentage.
