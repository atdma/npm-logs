# Nginx Proxy Manager Log Dashboard

A ready-to-run Loki + Grafana stack that parses Nginx Proxy Manager access and error logs into a pre-built dashboard.

```
  NPM Log Files ──> Promtail ──> Loki ──> Grafana
  (your host)       (parse)      (store)   (visualize)
```

## Setup

1. Copy and edit the environment file:

   ```bash
   cp .env.example .env
   ```

   Set `NPM_LOG_DIR` to your NPM logs directory (default: `/data/compose/1/data/logs`).

2. Start the stack:

   ```bash
   docker compose up -d
   ```

3. Open Grafana at [http://localhost:3000](http://localhost:3000) (default login: `admin` / `admin`).

The **Nginx Proxy Manager Logs** dashboard is pre-loaded and ready to use.
