# InfraPilot

> Personal Infrastructure Orchestration Platform

---

# О проекте

InfraPilot — это персональная платформа управления инфраструктурой, разрабатываемая с нуля в образовательных и практических целях.

Основная задача проекта — создать единый центр управления домашней лабораторией, который объединит:

- управление Linux-серверами;
- управление виртуальными машинами VMware;
- управление Docker-контейнерами;
- централизованный мониторинг;
- систему логирования;
- резервное копирование;
- автоматизацию через Ansible;
- управление через Telegram-бота;
- Web Dashboard;
- Kubernetes (на следующих этапах).

Проект разрабатывается поэтапно. Каждый новый модуль добавляется только после полного понимания предыдущего.

---

# Цели проекта

## Основная цель

Создать полноценную платформу управления инфраструктурой, максимально приближенную к реальным корпоративным решениям.

## Дополнительные цели

- Изучение Linux на практике
- Изучение DevOps-инструментов
- Автоматизация рутинных задач
- Построение собственной домашней лаборатории
- Формирование портфолио

---

# Текущий статус

Версия:

0.1.0

Этап:

Фундамент

Статус:

🟢 В разработке

---

# Аппаратная платформа

## Хостовая машина

| Параметр | Значение |
|----------|----------|
| CPU | AMD Ryzen 7 7435HS |
| RAM | 16 GB DDR5 |
| GPU | NVIDIA RTX 4060 8 GB |
| Hypervisor | VMware Workstation Pro 17.5 |

---

## Главный сервер

| Параметр | Значение |
|----------|----------|
| Hostname | debmasterserv |
| ОС | Debian GNU/Linux 13 (Trixie) |
| RAM | 8 GB |
| Disk | 50 GB |
| Разметка | LVM |
| Сеть | DHCP (временно) |

---

# Планируемая архитектура

```
                    Telegram Bot
                          │
                          ▼
                 InfraPilot API
                          │
 ┌──────────────┬──────────┴─────────────┐
 │              │                        │
 ▼              ▼                        ▼
Docker      VMware Manager          Ansible
 │              │                        │
 └──────────────┴───────────────┬────────┘
                                ▼
                      Infrastructure
```

---

# План развития

- [x] Подготовка Debian
- [x] Создание структуры проекта
- [ ] Git Repository
- [ ] Docker
- [ ] PostgreSQL
- [ ] FastAPI
- [ ] Monitoring
- [ ] Telegram Bot
- [ ] Docker Manager
- [ ] VMware Manager
- [ ] Logging
- [ ] Backup
- [ ] Web Dashboard
- [ ] Kubernetes

---

# Структура проекта

```
infrapilot/

api/
ansible/
backups/
bot/
config/
data/
docker/
docs/
logs/
scripts/
tests/
web/
```

---

# Используемые технологии

## Операционная система

- Debian 13

## Языки

- Python
- Bash
- SQL

## Базы данных

- PostgreSQL

## Контейнеризация

- Docker
- Docker Compose

## Автоматизация

- Ansible

## Мониторинг

- Prometheus
- Grafana
- Alertmanager

## Логирование

- Loki
- Promtail

## Оркестрация

- Kubernetes (позже)

---

# Основные принципы

- Infrastructure as Code
- Git First
- Automation First
- Documentation First
- Security by Default
- Каждый этап должен быть полностью завершен перед переходом к следующему.

---

# Лицензия

MIT
