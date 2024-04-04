# 2024-spring-ab-python-ads-HW-7

На Kind-кластере развернуть SeldonCore + Prometheus + Graphana. Реализовать с помощью SeldonDeployment приложение на основе uplift-модели с endpoint'ом ```/predict```, который по фичам клиента возвращает предсказание uplift (вероятность покупки с промо - вероятность покупки без промо). Построить в Graphana дэшборд, показывающий количество успешных реквестов во времени.

Все шаги описать в Makefile вида:
```yaml
train:
    python train.py

build:
    mlserver build . -t [YOUR_CONTAINER_REGISTRY]/[IMAGE_NAME]

kind-cluster:
    kind create cluster --name seldon-cluster --config kind-cluster.yaml --image=kindest/node:v1.21.1

ambassador:
    ###

seldon-core:
    ###

...
```
