쿠버네티스_프로메테우스_그라파나_오토스케일링

$ cd ~
$ kubectl top node
-- error: Metrics API not available
$ kubectl top pod
-- error: Metrics API not available

metric-server

$ kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/download/v0.6.1/components.yaml

$ kubectl edit deploy -n kube-system metrics-server
----------------------------------------
# `spec.template.spec.containers.args` 아래에 추가
--kubelet-insecure-tls

![image](https://github.com/doitcomet/grafana/assets/148560062/7c94d2ab-1d5e-44dc-b2c8-25cde45d0ec4)


