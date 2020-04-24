Prometheus (not working!)

This project is intended to showcase prometheus monitoring service over a Kubernetes
cluster. This involved using a manifest for "kube state metrics" to allow nodes
to scrape metrics, and then sending these metrics to the prometheus deployment,
where the results would be shown in browser.

step-by-step (not currently working!):
This is using vagrant and VM virtualbox
- download/clone repo
- once in repo folder, "vagrant up" the multi-machines
- once up "vagrant ssh Kube-master" to enter the master node
- use "kubectl apply -f /home/ubuntu/metrics/" to deploy kube-state-metrics
- use "kubectl create namespace monitoring" to create the namespace for the monitoring service
- use "kubectl apply -f /home/ubuntu/prometheus/" to deploy Prometheus
- access the console with ip "192.168.10.105:30000"

Issues:
- The console does not show up on the ip above after steps are followed
