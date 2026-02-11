# Домашнее задание к занятию «Базовые объекты K8S» - Крюков Егор

### Цель задания

В тестовой среде для работы с Kubernetes, установленной в предыдущем ДЗ, необходимо развернуть Pod с приложением и подключиться к нему со своего локального компьютера. 

------

### Чеклист готовности к домашнему заданию

1. Установленное k8s-решение (например, MicroK8S).
2. Установленный локальный kubectl.
3. Редактор YAML-файлов с подключенным Git-репозиторием.

------

### Инструменты и дополнительные материалы, которые пригодятся для выполнения задания

1. Описание [Pod](https://kubernetes.io/docs/concepts/workloads/pods/) и примеры манифестов.
2. Описание [Service](https://kubernetes.io/docs/concepts/services-networking/service/).

------

### Задание 1. Создать Pod с именем hello-world

1. Создать манифест (yaml-конфигурацию) Pod.
2. Использовать image - gcr.io/kubernetes-e2e-test-images/echoserver:2.2.
3. Подключиться локально к Pod с помощью `kubectl port-forward` и вывести значение (curl или в браузере).

------

### Задание 2. Создать Service и подключить его к Pod

1. Создать Pod с именем netology-web.
2. Использовать image — gcr.io/kubernetes-e2e-test-images/echoserver:2.2.
3. Создать Service с именем netology-svc и подключить к netology-web.
4. Подключиться локально к Service с помощью `kubectl port-forward` и вывести значение (curl или в браузере).

------

### Решение

## Задание 1. Создать Pod с именем hello-world

**Манифест:** [task1-pod.yaml](hw/task1-pod.yaml)

**Результат запуска:**
![Скриншот](hw/1.png)

**Результат подключения (port-forward):**
![Скриншот](hw/2.png)

## Задание 2. Создать Service и подключить его к Pod

**Манифест Pod:** [task2-pod.yaml](hw/task2-pod.yaml)
**Манифест Service:** [task2-service.yaml](hw/task2-service.yaml)

**Статус подов и сервисов:**
![Скриншот](hw/3.png)

**Результат подключения через Service:**
![Скриншот](hw/4.png)
