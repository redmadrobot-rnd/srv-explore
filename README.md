# srv-explore

Безопасный readonly-эксплорер сервера: MCP-интерфейс для кодового агента рядом
с данными, логами и сервисами. Вынесен из
[very-ai-framework](https://github.com/redmadrobot-rnd/very-ai-framework) в
отдельный репозиторий — этот репо и есть source of truth.

- **Документация** — [`srv_explore/README.md`](srv_explore/README.md)
- **Плагины** (docker/postgres/redis/mongo/rabbitmq) — [`srv_explore/PLUGINS.md`](srv_explore/PLUGINS.md)

## Деплой

Actions → **«Deploy srv-explore (host service)»** → выбрать environment.
Environment на каждый целевой хост; нужны `SSH_HOST`/`SSH_USER` (variables),
`SSH_KEY` + `CLAUDE_CODE_OAUTH_TOKEN` (secrets). Идемпотентно: scp бандла +
`install.sh` + systemd.
