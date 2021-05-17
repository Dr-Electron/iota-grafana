# Prometheus

Modify the prometheus.yml file (if you followed the installation guide mentioned here, it should be located in `/etc/prometheus/prometheus.yml `) to your needs. You can use the [Prometheus template](https://github.com/Dr-Electron/iota-grafana/blob/main/configs/single-node/prometheus/prometheus-template.yml) as an example.
For a simple single node setup you can do:
```
wget https://github.com/Dr-Electron/iota-grafana/blob/main/configs/single-node/prometheus/prometheus-template.yml
mv -f prometheus-template.yml /etc/prometheus/prometheus.yml
```