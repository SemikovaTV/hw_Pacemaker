# Домашнее задание к занятию 10.3 «Pacemaker» - Семикова Т.В. FOPS-9
### Задание 1

Опишите основные функции и назначение Pacemaker.

*Приведите ответ в свободной форме.*

Pacemaker - программное обеспечения для настройки отказоустойчивых систем. Например, с его помощью можно настроить кластер серверов высокой доступности.
- позволяет находить и устранять сбои на уровне нод и служб;
- не зависит от подсистемы хранения;
- не зависит от типов ресурсов: все, что можно прописать в скрипты, можно кластеризовать;
- поддерживает STONITH (Shoot-The-Other-Node-In-The-Head), то есть остановленная нода изолируется и запросы к ней не поступают, пока нода не отправит сообщение о том, что она снова в рабочем состоянии;
- поддерживает кворумные и ресурсозависимые кластеры любого размера;
- поддерживает практически любую избыточную конфигурацию;
- может автоматически реплицировать конфигурации на все узлы кластера — не придется править все вручную;
- можно задать порядок запуска ресурсов, а также их совместимость на одном узле;
- поддерживает расширенные типы ресурсов: клоны (когда ресурс запущен на множестве узлов) и дополнительные состояния (master/slave и подобное) — актуально для СУБД (MySQL, MariaDB, PostgreSQL, Oracle);
имеет единую кластерную оболочку CRM с поддержкой скриптов.
---

### Задание 2

Опишите основные функции и назначение Corosync.

*Приведите ответ в свободной форме.*

Corosync программный продукт, позволяющий реализовать кластер серверов. Его основное назначение — знать и передавать состояние всех участников кластера.
Этот продукт позволяет:

- мониторить статус приложений;
- оповещать приложения о смене активной ноды в кластере;
- отправлять идентичные сообщения процессам на всех нодах;
- предоставлять доступ к общей базе данных с конфигурацией и статистикой;
- отправлять уведомления об изменениях, произведенных в базе.

---

### Задание 3

Соберите модель, состоящую из двух виртуальных машин. Установите Pacemaker, Corosync, Pcs. Настройте HA кластер.

*Пришлите скриншот рабочей конфигурации и состояния сервиса для каждого нода.*
