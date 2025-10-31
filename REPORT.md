# 🧾 REPORT — Практика 3: CI / DevSecOps

## Репозиторий и ветка
- Repo: <ссылка на репозиторий>
- Основная ветка: `main`

## CI и результаты
- Платформа: GitHub Actions
- Все 7 job успешны ✅:
  - pre-commit checks
  - Build and Test (Docker)
  - Gitleaks (Secrets)
  - Semgrep (SAST, OWASP Top 10)
  - Trivy FS (Dependencies)
  - Trivy Image (Container)
  - SBOM (CycloneDX)

### Артефакты
- `results.sarif` (Gitleaks)
- `semgrep.sarif`
- `trivy-fs.sarif`
- `trivy-image.sarif`
- `sbom.cdx.json`

## Скриншоты
- ✅ Скрин успешного CI (7/7 green)
- ✅ Скрин настроек защиты ветки `main` (ruleset + required checks)

## Выводы
- Пайплайн покрывает тесты, линтинг и проверки безопасности (секреты, SAST, зависимости, контейнер).
- SBOM фиксирует состав зависимостей для контроля цепочки поставок.
- Защита ветки заставляет работать через PR и не пропускает код без зелёных проверок.

## Улучшения
- Включить Code Scanning, чтобы SARIF отображался в Security → Code scanning alerts.
- Добавить уведомления (Slack/Telegram) о статусе CI.
