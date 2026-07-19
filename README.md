# Delivery Service Infrastructure

Репозиторий содержит инфраструктурное окружение для локальной разработки и тестирования сервиса Delivery. Все компоненты
упакованы в Docker Compose и настроены для совместной работы. Остальные продуктовые сервисы (**Basket, Discount, Geo**), необходимые для работы
**Delivery**
находятся [в репозитории Кирилла Ветчинкина](https://gitlab.com/microarch-ru/ddd-in-practice/infrastructure)

- Kafka
- [Kowl](http://localhost:8087)
- Debezium
- [Backoffice](http://localhost:8086)

#### Поднять инфраструктуру

Cоздать все:
```
docker compose up -d
```

Cоздать выборочно (удалите лишнее):
```
docker compose up -d  kafka init-kafka kowl debezuim connect-init backoffice
```

Остановить и полностью удалить контейнеры:
```
docker compose down --remove-orphans
```