# 🐘 Homelab PostgreSQL

Primary relational database instance for self-hosted apps and development services.

Part of the [homelab-core](https://github.com/kiskaadee/homelab-core) cluster ecosystem.

---

## 🏗️ Architecture & Storage

- **Container Image**: `postgres:16-alpine`
- **Storage**: Docker named volume `postgres_data`
- **Network**: `proxy-net`
- **Port**: `5432`
- **Domain**: `pgsql.arch-services.mywire.org`

---

## ⚙️ Environment Variables & Secrets

| Variable | Description | Source |
| :--- | :--- | :--- |
| `POSTGRES_USER` | Master superuser name | SOPS secrets |
| `POSTGRES_PASSWORD` | Master password | SOPS secrets |
| `POSTGRES_DB` | Default database name | SOPS secrets |

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up homelab-pgsql
```

### Manual Deployment
```bash
docker compose up -d
```
