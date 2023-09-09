# Argo experimental personal labs

## Experimental applications

Available Applications:

| Applications  | DNS | Username  | Password | Links |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Clickhouse | <https://clickhouse.local.com.br/play?user=admin> | admin | password | <https://clickhouse.com> |
| Redpanda |redpanda-0.redpanda.redpanda.svc.cluster.local.:9093 | admin | password | <https://redpanda.com> | |
| Redpanda/console | <http://redpanda.local.com.br> | admin | password | <https://redpanda.com/redpanda-console-kafka-ui> | |
| Kafka | kafka-controller-0.kafka-controller-headless.kafka.svc.cluster.local.:9092 | admin | password | <https://kafka.apache.org/> | |
| Kafka/console | <http://kafka.local.com.br> | <admin@conduktor.io> | password | <https://www.conduktor.io/console/> | |

## ArgoCD Folders organization

### Base

- **base/applications-data**: Contains k8s observability applications

### Overlay

Environments folders that inherit from base folder. It uses [kustomize](https://github.com/kubernetes-sigs/kustomize) to allow environment based customization.

### Limitations

- open issue working with clickhouse keeper <https://github.com/bitnami/charts/issues/15935>
