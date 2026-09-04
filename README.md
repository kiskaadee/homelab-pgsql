# 🐘 Homelab PostgreSQL & Adminer

Relational database backend stack with PostgreSQL 16 engine and Adminer web management console.

---

## 🏗️ Architecture & Requirements

- **Proxy Network**: Attached to external `proxy-net`
- **Domain**: `pgsql.roadtotech.me`
- **Target Port**: `8080` (Adminer Web GUI), `5432` (PostgreSQL TCP)

---

## ⚙️ Configuration & Metadata (`app.yaml`)

```yaml
name: "pgsql"
aliases:
  - "postgres"
  - "db-sql"
domain: "pgsql.roadtotech.me"
description: "PostgreSQL Database Engine & Adminer Web Client"
visible: false
auth: false
networks:
  - proxy-net
env:
  POSTGRES_DOMAIN: "pgsql.roadtotech.me"
```

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up pgsql
```

### Manual Deployment
```bash
docker compose up -d
```

---

## 📄 License
This repository is released into the public domain under the [Unlicense](LICENSE).
