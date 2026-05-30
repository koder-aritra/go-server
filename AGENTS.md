# AGENTS.md - Project Guide for AI Agents

## General Rules
- When uncertain about any decision, design choice, or course of action — ask the user before proceeding. Do not assume.

## Project Overview
A Go web server project (initial scaffold; intended to grow into an HTTP server serving static files).

## Project State
- **Module**: Not yet initialized (no `go.mod`). Run `go mod init github.com/<user>/go-server` before adding dependencies.
- **Dependencies**: Stdlib only (`fmt`). Planned: `net/http`, `log`.
- **Static assets**: `static/` directory (empty) for future HTML/CSS/JS.

## Commands

| Action | Command |
|---|---|
| Run | `go run .` |
| Build | `go build -o server.exe .` |
| Test | `go test ./...` |
| Format | `go fmt ./...` |
| Vet | `go vet ./...` |

## Conventions
- Keep the project as a single `main` package until it grows enough to warrant splitting into subpackages.
- Use stdlib `net/http` for the HTTP server (no third-party frameworks unless discussed).
- Test files: `*_test.go` alongside source files, using stdlib `testing` package.
- No comments in production code unless the logic is non-obvious.
- Run `go fmt ./...` and `go vet ./...` before every commit.

## Future Plans (inferred from commented-out imports)
- Serve static files from `static/` directory.
- HTTP server with stdlib `net/http`.
- Logging via stdlib `log` package.
