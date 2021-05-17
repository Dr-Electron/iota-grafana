# Hornet-Config

In Hornet you need to change the `config.json`. 
First enable the `Prometheus` plugin:
```
"node": {
    "alias": "HORNET node",
    "profile": "auto",
    "disablePlugins": [],
    "enablePlugins": [
      "Prometheus"
    ]
},
```

Now you need to enable all prometheus metrics. We don't use the promhttp metrics yet.
```
"prometheus": {
    "bindAddress": "localhost:9311",
    "fileServiceDiscovery": {
      "enabled": false,
      "path": "target.json",
      "target": "localhost:9311"
    },
    "databaseMetrics": true,
    "nodeMetrics": true,
    "gossipMetrics": true,
    "cachesMetrics": true,
    "restAPIMetrics": true,
    "migrationMetrics": true,
    "coordinatorMetrics": true,
    "debugMetrics": true,
    "goMetrics": true,
    "processMetrics": true,
    "promhttpMetrics": false
}
```