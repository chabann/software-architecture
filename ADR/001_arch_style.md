# ADR 001: Выбор архитектурного стиля системы

## Контекст
Проект требует построения масштабируемого, поддерживаемого и гибкого приложения для фитнес-сервиса с мобильным клиентом, административным порталом и серверной частью. Необходимо обеспечить возможность быстрого развития и интеграции новых функций.

## Варианты решения
1. Монолитная архитектура  
2. Микросервисная архитектура  
3. Серверлесс архитектура  
4. Гибридный подход (микросервисы + монолит)

## Принятое решение
Выбрана микросервисная архитектура.

## Обоснование
- Обеспечивает независимую разработку и развертывание сервисов.  
- Улучшает масштабируемость и отказоустойчивость.  
- Позволяет использовать разные технологии для разных сервисов.  
- Поддерживает гибкое развитие и интеграцию.

## Последствия
| Риск                          | Митигация                                                                 |
|-------------------------------|---------------------------------------------------------------------------|
| Сложность отладки             | Внедрение распределенного трейсинга (Jaeger) и централизованных логов    |
| Задержки в межсервисном обмене | Оптимизация API (при необходимости использование gRPC вместо REST), кэширование (Redis)                  |
| Согласованность данных        | Корректное разделение на домены и области ответственности, в остальных случаях использование Saga-паттерна и событийной репликации                |
| Высокая стоимость DevOps      | Автоматизация CI/CD (GitLab + ArgoCD), настройка мониторинга и оповещений (Prometheus + Grafana)    |
