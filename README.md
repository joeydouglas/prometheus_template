## Prometheus/Alertmanager Template and RocketChat Integration

Template for deploying Prometheus and Alertmanager built from the Origin example:
\
https://github.com/openshift/origin/blob/master/examples/prometheus/prometheus.yaml.
\

Original RocketChat integration:
\
https://github.com/pavel-kazhavets/AlertmanagerRocketChat
\
### Prerequisites

kube-state-metrics:
\
https://github.com/raffaelespazzoli/openshift-enablement-exam/blob/master/misc/prometheus/kubernetes/kube-state-metrics-template.yaml
\
node-exporter:
\
https://github.com/openshift/origin/blob/master/examples/prometheus/node-exporter.yaml


### Installing

Prometheus:
```
oc proccess -f prometheus-template.yaml | oc apply -f -
```
The RocketChat integration needed to be updated because it defaults to displaying the 'instance'. When alerting on resource requests the instance label Prometheus provides is the pod and we're more concerned about the overal 'node'. Install notes can be found here:
\
https://github.com/pavel-kazhavets/AlertmanagerRocketChat
