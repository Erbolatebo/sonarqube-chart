# SonarQube Helm Chart

Этот Helm-чарт разворачивает SonarQube с PostgreSQL в Kubernetes-кластере. PostgreSQL подключён как зависимость через Bitnami-чарт.

## Состав

- SonarQube (в Docker-контейнере)
- PostgreSQL (Bitnami chart)
- NodePort-сервис (для доступа через внешний IP)

## Требования

- Kubernetes (в место миникуба как альтернативный вариант, K3s)
- Helm 3.x
- Установлен параметр `vm.max_map_count >= 262144`:

```bash
sudo sysctl -w vm.max_map_count=262144
