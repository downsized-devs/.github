## Hi there 👋

We're **Downsized Developers**, a small crew of backend engineers based in Indonesia. We build pragmatic Go libraries, service templates, and developer tooling — the stuff we wish existed every time we started a new project. Everything here is open source and battle-tested in production.

## 📦 Our Projects

| Repo | Description | Highlights |
| --- | --- | --- |
| [sdk-go](https://github.com/downsized-devs/sdk-go) | Monorepo of 40+ small, well-scoped Go packages — import only what you need. | Go · MIT |
| [template-service-go](https://github.com/downsized-devs/template-service-go) | Opinionated Go backend starter with Swagger and structured config layout. | Go · service scaffold |
| [docker-events-notifier](https://github.com/downsized-devs/docker-events-notifier) | Watches the Docker socket and pings Slack, Discord, or email on events. | <10MB image · no exposed ports · 3 forks |

## 🚀 Quick Start

Pull in `sdk-go` and wire up a logger with request-scoped context:

```go
import (
    "github.com/downsized-devs/sdk-go/appcontext"
    "github.com/downsized-devs/sdk-go/logger"
)

log := logger.Init(logger.Config{Level: "info"})
ctx := appcontext.SetRequestId(context.Background(), "req-123")
log.Info(ctx, "service ready")
```

Install: `go get github.com/downsized-devs/sdk-go`

## 🧰 What's Inside sdk-go

| Category | Packages |
| --- | --- |
| Config & bootstrap | `appcontext`, `configbuilder`, `configreader`, `featureflag` |
| Logging & observability | `logger`, `errors`, `audit`, `instrument`, `tracker` |
| Data & storage | `sql`, `nosql`, `redis`, `storage`, `query`, `null` |
| Auth & security | `auth`, `security`, `ratelimiter` |
| Messaging | `email`, `messaging`, `slack`, `gqlclient` |
| I18n | `language`, `translator` |
| Time & jobs | `clock`, `dates`, `scheduler` |
| Files | `files`, `pdf`, `parser` |
| Helpers | `convert`, `num`, `stringlib`, `checker`, `operator` |
| Tooling | `generator` (CLI scaffolder), `tests` (gomock fixtures) |

## 🤝 Contributing

Found a bug, want a new package, or have an idea? Fork the repo, open a PR, and ping the team in the discussion thread — we review quickly and welcome first-time contributors. For `sdk-go`, please read [docs/CONTRIBUTING.md](https://github.com/downsized-devs/sdk-go/blob/main/docs/CONTRIBUTING.md) before submitting; it covers our package layout, testing conventions, and release process. Smaller, focused PRs are easier to land than sweeping refactors.

## 📬 Contact

Security issues: please email **alvin.radeka@gmail.com** privately before filing a public issue.
