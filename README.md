## Prometheus/Alertmanager Template and RocketChat Integration

Template for deploying Prometheus and Alertmanager built from the Origin example:
<br>
https://github.com/openshift/origin/blob/master/examples/prometheus/prometheus.yaml.
<br>

Original RocketChat integration:
<br>
https://github.com/pavel-kazhavets/AlertmanagerRocketChat
<br>
### Prerequisites

kube-state-metrics:
<br>
https://github.com/raffaelespazzoli/openshift-enablement-exam/blob/master/misc/prometheus/kubernetes/kube-state-metrics-template.yaml
<br>
<br>
node-exporter:
<br>
https://github.com/openshift/origin/blob/master/examples/prometheus/node-exporter.yaml


### Installing

Prometheus:
```
oc proccess -f prometheus-template.yaml | oc apply -f -
```
<br>
RocketChat:
<br>
<br>
The RocketChat integration needed to be updated because it defaults to displaying the 'instance'. When alerting on resource requests the instance label Prometheus provides is the pod that has the requests in place but we're more concerned about the overall 'node'. Install notes can be found here:
<br>
https://github.com/pavel-kazhavets/AlertmanagerRocketChat
