
```
██████╗ ██╗      █████╗  ██████╗██╗  ██╗ ██████╗██╗ ██████╗ ██╗   ██╗███████╗██████╗
██╔══██╗██║     ██╔══██╗██╔════╝██║ ██╔╝██╔════╝██║██╔═══██╗██║   ██║██╔════╝██╔══██╗
██████╔╝██║     ███████║██║     █████╔╝ ██║     ██║██║   ██║██║   ██║█████╗  ██████╔╝
██╔══██╗██║     ██╔══██║██║     ██╔═██╗ ██║     ██║██║   ██║╚██╗ ██╔╝██╔══╝  ██╔══██╗
██████╔╝███████╗██║  ██║╚██████╗██║  ██╗╚██████╗██║╚██████╔╝ ╚████╔╝ ███████╗██║  ██║
╚═════╝ ╚══════╝╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝ ╚═════╝╚═╝ ╚═════╝   ╚═══╝  ╚══════╝╚═╝  ╚═╝
```

<p align="center">
  <a href="https://t.me/BlackC1over"><img src="https://img.shields.io/badge/@BlackC1over-191919?style=flat-square&logo=telegram"/></a>
  <a href="https://github.com/BlackC1over/END_Tagger"><img src="https://img.shields.io/badge/END_Tagger-бот-22C55E?style=flat-square&labelColor=111"/></a>
  <img src="https://komarev.com/ghpvc/?username=BlackC1over&style=flat-square&color=8B5CF6"/>
</p>

<p align="center">
  <b>Data Engineer / Solo DE · DevOps · Администратор инфраструктуры</b><br>
  <sub>Семён · seller.ru (AI&ML) · Екатеринбург</sub>
</p>

---

## 🎯 Кто я

**Единственный инженер данных в команде.** Сам нахожу проблемы, проектирую архитектуру, пишу код, поднимаю инфраструктуру, документирую и администрирую.

> DE + DevOps + Аналитик + Архитектор = Solo DE  
> Ментора нет — я сам

| Метрика | Значение |
|---------|----------|
| **Задачи (7 мес)** | 97 задач · 74 закрыто (76%) · 30 blocker/critical |
| **Комментарии** | 519 · 69 задач с обсуждениями |
| **Worklog** | 218 часов · 130 записей |
| **Проактивность** | 30 задач создал сам · 52% self-assigned |
| **Очереди** | BusinessAnalyst + NikasDev + DataScientist + TheChumbucket |

---

## 🧰 Стек — что реально используется в коде

### Языки и рантаймы
`Python 3.12` · `asyncio` · `JavaScript` (JSX) · `Bash` / `PowerShell` · `SQL`

### Базы данных
`ClickHouse 26.1` — ReplacingMergeTree, MergeTree, SCD2, cityHash64, INSERT ALL  
`Redis 7.2` — Pub/Sub, asyncio · `PostgreSQL` — asyncpg · `SQLite` — WAL mode

### Основные библиотеки
`aiogram 3` (FSM) · `aiohttp` · `httpx` · `hvac` (Vault) · `clickhouse-driver` / `clickhouse-connect`  
`redis-py` · `asyncpg` · `pydantic` · `python-dotenv` · `paramiko` (SFTP) · `pytest` / `pytest-asyncio` · `ruff`

### Инфраструктура
`Docker` / `Docker Compose` (multi-stage, свои Dockerfile)  
`Linux Ubuntu 24.04` · `Kubernetes` (осваиваю)  
`Nginx` · `Grafana` · `Prometheus` · `HashiCorp Vault` (AppRole)  
`Yandex S3` · `webdis` (HTTP → Redis) · `SSH` (туннели, порты, SOCKS5)

### CI/CD и деплой
`GitLab CI` — selective builds для микросервисов  
`GitHub Actions` — SSH + Docker деплой  
`SCP` / `SFTP` (paramiko) · `Docker Compose` на проде

### Интеграции
`Wildberries API` · `Ozon Seller API` · `Yandex Market API`  
`1С Denvic` (выгрузка + webdis) · `Bitrix24 API` · `Telegram Bot API`  
`Twitch API` · `YouTube API` · `Yandex Tracker API`

### AI
`OpenCode CLI` · `Claude` · `Gemini` · `OpenAI`  
`RAG` + `Obsidian` (self-knowledge) · `MCP`

### Web3
`Solidity` · `Ethereum` · `web3.py` · `Foundry`

### Фронт и тулы
`React` / `Vite` / `TailwindCSS` · `Dexie.js` (IndexedDB)  
`Obsidian` (база знаний) · `Markdown` (документация)

---

## 🖥 Администрирование и инфраструктура

Сам поднимаю сервера, настраиваю, деплою, мониторю и чиню.

```
┌─ VPS ────────────────────────────────────────┐
│  194.85.249.26 · Ubuntu 24.04                │
│  ┌──────────┐ ┌────────────┐ ┌────────────┐  │
│  │Telegram  │ │   SOCKS5   │ │   XRay     │  │
│  │Bot       │ │   Proxy    │ │   VPN      │  │
│  │Docker    │ │   :1080    │ │            │  │
│  └──────────┘ └────────────┘ └────────────┘  │
├──────────────────────────────────────────────┤
│  PROD: Vault:8200 · Grafana:3000 · Prom      │
│  DEV:  Vault (тесты)                         │
│  CH:   ClickHouse:8123 · MCP:3838            │
│  SSH туннели · Проброс портов                │
└──────────────────────────────────────────────┘
```

**Деплой:** Docker Compose пишу сам. CI/CD настраиваю сам. Доку к docker-compose и Dockerfile веду сам. SSH/SFTP для ручного деплоя.

**Мониторинг:** Grafana дашборды, Prometheus метрики, Bitrix24 + Telegram алерты. Если что-то упало — я первый узнаю и первый чиню.

**Lock-механизмы в проектах:**
- S3 Lock-файл — защита конкурентных бэкапов ClickHouse
- `daemon_tracker.worker_tracker` — координация 12 воркеров маркетплейсов
- Recovery cycle в 1С Denvic → DWH — zero-loss на случай сбоя Redis/сети

---

## 🏗 Проекты

### 🏭 DWH 3 маркетплейсов (Wildberries, Ozon, Yandex Market)
**12 микросервисов** в Docker Compose. Спроектировал архитектуру, написал все Dockerfile, docker-compose, CI/CD, документацию.
- Bronze (raw API) → Silver (нормализация) → Mart (витрина seller_stocks)
- SCD2 для истории остатков. ReplacingMergeTree + cityHash64 для дедупликации
- `daemon_tracker.worker_tracker` — воркеры ждут друг друга перед пересборкой
- HashiCorp Vault для API-ключей. Ниหนึ่ง секрет в коде
- GitLab CI с точечной сборкой (только изменённый воркер)
- Инкрементальная загрузка, rate limiting, chunked inserts по 100 записей

### 🔄 1С Denvic → DWH в реальном времени
**Redis Pub/Sub + webdis → 3 asyncio-цикла:** Listener + Worker + Recovery
- HTTP-сигнал из 1С → webdis → Redis → ClickHouse. Задержка < 1 сек
- Recovery polling — ни одна проводка не потеряна при сбое
- 4 уровня safety-check: защита от дублей, zero-safety, empty check, error handling
- cityHash64 в ReplacingMergeTree для идемпотентности

### 💾 ClickHouse Backup Daemon
Авто-бэкап всех PROD БД в Yandex S3 каждые 3 часа
- S3 Lock-файл — предотвращает конкурентные запуски
- Верификация: восстановление на DEV + сверка row count
- Ретенция 24ч с ротацией. Bitrix24 + Telegram со структурным отчётом
- Load testing перед запуском в прод

### 🤖 Telegram Bot — @QZarBot (END_Tagger)
Чат-менеджер с AI саммари через OpenCode CLI
- Twitch/YouTube алерты, дни рождения, pidor-статистика per-chat
- aiogram 3 (FSM), SQLite WAL, Docker на VPS
- Миграции БД, тесты (pytest), CI/CD через GitHub Actions

### 🧠 Курс Junior DE
12 уроков по ETL архитектуре и паттернам. Разбор анти-паттернов. Код-стайл. Реальные примеры из прода.

---

## 🤖 AI как советчик, а не раб

Не прошу написать код — прошу помочь подумать.

`OpenCode CLI` · `Claude` · `Gemini` · `OpenAI`  
`RAG + Obsidian` (личная база знаний) · `MCP инструменты` · `AI code review`

AI — это сеньор у меня в кармане. Код пишу сам, тесты пишу сам, архитектуру проектирую сам.

---

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=BlackC1over&theme=react-dark&hide_border=true&area=true" width="95%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/DWH-с_нуля-8B5CF6?style=flat-square"/>
  <img src="https://img.shields.io/badge/1С_выгружаю-EF4444?style=flat-square"/>
  <img src="https://img.shields.io/badge/VPS_администрирую-3B82F6?style=flat-square"/>
  <img src="https://img.shields.io/badge/Lock_механизмы-22C55E?style=flat-square"/>
  <img src="https://img.shields.io/badge/Документацию_веду-F59E0B?style=flat-square"/>
  <img src="https://img.shields.io/badge/AI_советчик_не_раб-8B5CF6?style=flat-square"/>
  <img src="https://img.shields.io/badge/Сборка_пиздатая-EF4444?style=flat-square"/>
</p>
