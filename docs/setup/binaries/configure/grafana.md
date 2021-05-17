# Grafana

You can configure Grafana threw the grafana.ini file. If you followed the guide in this docs cou can find it under `/etc/grafana/grafana.ini
`

## Serve Grafana On Subpath

If you have configured a reverse proxy, you can serve grafana on a subpath.
Uncomment `root_url` and `serve_from_sub_path` in the `[server]` section. Change the root_url to your needs. For example:
```
[server]
# The full public facing url you use in browser, used for redirects and emails
# If you use reverse proxy and sub path specify full url (with sub path)
root_url = %(protocol)s://%(domain)s:%(http_port)s/grafana/

# Serve Grafana from subpath specified in `root_url` setting. By default it is set to `false` for compatibility reasons.
serve_from_sub_path = true
```

## Anonymous Auth

You can configure grafana with anonymous Auth. That way users can view your read-only dashboard withoud log in.

```
#################################### Anonymous Auth ######################
[auth.anonymous]
# enable anonymous access
enabled = true

# specify organization name that should be used for unauthenticated users
org_name = Main Org.

# specify role for unauthenticated users
org_role = Viewer

# mask the Grafana version number for unauthenticated users
;hide_version = false
```

## Add Dashboard

Go to the Grafana dashboard. Go to `+` -> `Import` and upload or past on of the dashboards in this repo there.
We have different dashboard for either [single node setups](https://github.com/Dr-Electron/iota-grafana/tree/main/configs/single-node/grafana)
or [multi node setups]() 
<!-- TO-DO --->
 